# CONTROL LAB - Visor de Respuesta PID

Proyecto de demostracion para EL4203 Programacion Avanzada.
Es una aplicacion web estatica que carga resultados de simulacion desde
`datos.json` y los visualiza en graficos interactivos.

## Funcionalidades
- Respuesta a escalon para tres sintonias PID: conservadora, balanceada y agresiva.
- Señal de control `u(t)` con saturacion del actuador.
- Radar comparativo de desempeno normalizado.
- Grafico de barras para sobrepaso y tiempo de asentamiento.
- Panel de metricas por sintonia: sobrepaso, asentamiento, subida y error permanente.

## Estructura del proyecto
- `index.html`: interfaz completa (HTML, CSS y JavaScript) usando Chart.js por CDN.
- `datos.json`: resultados precomputados de simulacion.
- `.gitignore`: exclusiones de archivos locales para Git.

## Requisitos
- Navegador web moderno.
- Un servidor HTTP local (necesario porque `fetch` no funciona abriendo el archivo directo).

## Ejecutar en local
Desde la carpeta del proyecto:

```bash
python -m http.server 8000
```

Luego abrir:

```text
http://localhost:8000
```

## Despliegue en Vercel
1. Sube este proyecto a GitHub.
2. En Vercel, importa el repositorio.
3. Selecciona el preset `Other` y deja Build Command vacio.
4. Deploy.

## Notas
- Esta app no ejecuta la simulacion numerica en el frontend.
- Solo consume y presenta resultados ya generados en `datos.json`.
- Es compatible con despliegue estatico (sin backend).
