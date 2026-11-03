# MÓDULO 2: El Cálculo Exterior de Cartan y Topología I
**Duración:** Semanas 8 a 10 (Semanas 08 a 10)  
**Objetivo Pedagógico:** Dominar las operaciones diferenciales intrínsecas de Cartan ($d, \iota_X$) y descubrir cómo la topología del espacio físico determina la existencia o el fracaso de los potenciales físicos globales (Nakahara). Aplicar los marcos móviles de O'Neill a la cinemática de sistemas rotantes no inerciales.

---

## 🔗 Hilo Conductor y Conexión Acumulativa

* **Punto de Partida (Desde Módulos 0 y 1):** Tenemos la base de 1-formas $dx^i$, 2-formas $dx^i \wedge dx^j$ y el producto antisimétrico gobernado por el álgebra de permutaciones.
* **Lo que construimos en este módulo:**
  1. La derivada exterior $d$ como la densidad de circulación infinitesimal por unidad de área.
  2. La demostración de $d^2 = 0$ usando la simetría de derivadas cruzadas de Schwarz.
  3. **Topología I (Inspiración Nakahara):** El Lema de Poincaré local vs. el fallo global debido a agujeros topológicos. La 1-forma del vórtice $d\theta$, el efecto Aharonov-Bohm y el primer grupo de cohomología de de Rham $H^1(\mathbb{R}^2 \setminus \{0\}) \cong \mathbb{R}$.
  4. La contracción $\iota_X$ y las formas de conexión $\omega_{ij}$ de Cartan para marcos móviles ortonormales en $\mathbb{R}^3$.
* **Hacia dónde vamos (Conexión con Módulo 3):**
  * La nilpotencia $d^2 = 0$ se emparejará con la propiedad topológica de fronteras $\partial^2 = \emptyset$ en el Teorema Generalizado de Stokes.
  * El producto interior $\iota_X$ será el operador con el que formularemos la dinámica hamiltoniana: $\iota_{X_H}\omega = dH$.

---

## 📚 Desglose de Semanas

### [Semana 08: La Derivada Exterior $d$: Densidad de Circulación Local](Semana_08_Derivada_Exterior_Circulacion/)
* **Pregunta física:** Si colocamos una pequeña rueda de paletas en la corriente de un río, ¿qué mide exactamente su rotación en cada punto del plano?
* **Conceptos clave:** La derivada exterior $d: \Omega^k \to \Omega^{k+1}$. Circulación de una 1-forma alrededor de un lazo rectangular infinitesimal $\Delta x \times \Delta y$. Límite del cociente $\text{Circulación} / \text{Área}$. Regla de Leibniz graduada: $d(\alpha \wedge \beta) = d\alpha \wedge \beta + (-1)^{\deg\alpha} \alpha \wedge d\beta$.
* **Modelo visual (Fortney Cap. 4):** Comparación gráfica: el vórtice $V = -y\partial_x + x\partial_y$ (densidad de circulación constante) vs. la fuente $U = x\partial_x + y\partial_y$ (circulación nula). La derivada exterior cuenta cuántos tubos nuevos nacen o mueren localmente.
* **Física:** Circulación hidrodinámica; el rotacional en 2D sin necesidad de invocar una tercera dimensión artificial.
* **Lectura asignada:** Fortney (Cap. 4), Bachman (Cap. 5, Secc. 5.1–5.4), O'Neill (Cap. 1, Secc. 1.6).

---

### [Semana 09: Nilpotencia $d^2 = 0$, Lema de Poincaré y Topología I (Nakahara)](Semana_09_Nilpotencia_Poincare_Topologia/)
* **Pregunta física:** ¿Por qué no existen monopolos magnéticos aislados? ¿Bajo qué condiciones un campo de fuerzas sin rotacional admite realmente una función de energía potencial global?
* **Conceptos clave:** La identidad maestra $d(d\omega) = 0$ y su origen en la simetría de derivadas cruzadas de Schwarz. Formas cerradas ($d\omega = 0$) vs. exactas ($\omega = d\alpha$). El Lema de Poincaré en dominios estrellados de $\mathbb{R}^n$.
* **Topología I (Inspiración Nakahara):**
  * La 1-forma del vórtice: $\omega = \frac{-y\,dx + x\,dy}{x^2+y^2} = d\theta$. Demostración de que $d\omega = 0$ en $\mathbb{R}^2 \setminus \{(0,0)\}$, pero $\oint \omega = 2\pi \neq 0$.
  * Por qué fallan los potenciales: dominios conexos vs. simplemente conexos. El primer grupo de cohomología de de Rham $H^1(\mathbb{R}^2 \setminus \{0\}) \cong \mathbb{R}$ entendido como el detector de un filamento o agujero físico.
* **Física:** El efecto Aharonov-Bohm (física cuántica en un espacio con agujero topológico) y la cuantización de la circulación en helio superfluido y superconductores.
* **Lectura asignada:** Nakahara (Cap. 1, Secc. 1.8–1.9; Cap. 2, Secc. 2.3; Cap. 6, Secc. 6.2–6.3), Bachman (Secc. 5.5–5.6), Baez & Muniain (Cap. 1 y 2).

---

### [Semana 10: Contracción Interior ($\iota_X$) y Marcos Móviles de Cartan en $\mathbb{R}^3$](Semana_10_Contraccion_Marcos_Moviles/)
* **Pregunta física:** ¿Cómo describe el movimiento un piloto dentro de un avión de combate que acelera y gira simultáneamente? ¿Por qué los marcos fijos cartesianos son torpes en dinámica curvilínea?
* **Conceptos clave:** El producto interior $\iota_X: \Omega^k \to \Omega^{k-1}$ y su regla de antiderivación. Marcos ortonormales móviles $\{e_1, e_2, e_3\}$ de O'Neill. 1-formas duales $\theta^i(e_j) = \delta^i_j$.
* **Las 1-Formas de Conexión de Cartan:** $\omega_{ij} = de_i \cdot e_j = -\omega_{ji}$ (conectando directamente con las matrices antisimétricas de rotación infinitesimal de la Semana 03). Las ecuaciones estructurales de Cartan en $\mathbb{R}^3$:
  $$d\theta^i = \sum \omega_{ij} \wedge \theta^j, \qquad d\omega_{ij} = \sum \omega_{ik} \wedge \omega_{kj}$$
* **Modelo visual (O'Neill Cap. 2):** El marco de Frenet-Serret $(T, N, B)$ visto como un marco móvil cuyas tasas de giro son la curvatura $\kappa$ y la torsión $\tau$.
* **Física:** Fuerzas ficticias (fuerza centrífuga y aceleración de Coriolis) deducidas limpiamente a partir de las formas de conexión $\omega_{ij}$; fuerza de Lorentz como contracción $F_L = q\,\iota_v B$.
* **Lectura asignada:** O'Neill (Cap. 2, Secc. 2.1–2.8), Flanders (Cap. 4), Arnold (Cap. 6).

---

## 📋 Estado de Avance y Entregables

| Semana | Tema | Lectura | Slides | Tarea | Estado |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **08** | Derivada Exterior $d$: Densidad de Circulación | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **09** | Nilpotencia $d^2=0$, Poincaré y Topología I | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **10** | Contracción ($\iota_X$) y Marcos Móviles de Cartan | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
