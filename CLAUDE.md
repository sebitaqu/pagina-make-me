# CLAUDE.md — Katemi Beauty Website

## Reglas de Comportamiento Claude

- Leer archivos existentes antes de escribir. No releer salvo que cambien.
- Razonamiento profundo, output conciso.
- Sin openers sycofanticos ni cierre con fluff.
- Sin emojis ni em-dashes en respuestas.
- No adivinar APIs, versiones, flags ni nombres de paquetes — verificar en código o docs primero.
- Código primero. Explicación solo si no es obvio.
- Sin boilerplate salvo que se pida explícitamente.
- Solución más simple que funcione. Sin over-engineering.
- Sin abstracciones para operaciones de un solo uso.
- Sin features especulativas.
- Sin manejo de errores para escenarios que no pueden ocurrir.
- Tres líneas similares es mejor que una abstracción prematura.

---

## Proyecto
Sitio web para **Katemi**, una tienda de maquillaje y belleza femenina con personalidad de boutique íntima y cercana. No es retail masivo: es una experiencia personalizada, cálida y sofisticada.

---

## Identidad de Marca

| Campo | Valor |
|-------|-------|
| **Nombre** | Katemi |
| **Eslogan** | "Maquillaje que realza tu esencia" |
| **Categoría** | Tienda de maquillaje y belleza femenina |
| **Personalidad** | Delicada, femenina, elegante, cercana, dulce, amigable, acogedora |

### ADN de Marca
- El maquillaje **no transforma** a las personas — **realza** lo que ya existe.
- La belleza auténtica nace de la **confianza**.
- Cada mujer tiene una **esencia única**.
- La experiencia de compra debe sentirse **cálida y especial**.
- La comunicación nunca debe ser agresiva ni basada en presión de venta.

**Sensación que debe transmitir:** Cercana · Amable · Elegante · Femenina · Tierna · Premium accesible

---

## Paleta de Colores

```css
:root {
  /* Primarios */
  --color-primary:        #E8C5B8;  /* Rosa nude empolvado */
  --color-primary-soft:   #F2D9D0;  /* Rosa maquillaje suave */

  /* Secundarios */
  --color-chocolate:      #7D5A50;  /* Marrón chocolate suave */
  --color-pink-pastel:    #F7E0DA;  /* Rosa pastel */
  --color-beige:          #F5EDE8;  /* Beige rosado */

  /* Fondos */
  --color-bg:             #FDF6F3;  /* Fondo principal */
  --color-bg-card:        #FFF9F7;  /* Fondo tarjetas */

  /* Texto */
  --color-text-dark:      #4A3228;  /* Texto principal */
  --color-text-mid:       #7D5A50;  /* Texto secundario */
  --color-text-light:     #B89690;  /* Texto sutil */

  /* Acento */
  --color-accent:         #C4897A;  /* Rosa terracota suave */
}
```

**Evitar:** colores neón, saturados o contrastes agresivos.

---

## Tipografía

- **Display/Títulos:** Serif elegante, moderna, editorial — inspiración en cosmética premium y revistas de moda. Opciones: `Cormorant Garamond`, `Playfair Display`, `DM Serif Display`.
- **Cuerpo/UI:** Serif delicada o sans-serif refinada para legibilidad. Opciones: `Lora`, `EB Garamond`, `Jost`.
- **No usar:** tipografías infantiles, pesadas, ni fuentes corporativas genéricas (Inter, Arial, Roboto).

---

## Estética Visual

**Estilo:** Quiet luxury + Soft luxury + Beauty boutique + Feminidad moderna + Minimalismo elegante

**Elementos gráficos a usar:**
- Destellos minimalistas (sparkle SVGs, puntos brillantes sutiles)
- Sombras suaves (box-shadow difuminada, sin dureza)
- Gradientes delicados (de un rosa a otro, nunca saturados)
- Formas orgánicas redondeadas (border-radius generoso, blobs)
- Patito Katemi (mascota, ver sección abajo)

**Evitar:** decoraciones excesivas, saturación visual, elementos infantiles exagerados, efectos tipo retail agresivo.

