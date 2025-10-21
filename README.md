# 🌦️ NR Weather App

Una aplicación de clima desarrollada en Node-RED que permite consultar el estado actual del tiempo en cualquier ubicación ingresada por el usuario. Utiliza la API de OpenWeatherMap para obtener coordenadas y clima actual en tiempo real.


## Características

- Entrada de texto para ubicación (ciudad)
- Geocodificación automática mediante OpenWeatherMap
- Consulta del clima actual:
  - 🌡️ Temperatura
  - 🧊 Sensación térmica
  - 💧 Humedad
- Visualización en dashboard con:
  - 📍 Ubicación formateada
  - 📈 Gráfico histórico de temperatura
  - 🕹️ Indicadores tipo gauge


## Componentes principales

- `ui-text-input`: ingreso de ubicación
- `template`: armado de URLs para geocoding y clima
- `http request`: llamadas a la API
- `change`: extracción de datos relevantes
- `ui-gauge`, `ui-chart`, `ui-text`: visualización en el dashboard


## Seguridad

⚠️ Este flujo incluye una API key genérica en los nodos de plantilla. Se recomienda:

- Reemplazar `"API_key"` por tu clave personal desde OpenWeatherMap


## Requisitos

- Node-RED instalado
- Cuenta en [OpenWeatherMap](https://openweathermap.org/) para obtener tu API key
- Paleta `node-red-dashboard` de flowFuse instalada


## 📁 Estructura del flujo

```plaintext
[ubicación] → [geocoding API] → [extraer lat/lon] → [weather API] → [visualización]
