# Decisiones de Diseño — Arcane Brews SPA

## Decisión 1: Elección de Fuentes

**¿Qué?** Cinzel para headings, Lora para body, Inter para UI.

**¿Por qué?**
- Cinzel evoca estética medieval D&D manteniendo legibilidad
- Lora es una serif legible para textos largos de descripción
- Inter es la fuente más legible para interfaces digitales

**Principio SWEBOK:** Usabilidad — la tipografía debe servir al contexto
temático sin sacrificar legibilidad.

**Patrón aplicado:** Escala tipográfica modular con ratio 1.25.

---

## Decisión 2: Paleta de Colores

**¿Qué?** Crimson (#8B0000) como color primario con Gold (#D4AF37)
como acento.

**¿Por qué?**
- Evoca atmósfera de taberna y magia medieval
- Contraste mínimo 4.5:1 verificado (WCAG 1.4.3)
- Gold sobre Dark supera 4.6:1 de contraste

**Principio SWEBOK:** Accesibilidad como calidad no funcional.

**Patrón aplicado:** Color semántico — cada color tiene un rol
específico (Primary, Surface, Text, Feedback).

---

## Decisión 3: Sistema de Navegación Accesible

**¿Qué?** Skip links, breadcrumbs semánticos, landmarks ARIA,
menú navegable por teclado.

**¿Por qué?**
- HU-06: usuarios necesitan saltar contenido repetido
- WCAG 2.4.1 Bypass Blocks (Nivel A)
- Usuarios con motor impairment dependen del teclado

**Principio SWEBOK:** Diseño para todos los usuarios desde el inicio.

**Patrón aplicado:** Progressive enhancement — funciona sin JS,
mejora con JS.

---

## Decisión 4: Formulario con Validación Accesible

**¿Qué?** Labels explícitos, mensajes de error con ícono+color+texto,
aria-describedby, aria-required.

**¿Por qué?**
- HU-05: Aprendiz con Temblor necesita formularios claros
- WCAG 3.3.1 Error Identification (Nivel A)
- WCAG 3.3.2 Labels or Instructions (Nivel A)
- El error nunca se comunica solo por color (WCAG 1.4.1)

**Principio SWEBOK:** Manejo de errores centrado en el usuario.

**Patrón aplicado:** Inline validation con feedback inmediato.

---

## Decisión 5: Cards de Poción

**¿Qué?** role="article", alt text descriptivo en imágenes,
aria-label en botones de acción.

**¿Por qué?**
- HU-01: Mago Invidente necesita contexto completo por lector
- WCAG 1.1.1 Non-text Content (Nivel A)
- Sin alt text las imágenes son invisibles para lectores de pantalla

**Principio SWEBOK:** Calidad de información — completitud y
precisión del contenido.

**Patrón aplicado:** Semantic HTML con ARIA augmentation.

---

## Decisión 6: Estados de Pedido con Ícono+Texto

**¿Qué?** Badges con ícono + texto en lugar de solo color.

**¿Por qué?**
- WCAG 1.4.1 Use of Color — la información no puede depender
  solo del color
- Usuarios con daltonismo no distinguen verde/rojo/naranja
- El ícono agrega redundancia semántica

**Principio SWEBOK:** Robustez — el diseño funciona para
el mayor rango posible de usuarios.

**Patrón aplicado:** Redundant coding — mismo dato por
múltiples canales (color + forma + texto).

---

## Decisión 7: Feedback de Carga con aria-live

**¿Qué?** aria-live="polite" y aria-busy en secciones dinámicas
como pedidos y carrito.

**¿Por qué?**
- HU-07: Druida con Conexión Lenta necesita saber que el
  sistema responde
- WCAG 4.1.3 Status Messages (Nivel AA)
- Sin aria-live el lector de pantalla no anuncia cambios dinámicos

**Principio SWEBOK:** Confiabilidad — el sistema comunica su
estado al usuario en todo momento.

**Patrón aplicado:** Live regions para contenido dinámico.