---

## Mascota — Patito Katemi

### Descripción
Un pequeño pato femenino, protagonista sutil de la experiencia visual.

### Rasgos visuales
- Ojo con pestaña larga
- Mejillas rosadas (rubor)
- Expresión suave y coqueta
- Aspecto limpio y minimalista
- Inspiración: kawaii elegante — **no infantil exagerado, no caricatura extrema**

### Comportamiento en el sitio
- Se asoma desde bordes de secciones
- Observa productos
- Guiña un ojo
- Interactúa suavemente con elementos visuales
- **Nunca roba protagonismo al producto**

### Implementación sugerida
Crear el patito como SVG inline con animaciones CSS sutiles (float, peek, blink).

---

## Fotografía de Producto

- El producto es **siempre la estrella principal**
- Fondo: rosa nude / beige rosado
- Iluminación suave, sombras delicadas
- Mucho espacio negativo
- Sensación premium y limpia
- El patito puede asomarse discretamente en esquinas

---

## Tono de Voz (Copywriting)

Hablar como **una amiga elegante**, nunca como una empresa.

| No usar | Usar |
|---------|------|
| "Aprovecha nuestras promociones." | "Elegimos esto porque sabemos que te hará sentir increíble." |
| "Compra ahora." | "Creemos que te encantará." |
| "Oferta limitada." | "Lo seleccionamos especialmente para ti." |
| "Stock disponible." | "Está esperándote." |

### Mensajes clave a reforzar
Belleza auténtica · Confianza · Delicadeza · Amor propio · Feminidad · Cuidado personal

---

## Experiencia de Usuaria

La clienta debe sentir que:
- Es **bienvenida**
- Está siendo **atendida personalmente**
- Está comprando en una **boutique especializada**
- Está recibiendo una **recomendación genuina**

No debe sentirse como una compra masiva de retail.

---

## Estructura Sugerida del Sitio

```
/                   → Hero + Eslogan + CTA suave
/productos          → Catálogo con filtros por categoría
/producto/:id       → Detalle de producto (producto como estrella)
/nosotras           → Historia de Katemi, ADN de marca, patito
/contacto           → Formulario cálido, redes sociales
```

### Secciones del Home
1. **Hero** — Eslogan, imagen hero, CTA suave ("Descubre tu esencia")
2. **Destacados** — Productos seleccionados ("Lo elegimos para ti")
3. **Filosofía** — ADN de la marca, breve y visual
4. **Categorías** — Navegación visual por tipo de producto
5. **Testimonios** — Reseñas de clientas (tono cálido)
6. **Patito CTA** — Sección con el patito invitando a explorar
7. **Footer** — Logo, redes, frase de marca

---

## Directrices Técnicas

- **Framework preferido:** HTML/CSS/JS vanilla o React (según scope)
- **Responsive:** Mobile-first, experiencia perfecta en celular
- **Animaciones:** Suaves, CSS-first, ningún movimiento brusco
- **Accesibilidad:** Contraste suficiente en textos, alt en imágenes
- **Performance:** Imágenes optimizadas, lazy loading
- **Fuentes:** Google Fonts (Cormorant Garamond + Lora recomendadas)

---

## Prohibiciones Absolutas

- Colores neón o saturados
- Tipografías corporativas genéricas
- Lenguaje de ventas agresivo
- Estética de retail masivo (banners de "OFERTA", "DESCUENTO", etc.)
- Decoraciones excesivas o elementos infantiles exagerados
- El patito más llamativo que el producto
- Sombras duras o contrastes agresivos

---

## Referencias de Estilo

Buscar inspiración en:
- Glossier (minimalismo beauty)
- Charlotte Tilbury (feminidad premium)
- Kosas (editorial suave)
- Laneige (soft luxury coreano)
- Revistas: Vogue Beauty, Harper's Bazaar Beauty

---

*Este documento define la identidad completa de Katemi. Toda decisión de diseño, copy y UX debe pasar el filtro: ¿Esto se siente como una boutique íntima y elegante, o como un retail genérico? Si es lo segundo, rediseñar.*
