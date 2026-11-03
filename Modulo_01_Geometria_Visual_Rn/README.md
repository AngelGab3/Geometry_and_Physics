# MÓDULO 1: La Geometría Visual de las Formas en $\mathbb{R}^n$
**Duración:** Semanas 4 a 6 (Semanas 04 a 06)  
**Objetivo Pedagógico:** Dar el salto natural del cálculo con índices en componentes hacia la geometría diferencial intrínseca sin coordenadas fijas. Construir la intuición física de vectores como operadores de derivación direccional, covectores como familias de láminas de nivel cortadas (Needham, Fortney), y el producto cuña como áreas orientadas de sombras proyectadas (Bachman).

---

## 🔗 Hilo Conductor y Conexión Acumulativa

* **Punto de Partida (Desde Módulo 0):** Dominamos la contracción con $\delta_{ij}$, el tensor métrico $g_{ij}$, el determinante y el símbolo antisimétrico $\epsilon_{ijk}$.
* **Lo que construimos en este módulo:**
  1. Identificación rigurosa de las derivadas parciales $\frac{\partial}{\partial x^i}$ con los vectores tangentes base.
  2. La dualidad: el diferencial $dx^i$ evalúa vectores mediante la delta aprendida en el Módulo 0: $dx^i(\partial_j) = \delta^i_j$.
  3. El producto exterior antisimétrico $\wedge$ como la transcripción geométrica directa del tensor alternante $\epsilon_{ijk}$.
  4. Los isomorfismos musicales ($\flat$ y $\sharp$) que conectan fuerzas (covectores) con velocidades (vectores) a través de $g_{ij}$.
* **Hacia dónde vamos (Conexión con Módulo 2):**
  * Las 1-formas y 2-formas serán diferenciadas por el operador intrínseco de Cartan $d: \Omega^k \to \Omega^{k+1}$.
  * Descubriremos por qué $d^2 = 0$ y cómo la presencia de agujeros topológicos impide que ciertas formas cerradas admitan potencial global (efecto Aharonov-Bohm).

---

## 📚 Desglose de Semanas

### [Semana 04: Puntos, Funciones Coordenadas y Vectores como Derivaciones](Semana_04_Puntos_Coordenadas_Vectores/)
* **Pregunta física:** ¿Por qué no tiene sentido físico sumar dos posiciones en el espacio? ¿Qué diferencia a un lugar de un movimiento o velocidad?
* **Conceptos clave:** Puntos como posiciones fijas vs. vectores anclados $v_p \in T_p\mathbb{R}^n$. Las coordenadas $x, y$ como funciones escalares reales $x: \mathbb{R}^n \to \mathbb{R}$. La derivada direccional vista como la verdadera definición de un vector tangente:
  $$v_p[f] \equiv \left.\frac{d}{dt}f(\gamma(t))\right|_{t=0} = v^i \partial_i f$$
  Identificación de los operadores de derivadas parciales con los vectores base: $e_i \leftrightarrow \left.\frac{\partial}{\partial x^i}\right|_p$.
* **Modelo visual (Fortney Cap. 2 / Bachman Cap. 2):** Espacios tangentes locales $T_p\mathbb{R}^n$ pegados en cada punto; la acción de un vector evaluando la tasa de variación instantánea sobre la gráfica de un campo escalar.
* **Física:** Partículas atravesando campos térmicos $T(x,y)$ o potenciales $V(x,y)$.
* **Lectura asignada:** Fortney (Secc. 2.1–2.3), Bachman (Secc. 3.1).

---

### [Semana 05: Covectores y 1-Formas: Medir sin Métrica e Isomorfismos Musicales](Semana_05_Covectores_1Formas_Laminas/)
* **Pregunta física:** En termodinámica el trabajo es $P\,dV$ sin necesidad de hablar de productos punto ni ángulos. ¿Qué es realmente el trabajo físico?
* **Conceptos clave:** El espacio dual $(T_p\mathbb{R}^n)^*$. Funcionales lineales que comen vectores y producen escalares. La base dual canónica $\{dx^1, \dots, dx^n\}$ definida por la contracción: $dx^i(\partial_j) = \delta^i_j$. El diferencial de una función $df = \partial_i f\, dx^i$ como 1-forma natural.
* **El Puente Musical ($\flat$ y $\sharp$):** La métrica $g_{ij}$ baja y sube índices, conectando vectores con covectores. La verdadera naturaleza del gradiente: $\vec{\nabla}f = (df)^\sharp$.
* **Modelo visual (Needham Cap. 32 / Fortney Cap. 5 / Bachman Secc. 5.7):** Una 1-forma como una **familia de láminas paralelas/curvas de nivel** (*lines-to-be-pierced*). Evaluar $\alpha(v)$ es contar con signo cuántas láminas perfora la flecha $v$. *Por qué NO dibujar una 1-forma como una flecha* (Bachman 5.7).
* **Física:** Fuerza conservativa como láminas equipotenciales; trabajo infinitesimal $\delta W = F_i dx^i$ como conteo de láminas perforadas.
* **Lectura asignada:** Needham (Secc. 32.1–32.3), Fortney (Secc. 2.4 y 5.1), Bachman (Secc. 3.2 y 5.7).

---

### [Semana 06: Álgebra Exterior: El Producto Cuña ($\wedge$) y Áreas Orientadas](Semana_06_Wedge_Areas_Orientadas/)
* **Pregunta física:** ¿Cómo medimos el área encerrada por dos vectores en un plano sin depender de la regla de la mano derecha en 3D?
* **Conceptos clave:** El producto exterior antisimétrico $\alpha \wedge \beta = -\beta \wedge \alpha$. La base de 2-formas en $\mathbb{R}^2$ ($dx \wedge dy$) y en $\mathbb{R}^3$ ($dy \wedge dz, dz \wedge dx, dx \wedge dy$). Relación directa con el símbolo de Levi-Civita $\epsilon_{ijk}$ del Módulo 0.
* **Modelo visual (Bachman Cap. 3 / Fortney Cap. 3 y 5):** 
  * Bachman: $(dx \wedge dy)(u, v)$ es el área orientada de la sombra proyectada por el paralelogramo $(u, v)$ sobre el plano $xy$.
  * Fortney: Dos familias de láminas que se cruzan forman un **panal de tubos/cajitas orientadas**. Evaluar la 2-forma es contar cuántos tubos encierra el paralelogramo.
* **Física:** Densidad de flujo magnético elemental a través de superficies proyectadas.
* **Lectura asignada:** Bachman (Cap. 3, Secc. 3.3–3.7), Fortney (Cap. 3 y Secc. 5.2–5.3).

---

## 📋 Estado de Avance y Entregables

| Semana | Tema | Lectura | Slides | Tarea | Estado |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **04** | Puntos, Coordenadas y Vectores como Derivaciones | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | ✅ Lista (`.pdf`) | Completada |
| **05** | Covectores, 1-Formas e Isomorfismos Musicales | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
| **06** | Álgebra Exterior: El Producto Cuña ($\wedge$) | ⏳ Pendiente | ⏳ Pendiente | ⏳ Pendiente | En cola |
