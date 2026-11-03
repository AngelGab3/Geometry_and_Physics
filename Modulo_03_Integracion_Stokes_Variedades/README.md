# MÓDULO 3: Integración, Stokes y Variedades Físicas
**Duración:** Semanas 11 a 13 (Semanas 11 a 13)  
**Objetivo Pedagógico:** Integrar formas sobre variedades sin depender de vectores normales artificiales $\hat{n}$. Demostrar visualmente el Teorema Generalizado de Stokes mediante la cancelación telescópica de celdas internas de Bachman. Comprender por qué la física exige variedades suaves y asimilar el principio fundamental de José & Saletan: las posiciones viven en $Q$, pero las velocidades habitan en el fibrado tangente $TQ$.

---

## 🔗 Hilo Conductor y Conexión Acumulativa

* **Punto de Partida (Desde Módulos 1 y 2):** Dominamos la diferenciación de formas con $d$, la nilpotencia $d^2 = 0$ y la noción de formas cerradas vs. exactas.
* **Lo que construimos en este módulo:**
  1. El operador estrella de Hodge $\star$ que traduce tubos de flujo (2-formas) a líneas de campo (1-formas/vectores).
  2. La demostración por celdas del Teorema de Stokes: $\int_{\partial \Omega} \omega = \int_\Omega d\omega$.
  3. **Topología II (Inspiración Bachman & Nakahara):** Cadenas y ciclos, por qué se requiere orientabilidad (la cinta de Möbius) y compacidad. La dualidad intrínseca $\langle \partial c, \omega \rangle = \langle c, d\omega \rangle$.
  4. Los espacios de configuración reales $Q$ ($S^1, S^2, T^2, SO(3)$) y el paso al **fibrado tangente $TQ$** para el cálculo de variaciones lagrangiano.
* **Hacia dónde vamos (Conexión con Módulo 4):**
  * La transformación de Legendre nos llevará del fibrado tangente $TQ$ (velocidades) al **fibrado cotangente $T^*Q$** (momentos como covectores), donde vive la mecánica hamiltoniana y la geometría simpléctica.

---

## 📚 Desglose de Semanas

### [Semana 11: Integración de Formas y el Operador Estrella de Hodge ($\star$)](Semana_11_Hodge_Integracion_Formas/)
* **Pregunta física:** ¿Cómo calculamos el flujo a través de una superficie curva sin recurrir a la elección arbitraria de un vector normal unitario $\hat{n}$?
* **Conceptos clave:** Integración de $k$-formas sobre subconjuntos parametrizados: $\int_S \omega$. El operador estrella de Hodge $\star: \Omega^k(\mathbb{R}^3) \to \Omega^{3-k}(\mathbb{R}^3)$ inducido por la métrica euclidiana $g_{ij}$ y la orientación $\epsilon_{ijk}$.
* **Modelo visual (Fortney Secc. 5.6):** La estrella de Hodge intercambia visualmente una familia de tubos de flujo (2-forma) con el vector axial que fluye por su interior (1-forma).
* **Física:** Reconstrucción geométrica inmediata de los operadores clásicos:
  $$\text{div}\,\vec{F} = \star d \star (F^\flat), \qquad \text{rot}\,\vec{F} = (\star d (F^\flat))^\sharp, \qquad \Delta f = \star d \star df$$
* **Lectura asignada:** Fortney (Secc. 5.6 y Cap. 7), Bachman (Cap. 4, Secc. 4.1–4.5).

---

### [Semana 12: El Teorema Generalizado de Stokes y Topología II (Bachman & Nakahara)](Semana_12_Stokes_Celdas_Topologia_II/)
* **Pregunta física:** ¿Por qué la suma de todos los pequeños vórtices microscópicos dentro de un fluido equivale exactamente a la velocidad total del fluido a lo largo del borde que lo contiene?
* **Conceptos clave:** Cadenas orientadas y el operador frontera $\partial \Omega$. La fórmula maestra de Stokes-Cartan:
  $$\int_{\partial \Omega} \omega = \int_{\Omega} d\omega$$
* **Topología II (Inspiración Bachman & Nakahara):**
  * Demostración visual de Bachman: descomposición en celdas y **cancelación telescópica** en todas las caras interiores compartidas.
  * Por qué se requiere compacidad (para que el flujo no se escape a infinito) y orientabilidad (por qué la cinta de Möbius no admite una 2-forma de área global que no se anule).
  * La dualidad de Nakahara: la integración como emparejamiento $\langle c, \omega \rangle = \int_c \omega$, donde $d$ es el adjunto formal de $\partial$: $\langle \partial c, \omega \rangle = \langle c, d\omega \rangle$.
* **Física:** Unificación en un solo renglón del Teorema Fundamental del Cálculo, Teorema de Green, Teorema de Stokes clásico y Teorema de la Divergencia de Gauss. Leyes integrales de Maxwell.
* **Lectura asignada:** Bachman (Cap. 6, Secc. 6.1–6.4), Nakahara (Cap. 6, Secc. 6.1), Needham (Cap. 37).

---

### [Semana 13: Espacios de Configuración Físicos ($Q$) y el Fibrado Tangente ($TQ$)](Semana_13_Espacios_Configuracion_TQ/)
* **Pregunta física:** Si un brazo robótico o péndulo doble se mueve en el espacio, ¿dónde vive su estado físico en cada instante? ¿Por qué forzar coordenadas cartesianas $\mathbb{R}^4$ arruina la comprensión del sistema?
* **Conceptos clave:** Ligaduras holónomas y subvariedades diferenciables (generalizando la visión paramétrica vs. normal de planos de la Semana 01). El espacio de configuraciones $Q$ (el círculo $S^1$ para el péndulo simple, el toro $T^2 = S^1 \times S^1$ para el péndulo doble, la esfera $S^2$ para el péndulo esférico, el grupo de Lie $SO(3)$ para el cuerpo rígido). Atlas y cartas locales.
* **El Principio de José & Saletan (Cap. 2):** *"Velocities do not lie in $Q$"*. Distinción física entre el espacio de posiciones $Q$ y el **fibrado tangente $TQ$** (espacio de estados de Lagrange con coordenadas locales $(q^i, \dot{q}^i)$).
* **Física:** El principio de mínima acción de Hamilton $\delta \int L(q, \dot{q})\, dt = 0$ formulado intrínsecamente sobre curvas en $TQ$.
* **Lectura asignada:** José & Saletan (Cap. 2, Secc. 2.1–2.4), Arnold (Cap. 4, Secc. 17–19), Nakahara (Cap. 5, Secc. 5.1–5.2).

---

## 📋 Estado de Avance y Entregables

| Semana | Tema | Lectura | Slides | Tarea | Estado |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **11** | Integración y Estrella de Hodge ($\star$) | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **12** | Teorema Generalizado de Stokes y Topología II | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **13** | Espacios de Configuración ($Q$) y Fibrado $TQ$ | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
