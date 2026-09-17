# 🎨 Moviola Editor — WebGPU & Canvas Pro Edition

[![Demo en Vivo](https://img.shields.io/badge/Demo_Online-moviola.fenix.ninja-1473e6?style=for-the-badge&logo=googlechrome&logoColor=white)](https://moviola.fenix.ninja)
[![Autor](https://img.shields.io/badge/Autor-fenix.ninja-ff2453?style=for-the-badge)](https://fenix.ninja)
[![Dependencias](https://img.shields.io/badge/Dependencias-0_(Vanilla_JS)-success?style=for-the-badge)](#arquitectura-técnica)
[![Herramientas](https://img.shields.io/badge/Herramientas-66_Profesionales-blueviolet?style=for-the-badge)](#catálogo-de-herramientas)
[![Internacionalización](https://img.shields.io/badge/i18n-7_Idiomas-orange?style=for-the-badge)](#soporte-multilingüe-i18n)

> **Moviola Editor** es un editor gráfico y fotográfico profesional de nivel escritorio ejecutado directamente en el navegador web. Desarrollado con tecnologías web puras (**HTML5, Canvas 2D, CSS3 y JavaScript moderno ES6+**), sin ninguna dependencia externa de npm ni frameworks pesados, alcanzando un rendimiento fluido de 60 FPS con composición multicapa no destructiva en tiempo real.

---

## 🌐 Probar Demo en Vivo

Puedes probar la versión completa y funcional de Moviola directamente en tu navegador sin instalar nada:

👉 **[https://moviola.fenix.ninja](https://moviola.fenix.ninja)** 👈

---

## ℹ️ Acerca de esta Versión (About This Build)

Creado por el autor **[Fénix Ríos (https://fenix.ninja)](https://fenix.ninja)**, este avanzado editor de fotos y gráficos basado en **WebGPU y Canvas 2D** fue concebido y desarrollado para demostrar habilidades de programación de alto nivel, una arquitectura moderna de software interactivo y la capacidad de trasladar herramientas complejas de escritorio directamente a la plataforma web estándar.

### Filosofía y Capacidades Clave del Software

1. **Cero Dependencias Externas (`Zero-Dependency Vanilla`)**:
   - Construido 100% con APIs nativas del navegador (`HTMLCanvasElement`, `CanvasRenderingContext2D`, `Path2D`, `ImageData`, `CSS Variables`, `LocalStorage` y `Local Font Access API`).
   - Sin librerías externas de terceros (sin React, sin Vue, sin jQuery, sin npm build pipelines). El código carga instantáneamente en cualquier navegador moderno.
2. **Motor Multicapa No Destructivo**:
   - Soporta un número ilimitado de capas con orden z independiente, opacidad de capa, opacidad de relleno (*Fill Opacity*), máscaras de capa (*Layer Masks*) y modos de fusión de color en tiempo real.
3. **Efectos de Capa en Vivo (Live FX)**:
   - Sombra paralela (*Drop Shadow*) y Resplandor exterior (*Outer Glow*) calculados e integrados dinámicamente en el compuesto.
4. **Suite Completa de 66 Herramientas Profesionales**:
   - Organizadas en 20 categorías de acceso rápido compatibles al 100% con los atajos estándar de la industria (Photoshop), con conmutación cíclica mediante tecla única y `Shift`.
5. **Herramientas Raster y Vectoriales Avanzadas**:
   - Trazados Bézier con pluma de precisión y puntos de ancla, formas geométricas paramétricas (rectángulos, elipses, polígonos, estrellas de N puntas, flechas), degradados suaves multicapa y tipografía interactiva con edición sobre el lienzo.
6. **Histograma Dinámico por Canales RGB**:
   - Análisis y renderizado en tiempo real de la distribución de frecuencias de los canales Rojo, Verde, Azul y Luminancia.
7. **Pila de Historial y Estados Reversibles**:
   - Motor de instantáneas profundas (*Snapshots*) con función ilimitada de Deshacer y Rehacer (`⌘Z` / `⌘⇧Z`).
8. **Arquitectura Modular Separada**:
   - Separación estricta entre la capa de interfaz y experiencia de usuario (**UIX**) y el motor gráfico y de herramientas (**TOOLS**), comunicados a través de una interfaz de contrato única (`window.Moviola`).

---

## ⚡ Características Principales (Features)

### 1. Sistema Multi-Documento en Pestañas (`Multi-Tab Body Area`)
- **Gestión Simultánea de Proyectos**: Permite abrir, editar y alternar entre múltiples proyectos gráficos o archivos RAW independientes sin salir de la aplicación.
- **Barra de Pestañas Dinámica (`.doc-tabs`)**: Muestra el nombre de cada archivo, el porcentaje de zoom en vivo, el espacio de color (`RGB/16*`) y un botón para cerrar la pestaña individual.
- **Aislamiento Total de Estado**: Cada pestaña almacena de manera encapsulada sus propias capas, selecciones, historial de deshacer/rehacer, coordenadas de zoom/paneo, guías y metadatos.
- **Lienzo Inicial Multicapa (`AI-Startup-Hero.RAW`)**: Al iniciar, el editor precarga un proyecto de diseño tecnológico completo de 1024 × 526 px compuesto por **9 capas independientes y 100% editables** (fondos con degradado, brillo neón rubí, guías láser, símbolo 3D infinito con transparencias y capas de texto estilizadas con tipografía moderna).

### 2. Motor de Tipografía y Detección de Fuentes del Sistema
- **Edición Tipográfica en el Lienzo (*On-Canvas Inline Text Editor*)**: Al hacer clic con la herramienta de texto (`T`), se despliega un editor interactivo en el punto exacto del lienzo que actualiza la capa tipográfica en tiempo real a medida que se escribe.
- **Sondeo de Fuentes Locales (*Font Probing Engine*)**: Algoritmo que compara métricas de texto (`measureText`) contra fuentes base del sistema (`sans-serif`, `serif`, `monospace`) para comprobar qué fuentes de un catálogo de más de 70 familias están físicamente instaladas en la máquina del usuario (macOS, Windows, Linux).
- **Compatibilidad con `Local Font Access API`**: Integración con `window.queryLocalFonts()` para consultar directamente las tipografías instaladas cuando el navegador lo permite.
- **Integración con Google Fonts**: Precarga de tipografías contemporáneas como *Plus Jakarta Sans* y *Outfit*.

### 3. Sistema de Internacionalización Multilingüe (i18n)
- **7 Idiomas Integrados**:
  - 🇪🇸 **Español** (`es`)
  - 🇬🇧 **English** (`en`)
  - 🇫🇷 **Français** (`fr`)
  - 🇩🇪 **Deutsch** (`de`)
  - 🇨🇳 **中文 (简体)** (`zh`)
  - 🇯🇵 **日本語** (`ja`)
  - 🇮🇳 **हिन्दी** (`hi`)
- **Detección Automática por Navegador**: Al abrir la aplicación, detecta automáticamente el idioma preferido del sistema del usuario mediante `navigator.languages`.
- **Selector en Menú `File > Settings...` (`⌘,`)**: Permite cambiar de idioma en cualquier momento mediante botones interactivos de un clic o menú desplegable, traduciendo dinámicamente el 100% del DOM, menús, barras de herramientas, opciones y paneles laterales sin recargar la página. Persiste la elección en `localStorage`.

---

## 🛠️ El Motor Detrás de las Herramientas (Graphic & Tool Engine)

El núcleo gráfico de Moviola está diseñado para operar con latencia mínima, garantizando una respuesta instantánea a 60 FPS:

```
┌────────────────────────────────────────────────────────────────────────┐
│                          WORKSPACE ESCENARIO                           │
│                                                                        │
│   ┌────────────────────────────────────────────────────────────────┐   │
│   │                      #stageShell (CSS3 Transform)              │   │
│   │                                                                │   │
│   │  ┌─────────────────────────┐     ┌──────────────────────────┐  │   │
│   │  │       #mainCanvas       │     │      #overlayCanvas      │  │   │
│   │  │    (Render Compuesto)   │     │    (Guías, Selección,    │  │   │
│   │  │   • Capas Raster/Vector │     │     Tiradores, Trazos)   │  │   │
│   │  │   • Modos de Fusión     │     │                          │  │   │
│   │  │   • Máscaras de Capa    │     │                          │  │   │
│   │  │   • Filtros de Ajuste   │     │                          │  │   │
│   │  └─────────────────────────┘     └──────────────────────────┘  │   │
│   └────────────────────────────────────────────────────────────────┘   │
└────────────────────────────────────────────────────────────────────────┘
```

### Arquitectura de Doble Lienzo (*Dual-Canvas Pipeline*)
1. **Lienzo Compuesto (`#mainCanvas`)**:
   - Es el búfer principal donde se dibuja el resultado final de la imagen.
   - Cada capa del documento posee su propio elemento `<canvas>` fuera de pantalla (*Offscreen Canvas*).
   - Durante `renderComposite()`, el motor recorre las capas visibles de abajo hacia arriba, aplica sus desplazamientos (`offsetX`, `offsetY`), sus máscaras de capa mediante operaciones `destination-in`, sus modos de fusión mediante `ctx.globalCompositeOperation` y sus efectos de sombra o resplandor.
   - Aplica filtros de color CSS nativos y correcciones de píxeles directas con `getImageData` y `putImageData` para curvas de Gamma y Temperatura tonal.
2. **Lienzo Superpuesto Interactivo (`#overlayCanvas`)**:
   - Se sitúa exactamente sobre el lienzo principal con eventos de puntero activos.
   - Dibuja en tiempo real las guías de recorte (*Crop Box* con regla de tercios), el contorno de hormigas marchantes (*Marching Ants*) de las selecciones geométricas y de lazo, las líneas de previsualización de degradados, los tiradores de transformación libre (*Transform Handles*), las mesas de trabajo, los sectores de exportación (*Slices*) y los trazados Bézier.

### Algoritmo de Auto-Selección Inteligente (`Auto-Select Hit-Testing`)
Al hacer clic con la herramienta Mover (`V`) con la opción *Auto-Select* habilitada:
1. El motor ejecuta `findLayerAtPoint(px, py)` evaluando las capas visibles en orden Z descendente (de la más alta a la más baja).
2. **Capas de Texto**: Calcula la caja delimitadora matemática considerando la posición, longitud, alineación y métricas de tipografía mediante `isPointInTextLayer()`.
3. **Capas de Píxeles**: Convierte las coordenadas del clic a las coordenadas locales de la capa (`lx = px - offsetX`, `ly = py - offsetY`) y consulta el canal alfa del píxel exacto con `ctx.getImageData(lx, ly, 1, 1)`. Si el valor alfa `pixel[3] > 8`, la capa es impactada de forma precisa incluso sobre siluetas irregulares o zonas transparentes.
4. **Agrupaciones**: Si el objetivo está configurado en modo `Group`, resuelve automáticamente el grupo padre de la capa impactada.

### Algoritmos de Procesamiento de Imagen y Píxeles
- **Varita Mágica (`magicWandSelect`)**: Muestrea el píxel bajo el cursor y recorre el mapa de bits aplicando el algoritmo de tolerancia euclidiana en el espacio cromático RGB (`ΔR² + ΔG² + ΔB² ≤ Tolerance²`).
- **Relleno Según el Contenido (`contentAwareFill`)**: Algoritmo que analiza el perímetro exterior del área seleccionada, muestrea los píxeles colindantes de textura y color circundantes y sintetiza un relleno orgánico continuo con gradiente de difusión y suavizado Gaussiano.
- **Herramientas de Retoque (Tampón de Clonar, Pincel Corrector, Parche)**: Muestrean un punto de origen definido por el usuario (`Alt + Clic`) y proyectan los píxeles preservando la textura o mezclando luminancia y color sobre el destino.

---

## 📑 El Sistema de Capas (Layers System)

El panel de capas de Moviola proporciona un control exhaustivo no destructivo sobre la composición:

### Tipos de Capas Soportadas
- **Capas de Píxeles (Raster)**: Lienzos de mapa de bits para pintura digital, retoque, clonación, borrado y filtros.
- **Capas de Texto (Vectoriales)**: Capas con metadatos tipográficos (`textData`), escalables, con modificación en caliente de fuente, color, tamaño, alineación e interlineado.
- **Capas de Formas Geométricas**: Rectángulos, elipses, triángulos, polígonos, estrellas y trazados vectoriales Bézier renderizados con precisión matemática.
- **Grupos de Capas (`group`)**: Carpetas jerárquicas para organizar, mover, ocultar o transformar múltiples capas simultáneamente.
- **Capas de Ajuste (`adjustment`)**: Capas no destructivas que aplican correcciones de exposición, contraste, brillo, niveles o posterización a las capas subyacentes.

### Modos de Fusión de Capas
Integración nativa mapeada directamente sobre el motor de composición de Canvas:
- **Normal**: Composición alfa estándar (`source-over`).
- **Multiplicar (Multiply)**: Multiplica los valores de luminosidad, oscureciendo la composición (`multiply`).
- **Trama (Screen)**: Multiplica los inversos de los colores, aclarando las luces (`screen`).
- **Superponer (Overlay)**: Combina Multiplicar y Trama según el brillo de la capa inferior (`overlay`).
- **Oscurecer (Darken)**: Selecciona el valor más oscuro de cada canal (`darken`).
- **Aclarar (Lighten)**: Selecciona el valor más claro de cada canal (`lighten`).
- **Sobreexponer Color (Color Dodge)**: Divide el color inferior por el inverso del color de la capa (`color-dodge`).
- **Subexponer Color (Color Burn)**: Invierte el color inferior, lo divide por la capa y lo vuelve a invertir (`color-burn`).

### Máscaras de Capa y Efectos en Vivo (FX)
- **Máscaras Alfa en Blanco y Negro**: Permiten ocultar selectivamente áreas de una capa usando pinceles o selecciones sin borrar los píxeles originales.
- **Sombra Paralela (Drop Shadow)**: Configurable con ángulo, distancia, desenfoque y color.
- **Resplandor Exterior (Outer Glow)**: Genera un halo de luz perimétrico sobre los bordes opacos.
- **Selección Múltiple de Capas**: Soporta selección continua con `Shift` y selección discontinua con `Cmd` / `Ctrl`, permitiendo arrastrar, alinear o transformar múltiples capas coordinadamente.

---

## ⌨️ Tabla Exhaustiva de Atajos de Teclado (Keyboard Shortcuts)

Moviola implementa la convención universal de atajos de teclado de Photoshop para garantizar una transición inmediata a profesionales del diseño:

### 1. Herramientas de la Barra Lateral (Acceso Directo y Rotación con `Shift`)

| Tecla | Herramienta Principal | Subherramientas en el Grupo (`Shift + Tecla`) |
| :---: | :--- | :--- |
| **`V`** | **Mover** (*Move Tool*) | Mesa de trabajo (*Artboard Tool*) |
| **`M`** | **Marco Rectangular** (*Rectangular Marquee*) | Marco elíptico, Marco de fila única, Marco de columna única |
| **`L`** | **Lazo** (*Lasso Tool*) | Lazo poligonal, Lazo magnético |
| **`W`** | **Selección de Objetos** (*Object Selection*) | Selección rápida, Varita mágica |
| **`C`** | **Recortar** (*Crop Tool*) | Recorte con perspectiva, Sector (*Slice*), Seleccionar sector |
| **`I`** | **Cuentagotas** (*Eyedropper*) | Cuentagotas de material 3D, Muestra de color, Regla, Nota, Recuento |
| **`J`** | **Pincel Corrector Puntual** (*Spot Healing*) | Pincel corrector, Parche, Movimiento con detección de contenido, Ojos rojos |
| **`B`** | **Pincel** (*Brush Tool*) | Lápiz, Sustitución de color, Pincel mezclador |
| **`S`** | **Tampón de Clonar** (*Clone Stamp*) | Tampón de motivo |
| **`Y`** | **Pincel de Historia** (*History Brush*) | Pincel histórico artístico |
| **`E`** | **Borrador** (*Eraser Tool*) | Borrador de fondos, Borrador mágico |
| **`G`** | **Degradado** (*Gradient Tool*) | Bote de pintura, Colocar material 3D |
| **`R`** | **Desenfocar** (*Blur Tool*) | Enfocar (*Sharpen*), Dedo (*Smudge*) |
| **`O`** | **Sobreexponer** (*Dodge Tool*) | Subexponer (*Burn*), Esponja (*Sponge*) |
| **`P`** | **Pluma Bézier** (*Pen Tool*) | Pluma de curvatura, Añadir punto de ancla, Eliminar punto de ancla, Convertir punto |
| **`T`** | **Texto Horizontal** (*Horizontal Type*) | Texto vertical, Máscara de texto horizontal, Máscara de texto vertical |
| **`A`** | **Selección de Trazado** (*Path Selection*) | Selección directa (*Direct Selection*) |
| **`U`** | **Rectángulo** (*Rectangle Tool*) | Rectángulo redondeado, Elipse, Triángulo, Polígono, Línea, Forma personalizada |
| **`H`** | **Mano** (*Hand Tool*) | Girar vista (*Rotate View*) |
| **`Z`** | **Zoom** (*Zoom Tool*) | Alternar Zoom In / Zoom Out |

---

### 2. Atajos de Archivo y Gestión de Documentos

| Atajo (macOS) | Atajo (Windows/Linux) | Acción |
| :--- | :--- | :--- |
| **`⌘ + N`** | **`Ctrl + N`** | Nuevo documento / Nueva pestaña de proyecto |
| **`⌘ + O`** | **`Ctrl + O`** | Abrir archivo de imagen local en una nueva pestaña |
| **`⌘ + W`** | **`Ctrl + W`** | Cerrar la pestaña o proyecto activo |
| **`Ctrl + Tab`** | **`Ctrl + Tab`** | Pasar a la siguiente pestaña abierta |
| **`Ctrl + Shift + Tab`** | **`Ctrl + Shift + Tab`** | Volver a la pestaña anterior |
| **`⌘ + S`** | **`Ctrl + S`** | Guardar documento |
| **`⌘ + ⇧ + S`** | **`Ctrl + Shift + S`** | Exportar imagen como archivo PNG a disco |
| **`⌘ + ,`** | **`Ctrl + ,`** | Abrir diálogo de Configuración y Preferencias (*Settings*) |

---

### 3. Atajos de Edición, Historial y Transformación

| Atajo (macOS) | Atajo (Windows/Linux) | Acción |
| :--- | :--- | :--- |
| **`⌘ + Z`** | **`Ctrl + Z`** | Deshacer (*Undo*) |
| **`⌘ + ⇧ + Z`** / **`⌘ + Y`** | **`Ctrl + Shift + Z`** / **`Ctrl + Y`** | Rehacer (*Redo*) |
| **`⌘ + X`** | **`Ctrl + X`** | Cortar píxeles de la selección activa |
| **`⌘ + C`** | **`Ctrl + C`** | Copiar la selección activa al portapapeles interno |
| **`⌘ + V`** | **`Ctrl + V`** | Pegar portapapeles como una nueva capa |
| **`⌘ + T`** | **`Ctrl + T`** | Transformación libre (*Free Transform*) |
| **`⌘ + A`** | **`Ctrl + A`** | Seleccionar todo el lienzo |
| **`⌘ + D`** | **`Ctrl + D`** | Deseleccionar (*Deselect*) |
| **`⌘ + ⇧ + I`** | **`Ctrl + Shift + I`** | Invertir selección activa |
| **`Supr`** / **`Backspace`** | **`Delete`** / **`Backspace`** | Borrar píxeles seleccionados o eliminar capa activa |
| **`Enter`** | **`Enter`** | Confirmar recorte (*Apply Crop*) o aplicar texto |
| **`Escape`** | **`Escape`** | Cancelar recorte, cerrar modal o descartar selección |

---

### 4. Atajos de Capas (*Layers*)

| Atajo (macOS) | Atajo (Windows/Linux) | Acción |
| :--- | :--- | :--- |
| **`⌘ + J`** | **`Ctrl + J`** | Duplicar capa activa o duplicar contenido seleccionado |
| **`⌘ + G`** | **`Ctrl + G`** | Crear un nuevo grupo con las capas seleccionadas |
| **`⌘ + E`** | **`Ctrl + E`** | Combinar capa activa con la inferior (*Merge Down*) |
| **`⌘ + ⇧ + E`** | **`Ctrl + Shift + E`** | Combinar todas las capas visibles (*Merge Visible*) |
| **`⌘ + ⇧ + ]`** | **`Ctrl + Shift + ]`** | Traer capa al frente (orden Z superior) |
| **`⌘ + ⇧ + [`** | **`Ctrl + Shift + [`** | Enviar capa al fondo (orden Z inferior) |
| **`⌘ + ]`** | **`Ctrl + ]`** | Subir capa un nivel |
| **`⌘ + [`** | **`Ctrl + [`** | Bajar capa un nivel |

---

### 5. Atajos de Vista, Zoom y Escenario

| Atajo (macOS) | Atajo (Windows/Linux) | Acción |
| :--- | :--- | :--- |
| **`⌘ + 0`** | **`Ctrl + 0`** | Ajustar documento a la pantalla (*Fit to Screen*) |
| **`⌘ + 1`** | **`Ctrl + 1`** | Píxeles reales al 100% (*Actual Pixels*) |
| **`⌘ + +`** | **`Ctrl + +`** | Acercar (*Zoom In*) centrado en el visor |
| **`⌘ + -`** | **`Ctrl + -`** | Alejar (*Zoom Out*) centrado en el visor |
| **`Rueda Ratón`** | **`Mouse Wheel`** | Desplazamiento horizontal y vertical (*Pan*) |
| **`Alt / ⌘ + Rueda`** | **`Alt / Ctrl + Wheel`** | Zoom interactivo centrado en la posición del cursor |
| **`Barra Espaciadora`** | **`Spacebar`** (Mantener) | Activar temporalmente la herramienta Mano (*Hand Pan*) |
| **`F`** | **`F`** | Alternar modos de pantalla (Estándar / Pantalla Completa) |
| **`Tab`** | **`Tab`** | Ocultar / Mostrar paneles laterales y barras flotantes |

---

### 6. Atajos de Pincel, Herramientas y Muestrarios de Color

| Atajo | Acción |
| :---: | :--- |
| **`[`** | Disminuir tamaño del pincel en píxeles |
| **`]`** | Aumentar tamaño del pincel en píxeles |
| **`{` (`Shift + [`)** | Disminuir dureza del pincel (*Hardness*) |
| **`}` (`Shift + ]`)** | Aumentar dureza del pincel (*Hardness*) |
| **`X`** | Intercambiar color frontal y de fondo (*Swap Colors*) |
| **`D`** | Restablecer colores por defecto: Blanco y Negro (*Default Colors*) |
| **`Q`** | Activar / Desactivar modo de Máscara Rápida (*Quick Mask*) |
| **`Alt + Clic`** | Definir origen de muestreo para Tampón de Clonar o Pincel Corrector |

---

## 🗂️ Estructura del Código Fuente

El proyecto sigue una arquitectura desacoplada y limpia dividida en módulos:

```
foto/
├── index.html          # Estructura semántica del DOM y orquestación de scripts
├── uix.css             # Estilos de interfaz: temas, paneles, modales, pestañas y menús
├── tools.css           # Estilos de lienzos, cursores, recuadros de selección y recorte
├── tools.js            # Motor gráfico: capas, transformaciones, algoritmos de píxel y 66 herramientas
├── uix.js              # Experiencia de usuario: menús, atajos globales, paneles laterales y modales
├── i18n.js             # Motor de internacionalización: traducciones en 7 idiomas y auto-detección
├── guide.md            # Guía técnica profunda de la arquitectura y contratos de interfaz
├── README.md           # Documentación principal del proyecto
└── assets/             # Recursos estáticos, iconos y fuentes
```

---

## 🧪 Pruebas Automatizadas y Suite de Auditoría

Para asegurar la robustez total del sistema, Moviola cuenta con herramientas automáticas de validación integradas:

### 1. Verificación Automática de las 66 Herramientas (`__testAll66Tools()`)
- Ejecuta una prueba funcional interactiva sobre cada una de las 66 herramientas: activación, renderizado de opciones, simulación de eventos `pointerdown`, `pointermove` y `pointerup` sobre el canvas interactivo y validación de renderizado compuesto sin excepciones.
- **Resultado de la suite**: **66/66 superadas con éxito (100% pasando)**.
- Puede ejecutarse en consola del navegador con `window.__testAll66Tools()` o accediendo con el parámetro URL:
  ```
  https://moviola.fenix.ninja/?autotest=1
  ```

### 2. Auditoría de Botones de Interfaz (`auditUI()`)
- Escanea todos los botones y elementos de menú del DOM verificando que cada uno posea un controlador de acción (`data-action`, `data-tool` o `data-adjust`) válido y conectado, garantizando que no existan botones muertos en la aplicación.
- Ejecutable desde el menú `Help > Run UI Button Check` o mediante `window.__uiAudit()`.

---

## 🚀 Cómo Ejecutar el Proyecto Localmente

Al ser una aplicación web pura sin dependencias de compilación ni empaquetadores (no requiere `npm install` ni `webpack`), ejecutarla localmente es inmediato:

### Opción 1: Abrir directamente en el navegador
Basta con hacer doble clic en el archivo [index.html] o arrastrarlo a Google Chrome, Safari, Firefox o Edge.

### Opción 2: Usar un servidor estático local
Puedes levantarlo con cualquier servidor HTTP para habilitar todas las APIs web avanzadas:

```bash
# Con Python 3
python3 -m http.server 8000

# Con Node.js (npx)
npx serve .

# Con PHP
php -S localhost:8000
```
Luego abre tu navegador en `http://localhost:8000`.

---

## 👨‍💻 Autor y Créditos

Desarrollado con dedicación y pasión por la ingeniería web por:

**Fénix Ríos**
- Sitio web: [https://fenix.ninja](https://fenix.ninja)
- Aplicación en vivo: [https://moviola.fenix.ninja](https://moviola.fenix.ninja)

---

## © Copyright © 2023-2026 Fénix Rios

Este proyecto está bajo la Licencia Privada. 
Si eres libre de usarlo, y No puedes Modificarlo ni uso comercial.
