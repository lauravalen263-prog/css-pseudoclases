# Pseudoclases de CSS

Repositorio de referencia con **todas las pseudoclases de CSS**, agrupadas por categoría, más una página de ejemplos vivos (`index.html`).

## Cómo usarlo

1. Clona o descarga el repositorio.
2. Abre `index.html` en el navegador (o usa la extensión Live Server de VS Code).
3. Edita `css/styles.css` para experimentar.

## Estructura

```
css-pseudoclases/
├── index.html        # ejemplos vivos con su código
├── css/styles.css    # estilos y demos de cada pseudoclase
├── README.md         # esta referencia
└── .gitignore
```

> **Sintaxis:** una pseudoclase empieza con `:` y se agrega a un selector: `selector:pseudoclase { ... }`.
> Las marcadas como *experimental* o *limitado* tienen soporte parcial; revisa [MDN](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes) o [Can I use](https://caniuse.com).

## 1. Enlaces y ubicación

| Pseudoclase | Selecciona |
|---|---|
| `:link` | Enlaces aún no visitados |
| `:visited` | Enlaces ya visitados |
| `:any-link` | Cualquier enlace (`:link` + `:visited`) |
| `:local-link` | Enlaces que apuntan a la misma página *(limitado)* |
| `:target` | Elemento cuyo `id` coincide con el fragmento `#` de la URL |
| `:target-within` | Elemento que contiene al `:target` *(limitado)* |
| `:scope` | Elemento de referencia del selector (en `querySelector`, `@scope`) |

## 2. Acción del usuario

| Pseudoclase | Selecciona |
|---|---|
| `:hover` | Elemento bajo el puntero |
| `:active` | Elemento que se está presionando |
| `:focus` | Elemento con foco |
| `:focus-visible` | Foco cuando el navegador considera que debe verse (teclado) |
| `:focus-within` | Elemento que tiene un descendiente con foco |

## 3. Formularios y entrada

| Pseudoclase | Selecciona |
|---|---|
| `:enabled` / `:disabled` | Controles habilitados / deshabilitados |
| `:read-only` / `:read-write` | Elementos no editables / editables |
| `:placeholder-shown` | Campo que muestra su `placeholder` |
| `:default` | Opción o botón por defecto del formulario |
| `:checked` | Checkbox, radio u option marcados |
| `:indeterminate` | Checkbox/radio/progress en estado indeterminado |
| `:valid` / `:invalid` | Campos que cumplen / no cumplen su validación |
| `:user-valid` / `:user-invalid` | Igual, pero solo después de que el usuario interactuó |
| `:in-range` / `:out-of-range` | Valor dentro / fuera de `min` y `max` |
| `:required` / `:optional` | Campos obligatorios / opcionales |
| `:autofill` | Campo rellenado por el navegador |
| `:blank` | Campo vacío *(experimental)* |

## 4. Estructurales (árbol del documento)

| Pseudoclase | Selecciona |
|---|---|
| `:root` | Raíz del documento (`<html>`) |
| `:empty` | Elementos sin hijos ni texto |
| `:first-child` / `:last-child` / `:only-child` | Primer / último / único hijo |
| `:nth-child(n)` / `:nth-last-child(n)` | Hijo en la posición `n` contando desde el inicio / final |
| `:first-of-type` / `:last-of-type` / `:only-of-type` | Primero / último / único de su tipo de etiqueta |
| `:nth-of-type(n)` / `:nth-last-of-type(n)` | Posición `n` entre hermanos del mismo tipo |

Fórmulas útiles de `n`: `odd`, `even`, `3n`, `3n+1`, `-n+3` (los 3 primeros).

## 5. Funcionales (lógicas)

| Pseudoclase | Selecciona |
|---|---|
| `:is(a, b)` | Cualquiera de la lista (toma la mayor especificidad) |
| `:where(a, b)` | Igual que `:is`, con especificidad cero |
| `:not(a)` | Lo que **no** coincide |
| `:has(a)` | Elemento que **contiene** (o precede a) algo que coincide |
| `:lang(es)` | Elementos según su idioma |
| `:dir(rtl)` | Elementos según la dirección del texto |

## 6. Estado de la pantalla y del navegador

| Pseudoclase | Selecciona |
|---|---|
| `:fullscreen` | Elemento en pantalla completa |
| `:modal` | Elemento modal (por ejemplo `<dialog>` con `showModal()`) |
| `:picture-in-picture` | Video en imagen en imagen |
| `:popover-open` | Popover abierto |
| `:open` | `<details>`, `<dialog>` o `<select>` abiertos |
| `:defined` | Elementos estándar o custom elements ya registrados |
| `:active-view-transition` | Raíz durante una transición de vista *(reciente)* |

## 7. Medios (audio y video)

| Pseudoclase | Selecciona |
|---|---|
| `:playing` / `:paused` | Medio en reproducción / en pausa |
| `:seeking` | Medio buscando una posición |
| `:buffering` / `:stalled` | Medio cargando / detenido por falta de datos |
| `:muted` | Medio silenciado |
| `:volume-locked` | Volumen bloqueado por el navegador |

## 8. Web Components (Shadow DOM)

| Pseudoclase | Selecciona |
|---|---|
| `:host` | El elemento que aloja al shadow tree |
| `:host(sel)` | El host solo si coincide con `sel` |
| `:host-context(sel)` | El host si un ancestro coincide *(limitado)* |
| `:state(nombre)` | Estado personalizado de un custom element |

## 9. Temporales (experimentales)

| Pseudoclase | Selecciona |
|---|---|
| `:current` / `:past` / `:future` | Texto activo / pasado / futuro en subtítulos (WebVTT) |

## Recursos

- [MDN: Pseudoclases](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes)
- [Can I use](https://caniuse.com)
