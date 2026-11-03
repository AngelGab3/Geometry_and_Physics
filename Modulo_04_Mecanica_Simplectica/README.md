# MÓDULO 4: Mecánica Clásica en Variedades Simplécticas
**Duración:** Semanas 13 a 16 (Semanas 13 a 16)  
**Objetivo Pedagógico:** La gran cosecha física del curso. Reconstruir la mecánica clásica de Hamilton a través de la geometría simpléctica intrínseca de Arnold y José & Saletan. Entender los momentos como covectores en el fibrado cotangente $T^*Q$, interpretar las transformaciones canónicas como difeomorfismos simplécticos, probar el teorema de Liouville en una línea, y culminar con la topología del espacio de fases y los toros invariantes de Arnold.

---

## 🔗 Hilo Conductor y Conexión Acumulativa

* **Punto de Partida (Desde Módulos 1, 2 y 3):** Conocemos las 1-formas, el producto cuña $\wedge$, el producto interior $\iota_X$, la derivada exterior $d$ y los espacios de configuración $Q$.
* **Lo que construimos en este módulo:**
  1. El fibrado cotangente $T^*Q$ (espacio de fases canónico) y su 1-forma de Liouville invariante $\theta = p_i\, dq^i$.
  2. La 2-forma simpléctica canónica $\omega = -d\theta = dq^i \wedge dp_i$ y el Teorema de Darboux.
  3. Las ecuaciones de Hamilton sin coordenadas: $\iota_{X_H}\omega = dH$ y los corchetes de Poisson geométricos.
  4. La demostración hidrodinámica del Teorema de Liouville mediante la fórmula mágica de Cartan: $\mathcal{L}_{X_H}\Omega = 0$.
  5. **Topología III (Inspiración Arnold & Nakahara):** La 1-forma de Poincaré-Cartan en el espacio extendido, el Teorema de recurrencia de Poincaré y los **toros invariantes de Liouville-Arnol'd** ($T^n$).
  6. Vista a las partes 2 y 3: La fase clásica de Hannay como el precursor directo de la fase cuántica de Berry y las teorías de norma (Baez & Muniain).

---

## 📚 Desglose de Semanas

### [Semana 13: El Escenario Físico Natural: El Fibrado Cotangente $T^*Q$](Semana_13_Cotangente_TstarQ_Liouville/)
* **Pregunta física:** En termodinámica y mecánica cuántica, la energía y el estado se expresan en términos del momento $p$ y no de la velocidad $\dot{q}$. ¿Por qué el momento lineal es físicamente un covector?
* **Conceptos clave:** La transformación de Legendre como mapeo entre fibrados: $TQ \to T^*Q$, con $p_i = \partial L / \partial \dot{q}^i$. El espacio de fases físico $\mathcal{P} = T^*Q$ con coordenadas canónicas $(q^1, \dots, q^n, p_1, \dots, p_n)$.
* **La 1-Forma Canónica de Liouville (Poincaré):**
  $$\theta = \sum_{i=1}^n p_i\, dq^i$$
  Demostración de que $\theta$ es un objeto geométrico intrínseco, libre de cualquier elección de coordenadas. Su significado físico como la acción mecánica infinitesimal.
* **Modelo visual (Arnold Cap. 8 / José & Saletan Secc. 5.2):** En el espacio $(q, p)$, la forma $\theta$ toma un vector tangente del espacio de fases, proyecta su velocidad sobre la configuración $Q$ y la evalúa contra el momento local $p$.
* **Física:** La integral de acción $\int \theta = \int p\, dq$; el salto natural y geométrico de Lagrange a Hamilton.
* **Lectura asignada:** José & Saletan (Cap. 5, Secc. 5.1–5.2), Arnold (Cap. 3, Secc. 14; Cap. 8, Secc. 41).

---

### [Semana 14: La 2-Forma Simpléctica Canónica ($\omega = -d\theta$) y Teorema de Darboux](Semana_14_Forma_Simplectica_Darboux/)
* **Pregunta física:** ¿Qué estructura matemática reemplaza a la métrica riemanniana en el espacio de fases? ¿Qué miden y preservan las transformaciones canónicas?
* **Conceptos clave:** La 2-forma simpléctica canónica:
  $$\omega = -d\theta = \sum_{i=1}^n dq^i \wedge dp_i$$
  Propiedades fundamentales: cerrada ($d\omega = 0$ garantizado por la nilpotencia $d^2=0$) y no degenerada. Variedades simplécticas abstractas $(\mathcal{M}, \omega)$.
* **Teorema de Darboux:** A diferencia de la geometría riemanniana (donde la curvatura es un invariante local), no existe curvatura simpléctica local; todos los espacios de fases de igual dimensión son localmente idénticos a $\mathbb{R}^{2n}$.
* **Transformaciones Canónicas:** Difeomorfismos $\Phi: \mathcal{M} \to \mathcal{M}$ que preservan la estructura simpléctica:
  $$\Phi^* \omega = \omega$$
