# ⛳ Golf Stats — Driving Range Analyzer

Aplicación web para analizar sesiones de driving range con datos de launch monitor (Trackman, GC2, FlightScope).

Disponible en dos versiones:
- **`index.html`** — Versión móvil (PWA instalable en iPhone/Android)
- **`golf_stats.html`** — Versión escritorio (dashboard completo)

---

## 📲 Instalar en iPhone

1. Abre Safari y ve a tu URL de GitHub Pages
2. Toca el botón compartir **□↑**
3. Toca **"Añadir a pantalla de inicio"**
4. Listo — funciona como app nativa sin conexión

## 💻 Usar en ordenador

Descarga `golf_stats.html` y ábrelo directamente en cualquier navegador. No necesita servidor ni instalación.

---

## 📂 Cargar una sesión

1. Exporta el CSV desde tu launch monitor
2. En la app, ve a la pestaña **Datos** (móvil) o usa el botón **"Seleccionar CSV"** (escritorio)
3. Selecciona el fichero — los datos se cargan al instante

El CSV debe tener el formato estándar de exportación con columnas como `Tipo de palo`, `Distancia total`, `Cara del palo`, etc.

---

## 🏌️ Funcionalidades

### Vista de campo
- Mapa de caída de bolas en vista cenital
- Color por: calidad de impacto, distancia, desviación lateral, cara del palo, efecto lateral, ángulo de ataque, backspin, velocidad de palo/bola, altura máxima
- Rangos dinámicos por cuartiles — se adaptan al palo seleccionado
- Cruz de referencia al seleccionar un golpe
- Tooltip con todos los parámetros

### Filtros
- Filtrar por palo (SW, PW, H9, H8, H7, H6, H5)
- Clic en leyenda para filtrar por rango de cualquier métrica
- Panel de filtros min/max por parámetro
- Ocultar golpes individuales (excluir de estadísticas)
- Reset completo con un clic

### Estadísticas
- Media, mínimo, máximo y desviación estándar por palo
- Comparación del golpe seleccionado vs media de su palo
- Dispersión lateral con indicador visual
- Tabla ordenable con todos los golpes y todos los parámetros

### Parámetros analizados
| Parámetro | Descripción |
|-----------|-------------|
| Distancia total / vuelo | Metros totales y de vuelo |
| Desviación lateral | Metros a izquierda (−) o derecha (+) |
| Cara del palo | Ángulo de la cara en impacto (°) |
| Línea de swing | Club path — out-to-in (+) / in-to-out (−) |
| Ángulo de ataque | Ascendente (+) / descendente (−) |
| Backspin | Revoluciones de retroceso (rpm) |
| Efecto lateral | Fade-spin (+) / draw-spin (−) (rpm) |
| Velocidad de palo / bola | m/s |
| Calidad de impacto | Smash factor (vel. bola / vel. palo) |
| Altura máxima | Metros |
| Eje de rotación | Inclinación del eje de giro (°) |

---

## 🛠 Tecnología

- HTML + CSS + JavaScript puro — sin dependencias ni frameworks
- Canvas API para el mapa de campo
- Compatible con cualquier navegador moderno
- PWA instalable en iOS 14+ y Android

---

## 📋 Formato CSV compatible

El fichero debe ser exportado directamente desde el software del launch monitor. Se espera:
- Primera fila: nombres de columnas
- Segunda fila: unidades (se omite automáticamente)
- Resto de filas: datos de cada golpe

Columnas reconocidas: `Tipo de palo`, `Fecha`, `Vel. palo`, `Cara del palo`, `Línea cabeza del palo`, `Ángulo de ataque`, `Distancia total`, `Distancia de desviación total`, `Dist.​vuelo`, `Retroceso`, `Efecto lateral`, `Calidad del impacto`, `Altura máxima`, `Velocidad de la pelota`, `Eje de rotación`, `Velocidad de rotación`, y más.

---

## 📸 Capturas

| Campo de caída | Estadísticas | Filtros |
|---|---|---|
| Vista cenital con colores por calidad | Parámetros por palo o golpe seleccionado | Cuartiles dinámicos por palo |

---

*Desarrollado para análisis personal de sesiones de golf. Compatible con datos de Garmin Golf y otros launch monitors con exportación CSV.*
