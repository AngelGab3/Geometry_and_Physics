# MÓDULO 0: Geometría Euclidiana, Arsenal de Índices, Rotaciones y Tensores Elementales
**Duración:** Semanas 1 a 4 (Semanas 01 a 04)  
**Objetivo Pedagógico:** Nivelar y empoderar a los estudiantes de **Física e Ingeniería** que solo han cursado cálculo tradicional de una y dos variables. Construimos desde la geometría más intuitiva de vectores, proyecciones, rectas y planos en $\mathbb{R}^3$, pasando por el arsenal de índices de Einstein y Levi-Civita, el grupo de rotaciones $SO(2)$ y $SO(3)$ (incluyendo el eje de rotación, rotaciones infinitesimales y diferencias con traslaciones), hasta las matrices Jacobianas y el tensor métrico $g_{ij}$.

---

## 🔗 Hilo Conductor y Conexión Acumulativa («La Necesidad Crea la Herramienta»)

* **Punto de Partida:** El estudiante de física o ingeniería conoce coordenadas cartesianas $(x, y, z)$, el Teorema de Pitágoras y derivadas parciales básicas.
* **Lo que construimos en este módulo (Paso a Paso):**
  1. **Semana 01 (Geometría de Vectores, Rectas y Planos):** Distinguimos físicamente **puntos** (ubicaciones) de **vectores** (desplazamientos invariantes ante traslaciones). Construimos la suma y resta mediante las dos diagonales del paralelogramo, la recta paramétrica $\vec{r}(t) = \vec{p}_0 + t\vec{v}$, el producto punto desde la Ley de Cosenos como máquina de proyecciones ortogonales, el producto cruz como área orientada, y las **dos caras duales del plano** ($\vec{r}(u,v) = \vec{p}_0 + u\vec{v}_1 + v\vec{v}_2$ vs. $\vec{n}\cdot(\vec{r}-\vec{p}_0)=0$), sembrando la semilla visual de las variedades y de las **1-formas como pilas de planos paralelos**.
  2. **Semana 02 (El Arsenal de Índices y Determinantes):** Ante la explosión algebraica de operar con componentes en 3D, construimos el convenio de Einstein, la delta de Kronecker $\delta_{ij} \equiv \hat{e}_i\cdot\hat{e}_j$, el símbolo de Levi-Civita $\epsilon_{ijk} \equiv \hat{e}_i\cdot(\hat{e}_j\times\hat{e}_k)$ como volumen con signo, la identidad $\epsilon-\delta$ por conteo de casos y el determinante $\epsilon_{ijk}M_{ia}M_{jb}M_{kc} = \det(M)\epsilon_{abc}$ como factor de escala de volumen.
  3. **Semana 03 (El Grupo de Rotaciones $SO(2), SO(3)$ y Traslaciones):** Construimos las matrices de rotación exigiendo rigidez ($\langle R\vec{u}, R\vec{v}\rangle = \langle \vec{u}, \vec{v}\rangle \implies R^T R = I$) y preservación de orientación frente a espejos ($\det R = +1$). Exploramos la no-conmutatividad en 3D, el Teorema de Euler del eje de rotación ($R\vec{v} = \vec{v}$), las rotaciones infinitesimales $R \approx I + \Omega\,dt$ ($\Omega^T = -\Omega \implies \vec{v} = \vec{\omega}\times\vec{r}$), y la diferencia estructural entre traslaciones afines y rotaciones lineales.
  4. **Semana 04 (Matrices Jacobianas, Coordenadas Curvas y Métrica $g_{ij}$):** Estudiamos cómo se deforman los vectores y las distancias en coordenadas polares, cilíndricas y esféricas mediante la matriz Jacobiana $J^i{}_a = \frac{\partial x^i}{\partial u^a}$ y el tensor métrico $g_{ab}$, distinguiendo diferenciales exactos ($df$) de inexactos ($\delta W$).

---

## 📚 Desglose de Semanas

### [Semana 01: Geometría del Espacio Euclidiano: Vectores, Proyecciones, Rectas y Planos](Semana_01_Geometria_Vectores_Rectas_Planos/)
* **Pregunta física y de ingeniería:** ¿Por qué no podemos «sumar ubicaciones» en un puente, cómo calculamos la fuerza que acelera un vagón sobre un riel sin medir ángulos, y por qué un plano en $\mathbb{R}^3$ puede describirse tanto con $2$ parámetros libres como con $1$ sola ecuación normal?
* **Construcción Activa del Conocimiento:**
  1. *Puntos vs. Vectores:* Invariancia de $\vec{v} = P_1 - P_0$ al mover el origen. Las dos diagonales del paralelogramo ($\vec{u}+\vec{v}$ y $\vec{u}-\vec{v}$).
  2. *Ecuación Paramétrica de la Recta:* $\vec{r}(t) = \vec{p}_0 + t\vec{v}$ ($1$ grado de libertad) y la velocidad $\dot{\vec{r}} = \vec{v}$ como semilla del vector tangente.
  3. *Producto Punto y Proyección Ortogonal:* Deducción desde la Ley de Cosenos. Descomposición $\vec{u} = \vec{u}_\parallel + \vec{u}_\perp$ sobre un riel y trabajo mecánico.
  4. *Producto Cruz y Orientación:* Deducción desde el sistema $\vec{u}\cdot\vec{n}=0, \vec{v}\cdot\vec{n}=0$. Área del paralelogramo y torca $\vec{\tau} = \vec{r}\times\vec{F}$.
  5. *Dualidad del Plano y Semilla de las 1-Formas:* Visión paramétrica $\vec{r}(u,v) = \vec{p}_0 + u\vec{v}_1 + v\vec{v}_2$ (semilla de variedades) vs. visión normal $\vec{n}\cdot(\vec{r}-\vec{p}_0)=0$. La familia de planos paralelos $n_1 x + n_2 y + n_3 z = c$ perforados por un vector $\vec{w}$ como **imagen exacta de una 1-forma de Cartan**.
  6. *Distancia Punto-Plano e Intersección de Planos:* $D(Q,\Pi) = \frac{|\vec{n}\cdot(\vec{q}-\vec{p}_0)|}{\|\vec{n}\|}$ y recta de intersección $\Pi_1 \cap \Pi_2$ con dirección $\vec{v} = \vec{n}_1 \times \vec{n}_2$ (semilla de las 2-formas).

