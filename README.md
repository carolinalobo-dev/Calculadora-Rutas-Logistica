<div align="center">

# 🚚 Calculadora Dinámica de Rutas Logísticas

**App de escritorio que calcula la ruta de una entrega en CABA y avisa si el tráfico o el clima pueden complicarla.**

![Python](https://img.shields.io/badge/Python-3-3776AB?style=flat-square&logo=python&logoColor=white)
![Tkinter](https://img.shields.io/badge/UI-Tkinter-FFB020?style=flat-square)
![OSRM](https://img.shields.io/badge/ruteo-OSRM-19F5A0?style=flat-square)
![Open-Meteo](https://img.shields.io/badge/clima-Open--Meteo-22E5FF?style=flat-square)

</div>

## Qué resuelve

En logística de última milla, salir sin saber cómo está el tráfico o el clima en destino genera demoras y riesgos. Esta aplicación permite al repartidor anticiparlos antes de salir: ingresa origen, destino y hora, y obtiene distancia, tiempo estimado y alertas.

## Funcionalidades

- 📍 **Geocodificación** de direcciones en texto libre (Nominatim / OpenStreetMap).
- 🛣️ **Cálculo de ruta real** por calles, con distancia y duración (OSRM).
- 🚦 **Ajuste del tiempo según la franja horaria**: hora pico de mañana, hora pico de tarde, horario normal y nocturno.
- ⛈️ **Alertas climáticas** en el punto de destino: lluvia, tormentas (Open-Meteo).
- 🗺️ **Mapa interactivo** con el recorrido dibujado.
- ✅ Validación de datos de entrada (campos vacíos y formato de hora `HH:MM`).

## Cómo funciona

```
Direcciones ─▶ Nominatim ─▶ coordenadas ─▶ OSRM ─▶ distancia y tiempo base
                                                          │
Hora de salida ─▶ factor de tráfico (x1.0 a x2.5) ────────┤
                                                          ▼
Coordenadas de destino ─▶ Open-Meteo ─▶ alertas   ─▶  resultado + mapa
```

## Stack

| Área | Tecnología |
|---|---|
| Lenguaje | Python 3 |
| Interfaz | Tkinter, tkintermapview |
| Geocodificación | Nominatim (OpenStreetMap) |
| Ruteo | Project OSRM |
| Meteorología | Open-Meteo |

Todas las APIs son públicas y no requieren clave.

## Cómo ejecutarlo

```bash
pip install requests tkintermapview
python centroLogistico.py
```

## Proyecto relacionado

Una versión ampliada, trabajada en equipo, con monitoreo y alertas del transporte público: [**DeliverysProyect**](https://github.com/carolinalobo-dev/DeliverysProyect).

## Autora

**Carolina Lobo** · [LinkedIn](https://www.linkedin.com/in/carolina-lobo-469705297)
