# PPR Designer · Estilo referencia

Aplicación web HTML/CSS/JS para diseño rápido de Prótesis Parcial Removible (PPR) con odontograma FDI, conectores mayores, retenedores UDD y exportación JSON.

## Uso local

Abre `index.html` directamente en el navegador.

## Publicación en GitHub Pages

1. Crea un repositorio nuevo en GitHub.
2. Sube `index.html` a la raíz del repositorio.
3. En GitHub: Settings → Pages.
4. Source: Deploy from a branch.
5. Branch: `main` / root.
6. Guarda y espera a que GitHub Pages entregue la URL pública.

## Vista 3D

La pestaña **3D · Modelo** (sobre el odontograma) muestra el mismo caso en 3D con [three.js](https://threejs.org/). Se diseña en el odontograma 2D y la vista 3D se actualiza sola; también permite seleccionar dientes y elementos con un clic.

- **Arcada paramétrica**: se genera desde el odontograma FDI (no usa modelos de pacientes). Los dientes ausentes muestran la rejilla de retención.
- **Coronas** con constricción cervical, ecuador dentario y cúspides según el tipo de diente; los brazos retentivos terminan bajo el ecuador.
- **Elementos de la PPR** con el mismo código de colores que los dibujos PNG. El lado de origen del retenedor se elige hacia la brecha desdentada; *Volteo horizontal* cambia mesial ↔ distal y *Volteo vertical* intercambia los brazos retentivo y recíproco.
- **Conectores mayores** siguen la arcada y respetan la posición y escala dadas en 2D. *Placa palatina / placoide* se dibuja como placa palatina en el maxilar o como placa lingual en la mandíbula, según dónde se ubique.
- **Ver en metal** alterna entre colores didácticos y metal Co-Cr; **Descargar PNG** guarda una imagen de la vista.

three.js se descarga desde el CDN jsDelivr solo al abrir la pestaña 3D, por lo que esa vista necesita conexión a internet. El resto de la app funciona sin conexión.

## Estructura

- `index.html`: app completa en un solo archivo.
- `.nojekyll`: evita procesamiento Jekyll en GitHub Pages.

## Notas

Esta versión es un prototipo docente/visual. La lógica clínica debe ser validada por el docente antes de usarla como herramienta oficial.
