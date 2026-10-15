# Tablero de estudio: renovación del registro calificado

Tecnología en Gestión Criminalística y Análisis Forense · Fundación de Educación Superior Alberto Merani.
Herramienta interna de estudio para la sustentación o la visita de pares, elaborada a partir del documento radicado (2026).

## Archivos

| Archivo | Uso |
|---|---|
| `index.html` | Tablero. Lee los datos de la carpeta `datos/`. Requiere publicarse (GitHub Pages) o abrirse con un servidor local. |
| `tablero_offline.html` | Mismo tablero con datos y librería incrustados. Se abre con doble clic, sin internet. No refleja cambios hechos en `datos/`. |
| `datos/cifras.json` | Series numéricas (`serie`, `categoria`, `subcategoria`, `valor`, `pagina`, `nota`). |
| `datos/fichas.json` | Hechos clave por condición (`id`, `condicion`, `tema`, `dato`, `pagina`). |
| `datos/preguntas.json` | Preguntas probables (`id`, `condicion`, `pregunta`, `respuesta`, `pagina`, `soporte`). |
| `datos/verificar.json` | Puntos por verificar (`id`, `condicion`, `prioridad` Alta/Media/Baja, `hallazgo`, `detalle`, `pagina`, `accion`). |
| `datos/anexos.json` | Índice de anexos (`condicion`, `anexo`, `descripcion`). |

## Publicar en GitHub Pages

1. Cree un repositorio **privado** y suba esta carpeta.
2. En *Settings → Pages* seleccione la rama y la carpeta raíz. Las páginas desde repositorios privados requieren un plan de GitHub que lo permita; si no, use un repositorio de la organización con acceso restringido o comparta `tablero_offline.html` por un canal interno.
3. Para probar en su equipo: `python -m http.server` dentro de la carpeta y abra `http://localhost:8000`.

## Cómo actualizar los datos

- Edite los JSON conservando los nombres de las columnas y las comillas; cada `id` debe ser único.
- `condicion` debe repetirse exactamente igual entre archivos (por ejemplo, `CC3 Aspectos curriculares`), porque alimenta los filtros.
- Si cambia los datos, regenere `tablero_offline.html` o aclare a los usuarios que esa versión no los refleja.

## Advertencias

- Las cifras de gráficas se leyeron del PDF y deben contrastarse con Q10 y los anexos antes de citarlas.
- Las preguntas y respuestas son una propuesta de estudio, no un documento oficial de la Fundación.
- No suba el repositorio como público: el contenido proviene de un documento institucional radicado ante el MEN.
