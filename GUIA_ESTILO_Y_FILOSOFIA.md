# Guía de Filosofía Pedagógica, Estándar Editorial y Guía de Estilo

**Curso:** Geometría y Física I: Mecánica Clásica y Formas de Cartan  
**Nivel:** Licenciatura en Física y Matemáticas  
**Repositorio:** `Geometry_and_Physics` (Rama: `main`)  

Este documento condensa los principios pedagógicos, conceptuales, técnicos y estéticos obligatorios para el desarrollo, refinamiento y mantenimiento de todo el material del curso (Notas de Estudio/Lecturas, Diapositivas Beamer y Tareas Semanales).

---

## 1. Filosofía Pedagógica: El «Motor Invisible»

1. **Constructivismo Subterráneo (No Declarativo):**
   - El aprendizaje constructivista es el motor interno que guía la secuencia de deducciones, preguntas y problemas, pero **nunca se nombra explícitamente**.
   - **Prohibición estricta de meta-etiquetas pedagógicas y de entrenamiento docente:**
     - ❌ **Prohibido:** *"Reto en clase (8 minutos)"*, *"Actividad 1"*, *"Discusión 2"*, *"Pregunta de consolidación"*, *"Preguntas de arranque"*, *"Cuestiones conceptuales"*, *"Preguntas de análisis"*, *"Balance conceptual"*, *"Para reflexionar en equipo"*.
   - **Títulos 100% Disciplinares:**
     - Todos los títulos de diapositivas y secciones deben ser puramente matemáticos, geométricos o físicos (e.g., *La Geometría de la Rigidez y la Condición $R^T R = I$*, *Invarianza Geométrica bajo Transformaciones Lineales*, *Axiomas de Grupo y el Grupo Ortogonal $O(n)$*).

2. **Diseño de Diapositivas de Preguntas y Recuperación Activa (Canvas Limpio):**
   - Las preguntas para el estudiante se presentan en **diapositivas dedicadas exclusivas**, directamente sobre el lienzo de la diapositiva con `\begin{enumerate}\itemsep14pt ... \end{enumerate}`.
   - **Sin cajas artificiales:** No encapsular las preguntas dentro de `alertblock`, `exampleblock` o `block` con títulos pedagógicos.
   - **Estructura fija en cada clase (Slides):**
     - **Slide 2 (Preguntas de Apertura / Retrieval Practice):** Preguntas dirigidas a recordar activamente definiciones formales de clases anteriores y pasos o trucos algebraicos cruciales empleados en demostraciones previas (e.g. propiedades del producto interno, anulación de índices, condiciones de ortogonalidad).
     - **Slides intermedias (Pares de Trabajo Activo y Deducción Guiada):**
       - **Slide A (Instrucciones de Trabajo Activo / Experimento en Cuaderno):** Título 100% disciplinar. Plantea un cálculo concreto, verificación analítica o manipulación indicial con instrucciones explícitas para que el estudiante tome lápiz y papel y experimente antes de recibir el resultado formal.
       - **Slide B (Resolución y Discusión Estructural):** Presenta el desarrollo riguroso, señala errores comunes de cálculo y discute el significado geométrico y físico del resultado obtenido.
     - **Última Slide (Preguntas de Cierre / Auditoría Mental):** Invita al alumno a recordar y reconstruir lo realizado durante esa misma sesión: pasos críticos de las demostraciones, trucos algebraicos desbloqueantes y síntesis conceptual.

3. **Cero Referencias hacia el Futuro (No Spoilers):**
   - Cada semana es conceptualmente autosuficiente y se apoya exclusivamente en lo construido hasta ese momento o en la intuición geométrica previa.
   - ❌ **Prohibido:** Afirmaciones como *"como veremos en la semana 5"*, *"esto se comprenderá cuando estudiemos el tensor métrico"*, o *"más adelante en Cartan"*.

4. **Universalidad y Cero Etiquetas Profesionales:**
   - No clasificar a los estudiantes ni justificar temas según perfiles profesionales (❌ *"esto es útil para los ingenieros"*, *"un físico hace esto"*). El lenguaje es riguroso, formativo y de primer nivel para ciencias físico-matemáticas.

---

## 2. Estándar de Formato: Presentaciones (Beamer)

* **Preámbulo y Paquetes:**
  - Uso obligatorio de `\usepackage{../../Common/course_slides}` y `\usepackage{../../Common/course_macros}`.
  - Relación de aspecto panorámica `[aspectratio=169]` en tamaño `10pt`.
* **Cero Desbordamientos Verticales (`Overfull \vbox`):**
  - Cada diapositiva debe compilar con **0 advertencias de `Overfull \vbox`**. Si el contenido excede el alto del frame, debe modularse el interlineado (`\itemsep2pt` o `\itemsep3pt`), compactarse ecuaciones o dividirse temáticamente en dos diapositivas consecutivas.
