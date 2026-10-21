# Documentación — Proyecto Arq Software

Índice y matriz de trazabilidad de toda la documentación del proyecto. Cada documento nuevo se registra aquí en el mismo cambio en que se crea o modifica.

## Estructura

```
Documentacion/
├── README.md                  ← este índice
├── 01-referencias/            material fuente y sus traducciones
│   └── imagenes/              figuras usadas por los documentos de la carpeta
├── 02-mapa-capacidades/       mapa de capacidades de negocio y su modelado
└── 03-casos-de-uso/           casos de uso y su modelado
```

| Carpeta | Contenido | Prefijo de ID |
|---|---|---|
| `01-referencias/` | Material fuente externo (libros, artículos, informes) y sus traducciones | `REF` |
| `02-mapa-capacidades/` | Mapa de capacidades de negocio y su modelado | `CAP` |
| `03-casos-de-uso/` | Casos de uso y su modelado | `CU` |

## Convenciones

- **Ubicación:** todo documento generado en el proyecto se guarda dentro de `Documentacion/`, en la carpeta de su tipo. Las imágenes van en una subcarpeta `imagenes/` junto al documento que las usa, enlazadas con rutas relativas.
- **Identificador:** `<PREFIJO>-<NN>` (por ejemplo, `CAP-02`). Es único y no se reutiliza aunque el documento se retire.
- **Nombre de archivo y carpeta:** en minúsculas, con guiones, sin espacios ni tildes (`mapa-capacidades-etapa-2.md`). Las carpetas de primer nivel llevan un número de orden (`04-...`).
- **Encabezado:** cada documento Markdown nuevo empieza con su identificador, versión, fecha y los documentos de los que deriva.
- **Trazabilidad:** la columna «Deriva de» indica de qué documentos sale cada uno; «Relacionado con» indica los documentos que deben mantenerse coherentes con él.
- **Estados:** `Borrador` → `En revisión` → `Aprobado` → `Obsoleto`.
- **Nueva carpeta:** cuando aparezca un tipo de documento que no encaje en las anteriores, se crea la carpeta con el siguiente número y se añade a la tabla de estructura con su prefijo.

## Matriz de documentos

| ID | Documento | Ruta | Tipo | Deriva de | Relacionado con | Fecha | Estado |
|---|---|---|---|---|---|---|---|
| REF-01 | *The Business Capability Map: The «Rosetta Stone» of Business/IT Alignment* (Ulrich y Rosen, Cutter Consortium, 2011) | [`01-referencias/rosetta-stone-ulrich-rosen-2011.pdf`](01-referencias/rosetta-stone-ulrich-rosen-2011.pdf) | Referencia (PDF) | — | REF-02 | 2026-10-15 | Aprobado |
| REF-02 | Traducción al español de REF-01 (con sus 17 figuras) | [`01-referencias/el-mapa-de-capacidades-de-negocio.md`](01-referencias/el-mapa-de-capacidades-de-negocio.md) | Traducción (Markdown) | REF-01 | CAP-01 | 2026-10-15 | Aprobado |
| CAP-01 | Modelo ArchiMate: mapa de capacidades y casos de uso de July (Cooperativa Padre Julián Lorente) | [`02-mapa-capacidades/mapa-capacidades-y-casos-de-uso.archimate`](02-mapa-capacidades/mapa-capacidades-y-casos-de-uso.archimate) | Modelo Archi (nativo) | REF-02 | CU-01 | 2026-10-20 | Borrador |
| CU-01 | Exportación ArchiMate 3.1 (Open Exchange) de los casos de uso de July | [`03-casos-de-uso/casos-de-uso-july-archimate.xml`](03-casos-de-uso/casos-de-uso-july-archimate.xml) | Modelo ArchiMate (XML de intercambio) | CAP-01 | CAP-01 | 2026-10-20 | Borrador |

## Historial de cambios del índice

| Fecha | Cambio |
|---|---|
| 2026-10-21 | Creación del índice y registro de los documentos existentes. |
| 2026-10-21 | Reorganización: carpetas numeradas sin espacios, imágenes movidas junto a REF-02 y archivos renombrados según la convención. |