* **Física:** Invarianza de áreas en cada plano de coordenadas conjugadas $(q^i, p_i)$.
* **Lectura asignada:** José & Saletan (Secc. 5.2–5.3), Arnold (Cap. 8, Secc. 41 y 43).

---

### [Semana 15: Dinámica Hamiltoniana, Corchetes de Poisson y Teorema de Liouville](Semana_15_Hamilton_Poisson_Liouville/)
* **Pregunta física:** ¿Por qué las ecuaciones de Hamilton llevan un signo menos asimétrico ($\dot{q} = \frac{\partial H}{\partial p}, \dot{p} = -\frac{\partial H}{\partial q}$)? Si soltamos una nube de condiciones iniciales, ¿cómo evoluciona su volumen en el tiempo?
* **Conceptos clave:** El campo vectorial hamiltoniano $X_H$ asociado a la energía $H$, definido por la ecuación universal sin coordenadas:
  $$\iota_{X_H} \omega = dH$$
* **Corchetes de Poisson geométricos:** $\{f, g\} \equiv \omega(X_f, X_g) = X_f[g]$. Conservación de la energía en una sola línea por antisimetría de la 2-forma:
  $$\frac{dH}{dt} = \omega(X_H, X_H) = 0$$
* **La Fórmula Mágica de Cartan y Demostración de Liouville:**
  $$\mathcal{L}_{X_H} \omega = d(\iota_{X_H} \omega) + \iota_{X_H}(d\omega) = d(dH) + \iota_{X_H}(0) = d^2 H = 0 \implies \mathcal{L}_{X_H}\Omega = 0$$
  donde $\Omega = \frac{1}{n!} \omega^n$ es la forma de volumen simpléctico.
* **Modelo visual (Arnold Cap. 3 y 8):** El flujo hamiltoniano es un **fluido rigurosamente incompresible**. La nube de estados se deforma y retuerce en filamentos delgados, pero su volumen de probabilidad es indestructible.
* **Física:** Base geométrica de la mecánica estadística clásica y el Teorema de Gibbs-Liouville.
* **Lectura asignada:** Arnold (Cap. 3, Secc. 16; Cap. 8, Secc. 38–40), José & Saletan (Secc. 5.3.4 y 5.4.1).

---

### [Semana 16: El Invariante de Poincaré-Cartan, Topología III y Vista al Futuro](Semana_16_PoincareCartan_Toros_Futuro/)
* **Pregunta física:** ¿Cómo se unifican el principio variacional, las leyes de conservación y las órbitas en un solo objeto geométrico? ¿Por qué los sistemas integrables acotados terminan viviendo en la superficie de un toro?
* **Conceptos clave:** El espacio de evolución extendido $\mathcal{M} \times \mathbb{R}$ con coordenadas $(q^i, p_i, t)$.
* **La 1-Forma de Poincaré-Cartan de Arnold:**
  $$\omega_H = \sum_{i=1}^n p_i\, dq^i - H(q, p, t)\, dt$$
  El invariante integral: $\oint_{\gamma_1} \omega_H = \oint_{\gamma_2} \omega_H$. Las trayectorias físicas reales son el **núcleo (líneas de vórtice)** de la 2-forma $d\omega_H$:
  $$\iota_{\dot{\gamma}} (d\omega_H) = 0$$
* **Topología III (Inspiración Arnold & Nakahara):**
  * Teorema de Recurrencia de Poincaré: la compacidad de la superficie de energía acotada obliga al sistema a retornar infinitas veces cerca de su estado inicial.
  * Teorema de Liouville-Arnol'd: las foliaciones lagrangianas de sistemas integrables forman **toros invariantes** $T^n = S^1 \times \dots \times S^1$. Variables de acción-ángulo $(I_i, \theta^i)$.
* **Cierre y Vista a las Partes 2 y 3:**
  * *Parte 2 (Electromagnetismo):* La 2-forma de Faraday $F = dA$ en el espacio-tiempo de Minkowski y las ecuaciones de Maxwell unificadas en dos líneas ($dF=0, d{\star}F=J$).
  * *Parte 3 (Fases Geométricas y Gauge):* La fase de Hannay en mecánica clásica como el ancestro directo de la fase cuántica de Berry y las conexiones de Yang-Mills (Baez & Muniain).
* **Lectura asignada:** Arnold (Cap. 9, Secc. 44–45; Cap. 10, Secc. 49–50), José & Saletan (Secc. 6.4.3), Baez & Muniain (Prólogo a la Parte II).

---

## 📋 Estado de Avance y Entregables

| Semana | Tema | Lectura | Slides | Tarea | Estado |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **13** | Fibrado Cotangente $T^*Q$ y Forma de Liouville | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **14** | 2-Forma Simpléctica $\omega$ y Teorema de Darboux | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **15** | Dinámica Hamiltoniana, Poisson y Liouville | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **16** | Poincaré-Cartan, Topología III y Toros de Arnold | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