* **Integridad Tipográfica y Compatibilidad TeX Live:**
  - En Beamer, nunca colocar acentos directos en letras griegas para vectores (e.g., evitar `\vec{\varepsilon}`); usar siempre `\vec{e}` o matrices explícitas para evitar fallos de renderizado de fuentes matemáticas.
* **Inspección Visual de Diagramas TikZ:**
  - Los diagramas TikZ deben ser claros, limpios y estilizados con la paleta del curso (`orangeacc`, `navyaccent`, `blackmain`, `creambg`).
  - Las etiquetas de vectores, puntos y curvas deben estar adecuadamente desplazadas para garantizar que **no exista solapamiento visual**.
* **Compilación Doble:**
  - Siempre compilar dos veces consecutivas con `pdflatex` para que la numeración total de diapositivas (`\inserttotalframenumber`) se resuelva de forma exacta.

---

## 3. Estándar de Formato: Lecturas y Tareas (Notas de Estudio)

* **Preámbulo y Paquetes:**
  - Uso obligatorio de `\usepackage{../../Common/course_notes}` y `\usepackage{../../Common/course_macros}`.
  - Clase `article` en tamaño `11pt, letterpaper`.

* **Encabezado Minimalista y Centrado (Página 1):**
  - En la primera página de toda lectura o tarea, **no debe aparecer el encabezado dinámico superior ni la barra de `fancyhdr`**. Se suprime automáticamente mediante `\thispagestyle{plain}` dentro de los comandos estándar.
  - **Uso obligatorio de macros oficiales de `course_notes.sty`:**
    - Para **Lecturas:**
      ```latex
      \lectureheader{MÓDULO XX}{SEMANA XX}{Título Principal de la Lectura}{Subtítulo temático conceptual}
      ```
    - Para **Tareas:**
      ```latex
      \assignmentheader{MÓDULO XX}{SEMANA XX}{Título de la Tarea Semanal}
      ```
  - **Estructura del bloque de título generado:**
    1. Metadatos discretos en sans-serif: `GEOMETRÍA Y FÍSICA I · MÓDULO XX · SEMANA XX`.
    2. Título principal en `\LARGE\bfseries\color{blackmain}`.
    3. Subtítulo elegante en `\large\color{graymuted}`.
    4. Barra horizontal estructural `\rule{\linewidth}{0.8pt}` en `orangeacc`.

* **Encabezados Dinámicos (Páginas 2 en adelante):**
  - Barra superior en `orangeacc` de `0.8pt`.
  - Izquierda: `Geometría y Física I`.
  - Derecha: Sección temática actual `\nouppercase{\rightmark}`.
  - Pie de página: Número de página centrado en `graymuted`.

* **Cajas de Contenido en Lecturas:**
  - `intuitionbox`: Para motivaciones geométricas, heurísticas físicas y contrastes conceptuales.
  - `infobox`: Para definiciones formales y propiedades estructurales.
  - `examplebox`: Para cálculos explícitos y ejemplos ilustrativos resueltos.
  - `theorembox`: Para enunciados formales, lemas y teoremas.

---

## 4. Estructura de Directorios del Curso

```text
Geometry_and_Physics/
├── Common/
│   ├── course_macros.sty      # Macros matemáticos universales (notación indicial, operadores, etc.)
│   ├── course_notes.sty       # Estilo tipográfico para lecturas y tareas (article)
│   └── course_slides.sty      # Tema y plantilla para presentaciones (beamer)
├── Modulo_00_Arsenal_Indicial/
│   ├── Semana_01_Geometria_Vectores_Rectas_Planos/
│   │   ├── Lectura_01.tex / .pdf
│   │   ├── Slides_01.tex  / .pdf
│   │   └── Tarea_01.tex   / .pdf
│   ├── Semana_02_Einstein_Kronecker_LeviCivita/
│   ├── Semana_03_Rotaciones_SO2_SO3_Traslaciones/
│   └── Semana_04_Jacobianas_Curvilineas_Metrica/
├── Modulo_01_Geometria_Visual_Rn/
│   └── Semana_05_Puntos_Coordenadas_Vectores/
└── GUIA_ESTILO_Y_FILOSOFIA.md  # Este archivo normativo
```

---

## 5. Protocolo de Trabajo en Nuevas Conversaciones

Al iniciar una nueva sesión para refinar o generar una semana:
1. **Comando de Arranque:** El usuario o el agente debe indicar *"Lee `GUIA_ESTILO_Y_FILOSOFIA.md` y procedamos con..."*.
2. **Refinamiento Contenido:** Revisar `Lectura_XX.tex`, `Slides_XX.tex` y `Tarea_XX.tex` aplicando estrictamente los principios de este documento.
3. **Verificación de Compilación:** Compilar con `pdflatex`, verificar 0 overfull boxes y revisar visualmente las páginas generadas.
4. **Higiene de Archivos:** Eliminar siempre archivos auxiliares (`rm -f *.aux *.log *.nav *.out *.snm *.toc`).
5. **Control de Versiones:** Hacer `git add`, `git commit` descriptivo y `git push origin main`.
