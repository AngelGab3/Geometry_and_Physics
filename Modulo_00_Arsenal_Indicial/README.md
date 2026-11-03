# MÓDULO 0: El Arsenal de Índices y Tensores Elementales
**Duración:** Semanas 1 a 3 (Semanas 01 a 03)  
**Objetivo Pedagógico:** Empoderar al alumno que solo cursó cálculo tradicional de una y dos variables con las herramientas operacionales de índices y álgebra multilineal elemental. Demostrar en 3 líneas identidades vectoriales que antes tomaban páginas enteras, desmitificar el producto cruz, y sentar las bases algebraicas de la contracción, la antisimetría y el tensor métrico.

---

## 🔗 Hilo Conductor y Conexión Acumulativa

* **Punto de Partida:** El alumno conoce el producto escalar $\vec{u}\cdot\vec{v}$ y el producto vectorial $\vec{u}\times\vec{v}$ mediante fórmulas de determinantes y componentes $(x, y, z)$.
* **Lo que construimos en este módulo:**
  1. La contracción con $\delta_{ij}$ y la antisimetría con $\epsilon_{ijk}$.
  2. Las matrices Jacobianas como la aproximación lineal de cambios de coordenadas y el determinante como volumen orientado.
  3. La descomposición simétrico/antisimétrico y la noción de métrica euclidiana $g_{ij}$.
* **Hacia dónde vamos (Conexión con Módulo 1):**
  * La delta de Kronecker $\delta^i_j$ será la definición de dualidad entre covectores y vectores: $dx^i(\partial_j) = \delta^i_j$.
  * El símbolo antisimétrico $\epsilon_{ijk}$ se convertirá en el producto cuña: $(dx \wedge dy)(u, v) = \epsilon_{ij} u^i v^j$.
  * El tensor métrico $g_{ij}$ construirá los isomorfismos musicales ($\flat$ y $\sharp$) para conectar fuerzas con velocidades.

---

## 📚 Desglose de Semanas

### [Semana 01: Notación de Einstein, Delta de Kronecker y Símbolo de Levi-Civita](Semana_01_Einstein_Kronecker_LeviCivita/)
* **Pregunta física:** ¿Cómo podemos simplificar cálculos de vectores y campos en 3D sin escribir matrices gigantes ni llenar páginas de componentes?
* **Conceptos clave:** Convenio de suma de Einstein (índices mudos y libres). La delta de Kronecker $\delta_{ij}$ como operador de sustitución/identidad. El símbolo de permutación totalmente antisimétrico de Levi-Civita $\epsilon_{ijk}$ en $\mathbb{R}^3$.
* **La Identidad Maestra $\epsilon-\delta$:**
  $$\epsilon_{ijk}\epsilon_{imn} = \delta_{jm}\delta_{kn} - \delta_{jn}\delta_{km}$$
* **Demolición en 3 líneas:** Demostración elegante y rigurosa de la identidad del triple producto vectorial:
  $$\vec{A} \times (\vec{B} \times \vec{C}) = \vec{B}(\vec{A}\cdot\vec{C}) - \vec{C}(\vec{A}\cdot\vec{B})$$
* **Modelo visual:** Permutaciones pares e impares vistas como giros en un círculo cíclico $(1 \to 2 \to 3 \to 1)$.
* **Física:** Momento angular $\vec{L} = \vec{r}\times\vec{p}$ en componentes $L_i = \epsilon_{ijk} x_j p_k$; fuerza magnética de Lorentz $\vec{F} = q(\vec{v}\times\vec{B})$.
* **Lectura asignada:** Kay (*Cálculo Tensorial*, Caps. 1 y 2), Arfken (*Mathematical Methods for Physicists*, Cap. 3).

---

### [Semana 02: Regla de la Cadena, Matrices Jacobianas y Volúmenes Orientados](Semana_02_Jacobianas_Determinantes_ReglaCadena/)
* **Pregunta física:** Cuando cambiamos de coordenadas cartesianas a polares o esféricas, ¿por qué aparece un factor multiplicativo ($r$ o $r^2\sin\theta$) y qué representa geométricamente?
* **Conceptos clave:** El operador gradiente en índices $\partial_i \equiv \frac{\partial}{\partial x^i}$. La regla de la cadena multivariable compacta: $\frac{\partial f}{\partial u^a} = \frac{\partial x^i}{\partial u^a}\partial_i f$. La matriz Jacobiana $J^i{}_a = \frac{\partial x^i}{\partial u^a}$ como la mejor aproximación lineal local.
* **El Determinante como Volumen Orientado:** Definición tensorial del determinante mediante $\epsilon_{ijk}$:
  $$\det(A) = \epsilon_{ijk} A_{1i} A_{2j} A_{3k}$$
* **Modelo visual (Bachman Cap. 2 y 4):** La matriz Jacobiana mapea un rectángulo o cubito infinitesimal en un paralelogramo o paralelepípedo inclinado; el determinante mide el factor de dilatación y la preservación o inversión de la orientación.
* **Física:** Conservación de la masa en mecánica de fluidos locales; transformaciones de coordenadas en cinemática (polares, cilíndricas, esféricas).
* **Lectura asignada:** Bachman (Cap. 2, Secc. 2.1–2.3; Cap. 4, Secc. 4.6), Fortney (Cap. 2).

---

### [Semana 03: Simetría, Antisimetría, Tensores y la Métrica Euclidiana](Semana_03_Simetria_Metrica_Diferenciales/)
* **Pregunta física:** ¿Por qué en termodinámica el trabajo infinitesimal $\delta W$ no es el diferencial de una función de estado, a diferencia de la energía interna $dU$?
* **Conceptos clave:** Descomposición de cualquier tensor de rango 2 en parte simétrica y antisimétrica: $T_{ij} = S_{ij} + A_{ij}$. Anulación de la contracción simétrico-antisimétrico: $S_{ij} A^{ij} = 0$.
* **El Tensor Métrico $g_{ij}$:** El producto punto como tensor simétrico covariante $g_{ij} = \delta_{ij}$ en cartesianas. Cómo se transforma la métrica bajo cambios de coordenadas: $g'_{ab} = \frac{\partial x^i}{\partial u^a}\frac{\partial x^j}{\partial u^b} g_{ij}$.
* **Diferenciales exactas vs. inexactas:** El criterio de integrabilidad de derivadas cruzadas de Schwarz ($\partial_i V_j = \partial_j V_i$) para campos conservativos.
* **Modelo visual:** La métrica como una elipse o círculo unitario en cada punto del espacio midiendo distancias y ángulos locales.
* **Física:** Tensor de inercia $I_{ij} = \int \rho (r^2\delta_{ij} - x_i x_j) dV$; tensor de esfuerzos en medios continuos.
* **Lectura asignada:** Kay (Cap. 3), Riley & Hobson (Cap. 26), O'Neill (Cap. 1, Secc. 1.2).

---

## 📋 Estado de Avance y Entregables

| Semana | Tema | Lectura | Slides | Tarea | Estado |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **01** | Notación de Einstein, $\delta_{ij}$ y Levi-Civita | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | Por iniciar |
| **02** | Jacobianas, Regla de la Cadena y Determinantes | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **03** | Simetría, Métrica Euclidiana y Diferenciales | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
