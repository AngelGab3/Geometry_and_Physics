# MÓDULO 0: El Arsenal de Índices, Rotaciones y Tensores Elementales
**Duración:** Semanas 1 a 3 (Semanas 01 a 03)  
**Objetivo Pedagógico:** Empoderar al alumno que solo cursó cálculo tradicional de una y dos variables con las herramientas operacionales de índices, transformaciones de coordenadas y geometría de grupos continuos. Demostrar en 3 líneas identidades vectoriales que antes tomaban páginas enteras, construir el grupo de rotaciones $SO(2)$ y $SO(3)$ a partir de movimientos rígidos y vectores base, distinguir transformaciones afines (traslaciones) de lineales (rotaciones), y tender el puente hacia las variedades y la métrica euclidiana.

---

## 🔗 Hilo Conductor y Conexión Acumulativa

* **Punto de Partida:** El alumno conoce el producto escalar $\vec{u}\cdot\vec{v}$ y el producto vectorial $\vec{u}\times\vec{v}$ mediante fórmulas de componentes fijas $(x, y, z)$.
* **Lo que construimos en este módulo (Paso a Paso):**
  1. **Semana 01:** La contracción con $\delta_{ij}$ y la antisimetría con $\epsilon_{ijk}$. La identidad $\epsilon-\delta$ como el arma definitiva contra identidades vectoriales kilométricas.
  2. **Semana 02:** El grupo de rotaciones $SO(2)$ y $SO(3)$. Por qué los movimientos rígidos exigen $R^T R = I$, por qué la continuidad de orientación exige $\det R = +1$, el experimento del libro (no-conmutatividad de rotaciones en 3D), y la diferencia fundamental entre traslaciones (espacio afín de puntos) y rotaciones (espacio vectorial tangente).
  3. **Semana 03:** Coordenadas curvilíneas (polares, cilíndricas, esféricas), matrices Jacobianas como la aproximación lineal local, la regla de la cadena multivariable compacta y el tensor métrico $g_{ij}$.
* **Hacia dónde vamos (Conexión con Módulo 1):**
  * La diferencia entre traslaciones (puntos) y rotaciones (vectores) fundamentará la definición intrínseca de **puntos vs. vectores tangentes como derivaciones** en la Semana 4.
  * La delta de Kronecker $\delta^i_j$ se convertirá en la contracción dual covector-vector: $dx^i(\partial_j) = \delta^i_j$.
  * El símbolo antisimétrico $\epsilon_{ijk}$ se transformará en el producto cuña: $(dx \wedge dy)(u, v) = \epsilon_{ij} u^i v^j$.
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

### [Semana 02: El Grupo de Rotaciones $SO(2)$, $SO(3)$ y Traslaciones](Semana_02_Rotaciones_SO2_SO3_Traslaciones/)
* **Pregunta física:** ¿Cómo garantizamos que las leyes de la física no dependan de la orientación de nuestro laboratorio en el espacio? ¿Qué diferencia a un giro de un desplazamiento en línea recta?
* **Construcción Activa del Conocimiento:**
  1. *El reto del cuerpo rígido:* Invarianza del producto punto $\langle R\vec{u}, R\vec{v}\rangle = \langle \vec{u}, \vec{v}\rangle \implies R^T R = I$. El alumno deduce que $R^{-1} = R^T$ sin memorizarlo.
  2. *Construcción columna a columna:* Siguiendo el destino de los vectores base $\hat{i}, \hat{j}, \hat{k}$ al girar un ángulo $\theta$. Deducción geométrica de $R(\theta)$ en 2D y de $R_x, R_y, R_z$ en 3D.
  3. *El experimento del espejo:* $(\det R)^2 = 1 \implies \det R = \pm 1$. Por qué las reflexiones ($\det = -1$) invierten la paridad y por qué una rotación física continua desde $\theta=0$ exige $\det R = +1$.
  4. *El experimento del libro:* Girar un objeto sobre dos ejes perpendiculares en distinto orden. Descubrimiento físico de la **no-conmutatividad**: $R_x(\pi/2) R_z(\pi/2) \neq R_z(\pi/2) R_x(\pi/2)$.
  5. *Rotaciones vs. Traslaciones:* Traslaciones $x \mapsto x+a$ (afines, mueven el origen, actúan sobre **puntos**) vs. Rotaciones $x \mapsto Rx$ (lineales, fijan el origen, actúan sobre **vectores**).
* **Física:** El grupo euclidiano $E(3) = \mathbb{R}^3 \rtimes SO(3)$, transformaciones pasivas vs. activas de sistemas de referencia, y momento de inercia bajo rotaciones.
* **Lectura asignada:** O'Neill (Cap. 3, Secc. 3.1–3.3), Goldstein (*Classical Mechanics*, Cap. 4), Carter (*Visual Group Theory*).

---

### [Semana 03: Matrices Jacobianas, Coordenadas Curvilíneas y el Tensor Métrico](Semana_03_Jacobianas_Curvilineas_Metrica/)
* **Pregunta física:** Si rotar ejes rectos preserva la métrica cartesiana $\delta_{ij}$, ¿qué le ocurre a las distancias y a los vectores cuando usamos coordenadas curvas (polares, cilíndricas, esféricas)?
* **Conceptos clave:** La matriz Jacobiana $J^i{}_a = \frac{\partial x^i}{\partial u^a}$ como la mejor aproximación lineal local. La regla de la cadena multivariable en índices: $\partial_a f = J^i{}_a \partial_i f$.
* **El Determinante como Factor de Escala de Volumen:**
  $$\det(J) = \epsilon_{ijk} J^1{}_i J^2{}_j J^3{}_k$$
* **El Tensor Métrico General $g_{ij}$:** Cómo se deforma el producto punto al cambiar a coordenadas curvas:
  $$ds^2 = g_{ab}\, du^a du^b, \qquad g_{ab} = \frac{\partial x^i}{\partial u^a}\frac{\partial x^j}{\partial u^b} \delta_{ij}$$
  Cálculo explícito para polares ($g_{rr}=1, g_{\theta\theta}=r^2$) y esféricas.
* **Modelo visual:** La matriz Jacobiana transforma pequeños rectángulos coordenados en paralelogramos curvilíneos locales; la métrica mide la distorsión de longitudes y ángulos en cada punto.
* **Física:** Gradiente y aceleración en coordenadas cilíndricas y esféricas sin memorizar tablas de fórmulas; conservación del momento angular en coordenadas polares.
* **Lectura asignada:** Bachman (Cap. 2, Secc. 2.1–2.3; Cap. 4, Secc. 4.6), Kay (Cap. 3), Fortney (Cap. 2).

---

## 📋 Estado de Avance y Entregables

| Semana | Tema | Lectura | Slides | Tarea | Estado |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **01** | Notación de Einstein, $\delta_{ij}$ y Levi-Civita | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | Por iniciar |
| **02** | Rotaciones $SO(2), SO(3)$ y Traslaciones | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **03** | Jacobianas, Coordenadas Curvas y Métrica $g_{ij}$ | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
