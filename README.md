# Apuntes-de-Clase-Unidad-1
Unidad I. Introducción a la graficación por computadora

# 1.1 Historia y evolución de la graficación por computadora

La graficación por computadora ha evolucionado desde representaciones simples de líneas hasta entornos tridimensionales fotorrealistas en tiempo real.

Años 50: El inicio se marca con el proyecto Whirlwind del MIT y el sistema SAGE de la Fuerza Aérea de EE. UU., que utilizaban tubos de rayos catódicos (CRT) para mostrar datos de radar como puntos y líneas.

Años 60: Ivan Sutherland desarrolló Sketchpad (1963), el primer sistema interactivo que usaba un lápiz óptico para dibujar vectores en una pantalla, sentando las bases del Diseño Asistido por Computadora (CAD).

Años 70: Surgieron los algoritmos de sombreado (Gouraud y Phong) y el concepto de Z-buffer para la determinación de superficies ocultas. Se establecieron las bases de los gráficos rasterizados.

Años 80 y 90: La llegada de las interfaces gráficas de usuario (GUI) y estándares como OpenGL y DirectX democratizaron los gráficos. La industria del cine (ej. Toy Story en 1995) impulsó el renderizado 3D comercial.

Actualidad: Las Unidades de Procesamiento Gráfico (GPU) modernas permiten técnicas de Ray Tracing (trazado de rayos) en tiempo real y el uso de inteligencia artificial para la generación y escalado de imágenes (ej. DLSS).

# 1.2 Áreas de aplicación

La graficación es transversal a múltiples disciplinas:

Simulación y Entrenamiento: Simuladores de vuelo, conducción y entornos médicos de Realidad Virtual (VR).

Diseño Asistido por Computadora (CAD): Arquitectura, diseño automotriz y modelado de piezas industriales.

Entretenimiento: Videojuegos, efectos visuales (VFX) en cine y animación 3D.

Visualización Científica y de Datos: Representación de funciones matemáticas, fluidos, estructuras moleculares y análisis de Big Data.

Interfaces de Usuario (UI): Entornos de escritorio, aplicaciones móviles y diseño web interactivo.

# 1.3 Aspectos matemáticos de la graficación

El motor detrás de la graficación por computadora es el álgebra lineal y la geometría analítica. Los objetos se definen en sistemas de coordenadas y se manipulan mediante transformaciones afines usando matrices.

Para representar gráficos bidimensionales con la capacidad de trasladar, rotar y escalar uniformemente, se utilizan coordenadas homogéneas, que permiten expresar todas las transformaciones mediante la multiplicación de matrices de $3 \times 3$.Por ejemplo, la matriz para una traslación bidimensional por un vector $(t_x, t_y)$ es:

<img width="255" height="114" alt="image" src="https://github.com/user-attachments/assets/8519ddc7-671b-41f9-a4cc-10d54a692402" />

Y la matriz para una rotación alrededor del origen por un ángulo $\theta$ es:

<img width="307" height="125" alt="image" src="https://github.com/user-attachments/assets/f2c84b9a-7613-4db1-b202-5f624354d5ca" />

En entornos 3D, estos conceptos se expanden a matrices de $4 \times 4$, incluyendo proyecciones ortogonales y de perspectiva para proyectar volúmenes en pantallas 2D.

# 1.4 Modelos del color: RGB, CMY, HSV y HSL

Los modelos de color son representaciones matemáticas que describen cómo se construyen los colores a partir de componentes básicos.

RGB (Red, Green, Blue): Modelo aditivo usado en pantallas (monitores, teléfonos). La suma de los tres colores al máximo nivel produce luz blanca.

CMY/CMYK (Cyan, Magenta, Yellow, Key/Black): Modelo sustractivo usado en impresión. La mezcla de tintas absorbe la luz. La "K" se añade porque la mezcla perfecta de CMY rara vez produce un negro puro en la impresión física.

HSV (Hue, Saturation, Value): Define el color por su Tono (matiz), Saturación (pureza) y Valor (brillo). Es más intuitivo para la percepción humana.

HSL (Hue, Saturation, Lightness): Similar al HSV, pero el eje de luminosidad va desde el negro (0%) hasta el blanco (100%), dejando el color puro en el 50%.

Tutorial: Iluminación de un cubo y sus caras en Blender

Para comprender cómo la luz interactúa con los modelos (afectando la percepción del color y el volumen), sigue estos pasos prácticos:

Preparación del entorno: Abre Blender. Por defecto, aparecerá un cubo en el centro del espacio de trabajo.
<img width="1919" height="1137" alt="image" src="https://github.com/user-attachments/assets/c1037b19-362a-4c64-959a-0d355e2dc04c" />