---

### [Semana 02: El Arsenal de Índices: Notación de Einstein, $\delta_{ij}$, Levi-Civita y Determinantes](Semana_02_Einstein_Kronecker_LeviCivita/)
* **Pregunta física:** ¿Cómo podemos simplificar cálculos de vectores, áreas y volúmenes en 3D sin escribir matrices gigantes ni llenar páginas de componentes?
* **Construcción Activa del Conocimiento:**
  1. *Dolor Cartesiano y Proyección sobre la Base:* $\delta_{ij} \equiv \hat{e}_i\cdot\hat{e}_j$ como interruptor selector y convenio de suma de Einstein.
  2. *Construcción Geométrica de Levi-Civita:* $\epsilon_{ijk} \equiv \hat{e}_i\cdot(\hat{e}_j\times\hat{e}_k)$ como volumen orientado de la base ortonormal.
  3. *La Identidad Maestra $\epsilon-\delta$:* Deducción constructiva por conteo de casos de $\epsilon_{ijk}\epsilon_{imn} = \delta_{jm}\delta_{kn} - \delta_{jn}\delta_{km}$ y demolición de $\vec{A}\times(\vec{B}\times\vec{C})$ y identidades de rotacional/divergencia.
  4. *El Determinante como Volumen Orientado:* Construcción de $\epsilon_{ijk} M_{ia} M_{jb} M_{kc} = \det(M)\epsilon_{abc}$ preparando la condición $\det R = +1$ de la Semana 03.

---

### [Semana 03: El Grupo de Rotaciones $SO(2)$, $SO(3)$ y Traslaciones](Semana_03_Rotaciones_SO2_SO3_Traslaciones/)
* **Pregunta física:** ¿Cómo garantizamos que una transformación mueva un cuerpo rígido sin deformarlo ni reflejarlo en un espejo, por qué los giros en 3D no conmutan, y qué es la velocidad angular $\vec{\omega}$?
* **Construcción Activa del Conocimiento:**
  1. *Condición de Rigidez:* $\langle R\vec{u}, R\vec{v}\rangle = \langle \vec{u}, \vec{v}\rangle \implies R^T R = I$ ($R^{-1} = R^T$).
  2. *Construcción Columna a Columna:* Destino de los vectores base $\hat{e}_1, \hat{e}_2, \hat{e}_3$ para obtener $R(\theta)$ en 2D y $R_x, R_y, R_z$ en 3D.
  3. *Experimento del Espejo y del Libro:* $\det R = +1$ (rotaciones propias vs. reflexiones impropias $\det R = -1$) y no-conmutatividad de $SO(3)$.
  4. *Eje de Rotación y Rotaciones Infinitesimales:* El eje de giro como vector propio $R\vec{v} = \vec{v}$ (Teorema de Euler) y matrices antisimétricas $\Omega^T = -\Omega$ como generadores de $\vec{v} = \vec{\omega}\times\vec{r}$.
  5. *Traslaciones vs. Rotaciones:* Transformaciones afines sobre puntos vs. transformaciones lineales sobre vectores.

---

### [Semana 04: Matrices Jacobianas, Coordenadas Curvilíneas y el Tensor Métrico](Semana_04_Jacobianas_Curvilineas_Metrica/)
* **Pregunta física:** ¿Cómo medimos longitudes, áreas, volúmenes y gradientes cuando la simetría del problema exige coordenadas polares, cilíndricas o esféricas?
* **Conceptos clave:** Matriz Jacobiana $J^i{}_a = \frac{\partial x^i}{\partial u^a}$, factor de escala de área y volumen $|\det J|$, tensor métrico $g_{ab} = J^i{}_a J^j{}_b \delta_{ij}$ ($ds^2 = g_{ab}\,du^a du^b$), bases locales adaptadas vs. normalizadas, y diferenciales exactos $df$ vs. inexactos $\delta W$.

---

## 📋 Estado de Avance y Entregables

| Semana | Tema | Lectura | Slides | Tarea | Estado |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **01** | Geometría de Vectores, Proyecciones, Rectas y Planos | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | Completada |
| **02** | Notación de Einstein, $\delta_{ij}$, Levi-Civita y Determinantes | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | Completada |
| **03** | El Grupo de Rotaciones $SO(2), SO(3)$ y Traslaciones | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | Completada |
| **04** | Matrices Jacobianas, Coordenadas Curvas y Métrica $g_{ij}$ | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | Completada |
