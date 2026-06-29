# Guía de Estilos — Arcane Brews SPA

## 1. Paleta de Colores

| Token | Hex | Uso | Contraste AA |
|---|---|---|---|
| Primary/Crimson | #8B0000 | Botones primarios, header | ✅ 7.2:1 sobre blanco |
| Primary/Gold | #D4AF37 | Acentos, precios, estrellas | ✅ 4.6:1 sobre oscuro |
| Primary/Dark | #1A0A00 | Fondo hero, footer | ✅ 18:1 sobre blanco |
| Surface/Background | #F5F0E8 | Fondo general SPA | — |
| Surface/Card | #FFFFFF | Cards y modales | — |
| Surface/Panel | #EDE8DC | Paneles laterales | — |
| Text/Primary | #1A0A00 | Texto principal | ✅ 18:1 sobre #F5F0E8 |
| Text/Secondary | #5C4A3A | Texto de apoyo | ✅ 6.8:1 sobre #F5F0E8 |
| Text/Muted | #9C8877 | Placeholders, hints | ✅ 4.5:1 sobre blanco |
| Feedback/Success | #2D6A4F | Confirmaciones | ✅ 5.1:1 sobre blanco |
| Feedback/Error | #C0392B | Errores formulario | ✅ 5.8:1 sobre blanco |
| Feedback/Warning | #E67E22 | Alertas | ✅ 4.6:1 sobre oscuro |

## 2. Tipografía

| Token | Fuente | Tamaño | Peso | Uso |
|---|---|---|---|---|
| Heading/H1 | Cinzel | 32px | 700 | Títulos principales |
| Heading/H2 | Cinzel | 24px | 700 | Títulos de sección |
| Heading/H3 | Cinzel | 20px | 700 | Subtítulos |
| Body/Large | Lora | 18px | 400 | Cuerpo principal |
| Body/Base | Lora | 16px | 400 | Texto general |
| Body/Small | Lora | 14px | 400 | Texto secundario |
| UI/Label | Inter | 14px | 500 | Labels de formulario |
| UI/Button | Inter | 16px | 700 | Texto de botones |
| UI/Caption | Inter | 12px | 400 | Notas, breadcrumbs |

> Todas las fuentes son Google Fonts de uso libre.
> Tamaño mínimo: 16px para texto de lectura (WCAG 1.4.4).

## 3. Sistema de Espaciado (Base 8px)

| Token | Valor | Uso |
|---|---|---|
| space-1 | 8px | Gap mínimo entre elementos |
| space-2 | 16px | Padding interno de componentes |
| space-3 | 24px | Separación entre secciones |
| space-4 | 32px | Margen entre bloques |
| space-5 | 48px | Separación de secciones grandes |
| space-6 | 64px | Espacios hero/header |

## 4. Componentes

### Botón Principal
- Tamaño mínimo: 44×44px (WCAG 2.5.5)
- Estados: Default, Hover, Focus, Disabled, Loading
- Focus: anillo dorado 3px offset (WCAG 2.4.7)

### Card de Poción
- Imagen con alt text descriptivo (WCAG 1.1.1)
- role="article" aria-labelledby apunta al nombre
- Mínimo 44px en área interactiva

### Campo de Formulario
- label explícito asociado con for/id (WCAG 1.3.1)
- Error con ícono + texto + color (WCAG 1.4.1)
- aria-required="true" en campos obligatorios
- aria-describedby conecta campo con mensaje de error

### Badge de Estado
- Siempre ícono + texto (nunca solo color) (WCAG 1.4.1)
- Estados: Entregado, En camino, Pendiente, Cancelado