Cambiar la vista: Presiona la tecla Z y selecciona "Rendered" (Renderizado). Esto te permitirá ver la luz en tiempo real.
<img width="1919" height="1137" alt="image" src="https://github.com/user-attachments/assets/59967ab6-f112-4503-b41f-1134190c981f" />

Añadir iluminación: Presiona Shift + A, ve a la categoría "Light" y selecciona "Point" (Punto de luz).
<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/a0bf1552-7ac3-4236-8b43-e0ecd4de7257" />

Posicionamiento: Usa la herramienta de movimiento (tecla G) para acercar la luz a una de las esquinas superiores del cubo. Verás cómo las caras más cercanas se iluminan y las opuestas proyectan sombra.
<img width="1914" height="1143" alt="image" src="https://github.com/user-attachments/assets/88b76483-f035-40e7-b13c-660ae606f2c4" />

Propiedades de la luz: Con la luz seleccionada, ve al panel de propiedades (lado derecho), haz clic en el ícono del foco verde. Cambia el "Power" (Poder) a 1000 W y modifica el "Color" a un tono azul o rojo (usando la rueda de color RGB/HSV) para observar cómo rebota la luz en el material gris por defecto.
<img width="1919" height="1139" alt="image" src="https://github.com/user-attachments/assets/703f1208-ab99-48a2-a4e9-7dc47ebc36e4" />

Iluminación de caras específicas (Spot): Para iluminar solo una cara, cambia el tipo de luz en ese mismo panel de Point a "Spot". Usa la herramienta de rotación (tecla R) para apuntar el cono de luz directamente a la cara frontal del cubo.
<img width="1918" height="1138" alt="image" src="https://github.com/user-attachments/assets/99043b90-cedc-480e-878b-4de5eb0fea53" />

# 1.5 Representación y trazo de líneas y polígonos

A nivel de hardware, una pantalla es una cuadrícula de píxeles. Trazar una línea continua implica determinar qué píxeles discretos deben encenderse para aproximar mejor esa trayectoria (rasterización). Esto se logra mediante algoritmos como el DDA (Analizador Diferencial Digital) y el Algoritmo de Bresenham (que utiliza solo aritmética entera para mayor velocidad).

Los polígonos se representan como secuencias de vértices conectados por aristas (líneas). El relleno de estos polígonos requiere algoritmos de "escaneo de líneas" (scan-line), que determinan qué píxeles se encuentran dentro de los límites matemáticos de la figura.

# 1.5.1 Formatos de imagen

Imágenes Rasterizadas (Mapas de bits): Arreglos rectangulares de píxeles. Ejemplos: JPEG (compresión con pérdida), PNG (compresión sin pérdida con transparencia), GIF y BMP. No escalan bien sin perder calidad (pixelación).

Imágenes Vectoriales: Basadas en fórmulas matemáticas y geometría (líneas, curvas, polígonos). Ejemplos: SVG, EPS y PDF. Son infinitamente escalables sin perder resolución.

# Práctica delpolígono
<img width="1919" height="1135" alt="image" src="https://github.com/user-attachments/assets/bc8bbe15-b731-4040-9b91-f5739ea0219c" />

# Práctica flor de vida
<img width="1919" height="1142" alt="image" src="https://github.com/user-attachments/assets/758549b8-60af-49c4-98aa-7898ae0c0700" />

# 1.6 Procesamiento de mapas de bits

El procesamiento de mapas de bits (o procesamiento digital de imágenes) consiste en aplicar operaciones matemáticas o algorítmicas directamente sobre los valores numéricos de los píxeles de una imagen rasterizada.

Se divide principalmente en dos tipos de operaciones:

Operaciones de Punto: Alteran un píxel dependiendo únicamente de su valor original (por ejemplo, alterar el brillo o el contraste, o invertir colores mediante operaciones lógicas).

Operaciones de Vecindad (Filtros Espaciales): Alteran un píxel basándose en los valores de los píxeles adyacentes. Esto se logra mediante un proceso matemático llamado convolución, utilizando una matriz pequeña llamada "kernel". Se usa para desenfoque (Blur), detección de bordes o enfoque.
# Referencias Bibliográficas
Hearn, D. y Baker, M. P. (2006). Gráficas por computadora con OpenGL (3.ª ed.). Pearson Educación.

Universidad de Sevilla. (s.f.). Tema 1: Introducción a las Imágenes Digitales. Departamento de Ciencias de la Computación e Inteligencia Artificial. Recuperado de https://asignatura.us.es/imagendigital/Tema1.pdf

Mozilla (MDN Web Docs). (2023). Gráficos en la web. Recuperado de https://developer.mozilla.org/es/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML
