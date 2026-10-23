# La Cazuela de la 24 - Repositorio GitHub Ready

Este directorio está optimizado para cargarse directamente en GitHub y desplegarse en GitHub Pages.

## Solución al problema de carga de imágenes:
Los servidores de GitHub Pages funcionan en sistemas Linux donde los nombres de archivo son **estrictamente sensibles a mayúsculas/minúsculas y extensiones** (por ejemplo, `.jpeg` vs `.JPEG` vs `.jpg`).

Se ha implementado una rutina inteligente de recuperación automática en JavaScript (`tryNextExt`):
1. Intenta cargar el archivo original.
2. Si falla por diferencias de minúsculas/mayúsculas o formato (`.JPEG`, `.jpeg`, `.jpg`, `.JPG`, `.png`), prueba automáticamente todas las variaciones.
3. Si la foto no existe localmente, muestra un elegante indicador SVG visual en lugar de un icono roto de navegador.
