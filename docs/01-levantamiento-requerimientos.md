# Levantamiento de requerimientos — Ecommerce de lencería

> Documento de descubrimiento para la reunión de kickoff con el cliente.
> Objetivo: obtener la información necesaria para definir alcance, estimación y arquitectura
> de una plataforma **nativa / a la medida** (sin Shopify ni WordPress).

---

## 1. Negocio y contexto

1. ¿La marca ya existe y vende (tienda física, redes sociales, marketplace) o es un lanzamiento desde cero?
2. ¿Cuál es el objetivo principal del sitio en los primeros 6–12 meses? (ventas directas, posicionamiento de marca, migrar ventas de WhatsApp/Instagram, mayoreo, etc.)
3. ¿Quién es el cliente final? (edad, género, poder adquisitivo, ¿compra para sí o para regalo?)
4. ¿Venden solo a un país o hay planes de venta internacional? ¿Qué monedas e idiomas se necesitan?
5. ¿Cuál es el volumen esperado? (número de SKUs, pedidos/mes estimados, picos por temporada: San Valentín, Buen Fin, Navidad)
6. ¿Existe competencia directa de referencia? ¿Qué les gusta y qué no de esos sitios?
7. ¿Hay fecha objetivo de lanzamiento? ¿Es negociable el alcance o la fecha?
8. ¿Cuál es el presupuesto aproximado para desarrollo y para operación mensual (hosting, pasarela, mantenimiento)?

## 2. Catálogo y producto (específico de lencería)

9. ¿Cuántos productos iniciales habrá y quién carga/redacta el catálogo (fotos, descripciones, medidas)?
10. **Variantes:** ¿los productos se manejan por talla + color + estilo? ¿Sistemas de tallas (S/M/L, copa 32B/34C, tallas extendidas/plus)? ¿Tallas distintas por región (MX/US/EU)?
11. ¿Se venden sets/conjuntos (bra + panty) como un solo SKU, como bundle armable, o ambos?
12. ¿Se necesita **guía de tallas interactiva** o calculadora de talla (medidas de busto/bajo busto)? Esto reduce muchísimo devoluciones en esta categoría.
13. ¿Manejo de inventario por variante? ¿El stock vive solo en el sitio o hay que sincronizar con tienda física / otro sistema (ERP, Excel, marketplace)?
14. ¿Habrá productos con preventa, apartado o "avísame cuando haya stock"?
15. ¿Fotografía de producto: ya existe, se producirá, o se usarán fotos de proveedor? ¿Se requiere tratamiento especial (modelos, maniquí, plano)?
16. ¿Categorización esperada? (por tipo: bras, pantys, bodys, pijamas; por colección; por ocasión; por talla)

## 3. Precios, pagos y facturación

17. ¿Qué métodos de pago se requieren? (tarjeta, transferencia/SPEI, OXXO/efectivo, MSI, PayPal, Mercado Pago, Apple/Google Pay)
18. ¿Ya tienen cuenta en alguna pasarela (Stripe, Mercado Pago, Conekta, Openpay) o hay que asesorarlos?
19. ¿Se requieren cupones, descuentos por volumen, precios de mayoreo, programa de lealtad o gift cards?
20. ¿Facturación fiscal? (en México: emisión de CFDI — ¿automática desde el sitio o manual?)
21. ¿Los precios incluyen impuestos? ¿Se venden a otros países con cálculo de impuestos/aranceles?

## 4. Envíos y logística

22. ¿Quién surte los pedidos? (bodega propia, dropshipping, tienda física)
23. ¿Paqueterías a integrar? (Estafeta, DHL, FedEx, 99minutos, Envia.com/Skydropx como agregador)
24. ¿Tarifas de envío: fijas, por peso, por código postal, envío gratis a partir de X monto?
25. ¿Se requiere rastreo de pedido dentro del sitio y notificaciones (email/WhatsApp)?
26. ¿Empaque discreto? En lencería es un diferenciador frecuente (privacidad del comprador).
27. **Devoluciones:** por higiene, la lencería usualmente no admite devolución una vez abierta. ¿Cuál será la política exacta de cambios/devoluciones y quién la redacta? El flujo del sitio debe reflejarla.

## 5. Legal y cumplimiento

28. ¿Existen términos y condiciones, aviso de privacidad y política de cookies, o hay que redactarlos? (protección de datos personales: LFPDPPP en México / GDPR si venden a Europa)
29. ¿Se requiere verificación o advertencia de edad para cierto contenido/productos?
30. ¿La marca está registrada? ¿Los nombres de producto y fotografías tienen derechos asegurados?
31. Publicidad y contenido: las imágenes de lencería suelen tener restricciones en Meta/Google Ads. ¿Quién gestiona campañas y conoce esas políticas?

## 6. Diseño, UX y marca

