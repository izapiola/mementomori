# Setup Web — Tienda Nube + mementomori.ar

Guía para completar hoy. Tiempo estimado: 2–3 horas.

---

## Paso 1: Crear la cuenta en Tienda Nube

1. Ir a **tiendanube.com/ar**
2. Hacer clic en "Crear mi tienda gratis"
3. Registrarse con el email de la marca (no el personal)
4. Nombre de la tienda: **Memento Mori Gin**
5. Categoría: Bebidas / Alimentos y bebidas

**Plan recomendado para Fase 1:** Plan Emprendedor o Inicial.  
Tiene comisión por venta (~2%), pero es el más económico para arrancar. Evaluar Plan Pro cuando el volumen lo justifique (sin comisión por venta).

---

## Paso 2: Conectar el dominio mementomori.ar

### En el panel de Tienda Nube:
1. Ir a **Configuración → Dominios**
2. Hacer clic en "Agregar dominio propio"
3. Ingresar: `mementomori.ar`
4. Tienda Nube va a mostrar los registros DNS que hay que configurar

### En el panel de tu hosting (donde administran mementomori.ar):
Tienda Nube te va a pedir que configures uno de estos dos métodos:

**Opción A — CNAME (si el dominio usa subdomain www):**
```
Tipo: CNAME
Nombre / Host: www
Valor: stores.tiendanube.com
```
Más redirigir el dominio raíz (mementomori.ar) al www.

**Opción B — Registro A (apunta el dominio raíz directamente):**
```
Tipo: A
Nombre / Host: @ (o en blanco)
Valor: [IP que indique Tienda Nube — la plataforma la provee en ese paso]
```

**Tiempo de propagación DNS:** entre 15 minutos y 24 horas. En la mayoría de los casos, menos de 1 hora.

---

## Paso 3: Configurar la tienda (mínimo viable)

### 3.1 — Tema visual
- Ir a **Apariencia → Temas**
- Elegir un tema minimalista: **Maré** o **Sense** son los más austeros disponibles en Tienda Nube.
- Paleta de colores: negro (#000000), blanco (#FFFFFF), beige roto (#F5F0E8).
- Tipografía: serif para títulos (Georgia o similar), sans-serif para cuerpo (Inter o similar).

### 3.2 — Página de inicio
La home tiene una sola función: que el visitante entienda qué es Memento Mori y quiera comprar.

Estructura:
```
[Foto del producto — austera, fondo neutro]

"Recuerda que vas a morir."

[3 líneas del manifiesto]

[Botón: Comprar — $25.000]

[Link: Leer el manifiesto completo]
```

Sin carrusel. Sin sección "sobre nosotros" en la home. Sin pop-ups.

### 3.3 — Producto
- Ir a **Productos → Agregar producto**
- Nombre: **Memento Mori Gin**
- Descripción: extraer del manifiesto (no un texto de marketing — el mismo tono)
- Precio: $25.000 ARS
- Stock: 190 unidades (las 10 de reserva no se cargan como stock vendible)
- Foto: una sola imagen, bien tomada, fondo neutro

### 3.4 — Medios de pago
- Ir a **Pagos → Agregar medio de pago**
- Activar **Mercado Pago**: cubre tarjeta de crédito/débito, transferencia y cuotas.
- No agregar más opciones por ahora — menos fricción, más conversión.

### 3.5 — Envíos
- Ir a **Envíos → Configurar**
- Activar **Tienda Nube Envíos** (integrado con OCA y Andreani, calcula el costo automáticamente según el destino del comprador).
- Configurar el peso y dimensiones del paquete (botella de 560ml + packaging).
- El costo de envío lo paga el comprador — se muestra antes de finalizar la compra.

### 3.6 — Email de confirmación de compra
- Ir a **Configuración → Notificaciones → Confirmación de pedido**
- Editar el template. Reemplazar el texto genérico por:

```
Gracias.

Tu botella de Memento Mori Gin está en camino.

Elegiste un gin que existe porque la finitud importa.
Cuando lo abras, acordate de por qué lo compraste.

— Memento Mori
Pergamino, Argentina
```

---

## Paso 4: Verificar antes de publicar

Lista de control antes de hacer la tienda pública:

- [ ] El dominio mementomori.ar abre la tienda (puede tardar unas horas)
- [ ] El certificado SSL está activo (Tienda Nube lo gestiona automáticamente — aparece el candado en el navegador)
- [ ] Se puede agregar el producto al carrito
- [ ] El checkout funciona y llega al pago con Mercado Pago
- [ ] El email de confirmación llega después de una compra de prueba
- [ ] El stock se descuenta correctamente
- [ ] La tienda se ve bien en celular (la mayoría del tráfico va a venir de Instagram)

---

## Paso 5: Conectar Instagram

- Ir a **Canales de venta → Instagram Shopping** en Tienda Nube
- Vincular la cuenta de Instagram de la marca
- Esto permite etiquetar el producto en las publicaciones directamente

**Requisito de Instagram:** la cuenta debe estar en modalidad "Cuenta profesional" (no personal) y tener al menos un producto activo en la tienda.

---

## Lo que no configura hoy

- Blog integrado → el contenido largo va en el newsletter (Substack o similar), no en la tienda.
- Sección de reseñas → cuando haya compradores reales.
- Múltiples productos → cuando haya más SKUs.
- Descuentos o cupones → no existen por política de marca.

---

## Resultado al final del día

`mementomori.ar` abre una tienda austera con el manifiesto, una foto del producto y un botón de compra que funciona. El comprador paga, el sistema lo registra, y cuando el 3PL esté configurado, ellos despachan.

El equipo no toca nada entre el pedido y la entrega.

---
