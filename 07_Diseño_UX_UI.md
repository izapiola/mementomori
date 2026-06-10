# Diseño UX/UI — Memento Mori Gin

---

## Principios aplicados a esta marca

El gin se sirve sin garnish. El sitio funciona igual: sin elementos que no sirvan.  
Cada decisión de diseño tiene una razón filosófica además de una razón técnica.

---

## 1. Jerarquía visual

**Regla general:** el ojo del usuario sigue tamaño → contraste → posición.

Aplicado a Memento Mori:
- La frase "Recuerda que vas a morir." es el elemento más grande de la página. No el logo. No el precio. La idea.
- El producto entra después de que el visitante ya entiende de qué se trata.
- El CTA de compra es claro, pero no urgente. No "¡Comprá ahora!". Solo "Comprar — $25.000".

---

## 2. Tipografía

**Máximo dos familias tipográficas.**

| Uso | Tipografía | Por qué |
|---|---|---|
| Títulos, citas, manifiesto | Playfair Display (serif) | Evoca tradición, filosofía, peso |
| Cuerpo, precios, navegación | Inter (sans-serif) | Claridad, neutralidad, modernidad |

**Reglas de uso:**
- Títulos: Playfair Display, mayúsculas, tracking amplio (+0.05em)
- Subtítulos: Playfair Display italic, tamaño medio
- Cuerpo: Inter, 400 o 300, línea de 1.7–1.8 (legibilidad máxima)
- Precios y datos técnicos: Inter, 500, sin serif

---

## 3. Color

Paleta de tres colores. Sin excepciones.

| Nombre | Hex | Uso |
|---|---|---|
| Negro profundo | `#0A0A0A` | Fondo hero, secciones oscuras |
| Crema | `#F5F0E8` | Texto sobre negro, fondos claros |
| Blanco puro | `#FFFFFF` | Fondos de secciones de producto |

Sin colores de acento. Sin gradientes. Sin transparencias decorativas.  
El contraste negro-crema es el único "color de marca".

---

## 4. Espaciado y whitespace

**El espacio en blanco es un elemento de diseño, no ausencia de diseño.**

En una marca premium, el espacio comunica que la marca no necesita llenar cada centímetro para justificarse. Lo mismo que el gin sin garnish.

- Padding mínimo entre secciones: 120px vertical en desktop, 80px en mobile.
- Los párrafos del manifiesto tienen interlineado de 1.8.
- El producto nunca compite en el mismo viewport con texto denso.

---

## 5. Mobile-first

El tráfico llega desde Instagram. Instagram es mobile.  
El diseño se construye primero para 375px de ancho, después se adapta a desktop.

Principio: si algo no funciona en mobile, no funciona.

---

## 6. Estructura de la página (arquitectura de la información)

```
┌─────────────────────────────┐
│  NAV: logo izq. — CTA der.  │  (sticky, desaparece al scrollear)
├─────────────────────────────┤
│                             │
│   HERO (100vh, fondo negro) │
│   "Recuerda que vas a morir"│
│   [subtítulo del manifiesto]│
│   [flecha scroll]           │
│                             │
├─────────────────────────────┤
│                             │
│   MANIFIESTO (fondo crema)  │
│   3 párrafos seleccionados  │
│                             │
├─────────────────────────────┤
│                             │
│   PRODUCTO (fondo blanco)   │
│   [foto botella] [datos]    │
│   560ml · 42% ABV · 10 bot. │
│   $25.000 ARS               │
│   [Comprar]                 │
│                             │
├─────────────────────────────┤
│                             │
│   LA PRÁCTICA (fondo negro) │
│   Fragmento del manifiesto  │
│   [Leer manifiesto completo]│
│                             │
├─────────────────────────────┤
│  FOOTER: mínimo             │
│  © Memento Mori · Pergamino │
└─────────────────────────────┘
```

---

## 7. CTA (Call to Action)

**Un solo CTA primario por página: Comprar.**

- Diseño: borde fino (1px) crema sobre negro, o negro sobre blanco. Sin relleno de color.
- Texto: "Comprar — $25.000" (no "Agregar al carrito", no "Comprar ahora")
- Hover: inversión de fondo/texto
- Sin íconos, sin flechas, sin animaciones en el botón

El botón es austero porque la marca es austera.

---

## 8. Fotografía

**Una sola foto del producto. Bien tomada.**

- Fondo: negro profundo o blanco puro. Sin props.
- Iluminación: lateral, que muestre el líquido y la etiqueta.
- La botella ocupa el 60–70% del frame.
- Sin manos. Sin copa. Sin mesa.

Si todavía no hay foto profesional: fondo negro + render/mockup como placeholder.

---

## 9. Confianza y fricción

**Lo que se incluye para generar confianza:**
- Dirección de producción: "Destilería Los Terpenos, Pergamino"
- Datos del lote: "Lote inaugural · 200 botellas · Nº [X]"
- Checkout con Mercado Pago (logo visible)
- Política de envíos clara (cuántos días, quién paga)

**Lo que no se incluye:**
- Reseñas (no existen todavía — inventarlas es deshonesto)
- Garantías de satisfacción (el estoico no promete lo que no controla)
- Badges de "producto certificado" genéricos

---

## 10. Performance

- Sin videos autoplay.
- Sin animaciones de scroll complejas (la austeridad es también técnica).
- La imagen del producto es el único asset pesado — se optimiza a WebP.
- Carga en menos de 2 segundos en mobile con 4G.

---