32. ¿Existe manual de identidad (logo, paleta, tipografías) o hay que crearlo?
33. ¿Sitios de referencia visual? Pedir 3–5 ejemplos concretos y qué les gusta de cada uno (navegación, fichas de producto, checkout).
34. ¿Tono de la marca: elegante/sensual, cómodo/cotidiano, juvenil, inclusivo (body positive, tallas extendidas)? Esto define fotografía, copy y UI.
35. ¿Mobile-first? (en esta categoría típicamente 70–85 % del tráfico es móvil; el diseño debe partir de ahí)
36. ¿Se requiere blog o secciones de contenido (guías de talla, cuidado de prendas) para SEO?

> **Nota sobre HTTrack:** usarlo para descargar un sitio de referencia sirve para *estudiar* estructura y layout,
> pero **no podemos reutilizar HTML, CSS, imágenes, textos ni marca de un sitio ajeno** — eso es infracción de
> derechos de autor y nos expone a nosotros y al cliente. La práctica correcta: tomar los sitios de referencia
> como inspiración, definir wireframes propios y construir la UI desde cero con nuestro propio design system
> (componentes, tokens de color/tipografía). Mismo resultado visual de calidad, sin riesgo legal.

## 7. Funcionalidad del sitio (alcance MVP vs. fases)

37. ¿Compra como invitado, con registro, o ambas? ¿Login social (Google/Apple)?
38. ¿Wishlist / favoritos? ¿Carrito persistente entre dispositivos?
39. ¿Reseñas de producto con fotos? ¿Moderación?
40. ¿Búsqueda con filtros (talla, color, precio, tipo)? ¿Autocompletado?
41. ¿Recuperación de carrito abandonado (email/WhatsApp)?
42. ¿Chat de soporte (WhatsApp Business, chat embebido)?
43. ¿Newsletter y automatizaciones de email marketing (bienvenida, post-compra)? ¿Con qué herramienta?
44. ¿Qué es indispensable para el día 1 (MVP) y qué puede ir en fase 2? Proponer al cliente una tabla de priorización MoSCoW.

## 8. Panel de administración y operación

45. ¿Quién operará el sitio día a día y qué nivel técnico tiene? (define qué tan simple debe ser el admin)
46. ¿Qué necesita gestionar el admin? (productos, inventario, pedidos, cupones, banners/home, contenido)
47. ¿Roles y permisos? (dueño, operador de pedidos, marketing)
48. ¿Reportes requeridos? (ventas, productos top, inventario bajo, conversión)
49. ¿Notificaciones internas de nuevo pedido? (email, WhatsApp, dashboard)

## 9. Técnico e infraestructura

50. ¿Dominio ya comprado? ¿Quién administra DNS y correo corporativo?
51. ¿Preferencia o restricción de hosting/nube? (Vercel/Netlify + backend gestionado, VPS, AWS/GCP)
52. ¿Requisitos de integración con sistemas existentes? (contabilidad, ERP, punto de venta físico)
53. ¿Quién dará mantenimiento post-lanzamiento: nosotros (iguala mensual) o su equipo?
54. Analítica: ¿GA4, Meta Pixel, TikTok Pixel desde el día 1? ¿Quién los configura?
55. ¿Expectativa de SEO desde el arranque? (migración de URLs si ya existe sitio, contenido inicial, sitemap)

## 10. Definición de éxito y siguientes pasos

56. ¿Cómo mediremos que el proyecto fue exitoso a 3 y 6 meses? (ventas, conversión, tráfico)
57. ¿Quién es el punto de contacto único para decisiones y aprobaciones? ¿Cadencia de revisiones (demo semanal/quincenal)?
58. ¿Quién entrega los insumos (fotos, textos, políticas) y en qué fechas? — el retraso de insumos es la causa #1 de retraso en ecommerce a la medida.

---

## Anexo A — Propuesta de stack nativo (para discusión interna)

| Capa | Opción sugerida | Alternativa |
|---|---|---|
| Frontend | Next.js (React) — SSR/ISR para SEO | Nuxt (Vue) |
| Estilos / UI | Tailwind CSS + design system propio | — |
| Backend / API | Node.js (NestJS o Next API routes) | Laravel |
| Base de datos | PostgreSQL | MySQL |
| Pagos | Stripe / Mercado Pago | Conekta |
| Imágenes | Cloudinary / S3 + CDN | — |
| Emails transaccionales | Resend / SendGrid | — |
| Hosting | Vercel + Neon/Supabase | VPS + Docker |

*Se define en firme después de las respuestas de las secciones 1, 9 y del presupuesto.*

## Anexo B — Entregables esperados de la fase de descubrimiento

- [ ] Minuta de kickoff con respuestas a este cuestionario
- [ ] Alcance MVP priorizado (MoSCoW) y roadmap de fases
- [ ] Wireframes de las vistas clave (home, catálogo, ficha de producto, carrito, checkout)
- [ ] Propuesta económica y cronograma
- [ ] Definición de stack y arquitectura
