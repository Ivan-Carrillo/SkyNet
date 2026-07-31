# SkyNet

# ✈️ Red de Rutas Aéreas — TACA & Avianca

Aplicación web interactiva que modela una red de rutas aéreas reales mediante **relaciones binarias** y **matrices de adyacencia**, permitiendo buscar vuelos por número exacto de escalas, gestionar ciudades y rutas, y visualizar la red como un grafo.

Es la versión web de un programa de consola en Python que implementa la clase `RedRutasAereas`, pensado como proyecto académico de estructuras discretas (relaciones binarias, matrices y grafos).

🔗 **Demo:** abre `index.html` directamente en el navegador — no requiere instalación ni backend.

---

## 📌 Características

- **Dos aerolíneas independientes** (Avianca y TACA), cada una con su propia matriz de adyacencia y su propia lista de ciudades activas.
- **Búsqueda de vuelos por número de escalas**: indicas origen, destino y cuántas escalas quieres (0 = vuelo directo), y el sistema encuentra *todas* las rutas posibles con exactamente ese número de escalas, sin repetir ciudades (DFS con backtracking).
- **Gestión de la red**: agregar ciudades nuevas y registrar rutas directas entre cualquier par de ciudades.
- **Matriz de adyacencia** visual, con opción de mostrar solo las ciudades activas o la matriz completa.
- **Mapa de red (grafo tipo radar)**: visualización SVG de las ciudades activas y sus conexiones, con la ruta encontrada resaltada.
- Más de 55 ciudades reales de América Latina, España y Reino Unido, con rutas de ida y vuelta cargadas por defecto.

---

## 🧠 Fundamento teórico

El proyecto modela la red de vuelos como una **relación binaria** sobre el conjunto de ciudades, representada mediante una **matriz de adyacencia** `A` donde `A[i][j] = 1` si existe un vuelo directo de la ciudad `i` a la ciudad `j`.

- Un **vuelo directo** corresponde a una entrada `1` en la matriz.
- Una **conexión con escalas** corresponde a un camino en el grafo dirigido asociado, encontrado mediante búsqueda en profundidad (DFS) con backtracking, evitando ciclos.
- El proyecto puede extenderse fácilmente al cálculo de conectividad general mediante el **algoritmo de Warshall** o a la potencia de la matriz (`A²`, `A³`, …) para contar caminos de longitud fija.

---

## 🛠️ Tecnología

Un único archivo HTML autocontenido: **HTML + CSS + JavaScript vanilla**. Sin frameworks, sin dependencias, sin backend — todo corre en el navegador.

---

## 🚀 Cómo usarlo

1. Clona el repositorio o descarga el archivo.
2. Abre `index.html` en cualquier navegador moderno (Chrome, Firefox, Edge).
3. Selecciona una aerolínea, explora la red y prueba a buscar rutas con distintas escalas.

No requiere `npm install`, servidor local ni configuración adicional.

---

## 📂 Estructura del repositorio

```
.
├── index.html      # Aplicación completa (HTML + CSS + JS)
└── README.md        # Este archivo
```

---

## 🎓 Contexto académico

Este proyecto corresponde al **Trabajo 04: Análisis de rutas aéreas mediante relaciones y matrices de conectividad**, cuyo objetivo es modelar y analizar una red de rutas aéreas utilizando relaciones binarias y matrices de conectividad para determinar posibles conexiones entre nodos (ciudades), incluyendo vuelos directos y conexiones con escalas.

---

## 📄 Licencia

Proyecto de uso académico. Libre de usar y modificar con fines educativos.

## ✍️ Autor

**Ivan Leonardo Carrillo Alor**
