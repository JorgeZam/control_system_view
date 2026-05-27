# CONTROL·LAB — Visor de Respuesta PID

Demostración para EL4203 Programación Avanzada. Página web estática que lee
resultados de simulación de un sistema de control (controlador PID sobre una
planta de segundo orden) desde `datos.json` y los visualiza.

## Qué muestra
- **Respuesta a escalón** de tres sintonías PID (conservadora, balanceada, agresiva).
- **Señal de control** u(t) con saturación del actuador.
- **Radar comparativo** del desempeño normalizado.
- **Barras** comparando sobrepaso y tiempo de asentamiento.
- **Métricas** (sobrepaso, asentamiento, subida, error permanente) por sintonía.

## Archivos
- `index.html` — toda la interfaz (HTML + CSS + JS, Chart.js desde CDN).
- `datos.json` — resultados de la simulación (generados aparte, no calculados aquí).

## Ejecutar localmente
Por el `fetch` de `datos.json`, necesita un servidor (no abrir el archivo directo):

    python3 -m http.server 8000

Luego abrir http://localhost:8000

## Desplegar en Vercel
1. Subir esta carpeta a un repositorio de GitHub.
2. Conectar el repo en vercel.com (framework preset: "Other", sin build).
3. Listo: queda en una URL pública.

> Nota: la página solo *muestra* resultados ya calculados. La simulación del
> sistema dinámico se hace aparte; por eso este proyecto encaja en el modelo
> estático de Vercel sin necesidad de backend.
