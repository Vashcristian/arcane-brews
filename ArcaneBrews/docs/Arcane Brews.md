# Arcane Brews - Tienda de Pociones Mágicas

**Nombre del sistema:** Arcane Brews - Tienda de Pociones Mágicas

**Descripción:** SPA de e-commerce donde magos, aventureros y alquimistas pueden explorar, filtrar y comprar pociones. Incluye catálogo, detalle de producto, carrito, perfil de usuario y panel de pedidos.

---

## Roles de Usuario

| **Rol** | **Descripción** | **Necesidad de Accesibilidad** |
|---|---|---|
| **Mago Invidente** | Usuario avanzado que compra pociones frecuentemente | Usa lector de pantalla (NVDA/JAWS). Necesita ARIA labels, orden lógico de foco, imágenes con alt text descriptivo |
| **Aprendiz de mago** | Usuario nuevo con problemas de parkinson | Navega solo con teclado, sin ratón. Necesita áreas de clic grandes (mín. 44x44px), skip links, sin time-outs |
| **Alquimista Mayor** | Usuario adulto mayor con baja visión | Necesita contraste alto (4.5:1+), texto escalable hasta 200% sin romper layout, fuente mínimo 16px |
| **Druida con Conexión Lenta** | Usuario en zona rural con internet limitado | Necesita carga optimizada, imágenes comprimidas, feedback de carga visible, sin autoplay |

---

## 7 Historias de Usuario

### Caso 1 / Explorar catálogo
Mago Invidente quiere que el catálogo de pociones tenga imágenes con texto alternativo descriptivo, para poder entender cada producto usando lector de pantalla NVDA/JAWS.

### Caso 2 / Filtrar pociones
Aprendiz quiere filtrar pociones por categoría usando solo el teclado, para no depender del ratón.

### Caso 3 / Ver detalle de poción
Alquimista Mayor quiere que el texto de descripción de cada poción sea legible al 200% de zoom, para leerlo sin perder contenido.

### Caso 4 / Agregar al carrito
Mago Invidente quiere que al agregar una opción al carrito se anuncie una confirmación por lector de pantalla, para saber que la acción fue exitosa.

### Caso 5 / Completar formulario de compra
Aprendiz quiere que todos los campos del formulario tengan etiquetas visibles y mensajes de error descriptivos, para completar la compra sin confusión.

### Caso 6 / Navegar entre secciones
Aprendiz quiere un skip link al inicio de cada página para saltar directo al contenido principal, para no repetir la navegación en cada vista.

### Caso 7 / Ver mis pedidos
Druida con conexión lenta quiere que el historial de pedidos cargue con indicador de progreso visible, para saber que el sistema está respondiendo.
 
---

## Priorización (MoSCoW)

| **Prioridad** | **Historia** | **Funcionalidad** |
|---|---|---|
| **Must** | Caso 1, 2, 5, 6 | Catálogo, filtros por teclado, formulario accesible, skip links |
| **Should** | Caso 3, 4 | Zoom 200%, confirmación en carrito |
| **Could** | Caso 7 | Indicador de carga en pedidos |
| **Won't** | - | Modo oscuro automático, traducción automática |
