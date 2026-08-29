# Catalonia Booking System

Sistema de reservas hoteleras todo-en-uno: wizard de reserva de 3 pasos, mapa interactivo, estudio de mercado, chatbot y dark mode. **Archivo único**: `index.html` autocontenido (sin build ni dependencias de servidor).

## Stack

- HTML5 + CSS3 (custom properties, dark mode con `color-scheme`)
- JavaScript ES6+ (vanilla, sin framework)
- Leaflet.js 1.9.4 (mapa de destinos, lazy-load con IntersectionObserver)
- GSAP 3.12.5 + ScrollTrigger (reveal on scroll, contadores, KPI bars)
- Three.js 0.160.0 (hero canvas, import dinámico con `prefers-reduced-motion` guard)
- Font Awesome 6.5.1
- Google Fonts: Inter + Playfair Display
- Todo por CDN (sin paquetes locales)

## Estructura del archivo

| Sección | Línea (aprox.) | Contenido |
|---|---|---|
| `<head>` | 1–360 | Meta/SEO (OG + Twitter), CDNs, estilos completos |
| Nav + hero | 362–411 | Menú fijo, selector ES/EN, toggle dark mode, canvas Three.js |
| Booking wizard | 414–488 | 3 pasos: destino/fechas → huéspedes/promo → confirmar |
| Stats | 491–506 | Contadores animados (hoteles, destinos, score) |
| Destinos | 509–524 | Tabs España/Europa/Caribe + mapa Leaflet |
| Estudio de mercado | 527–578 | KPIs animados, mapa competitivo, 6 tendencias, FODA, fuentes |
| Hoteles | 581–592 | Grid dinámico con filtros (Urbano/Resort/Adults Only) |
| Experiencias | 595–608 | Carrusel horizontal (scroll-snap) |
| Ofertas | 611–619 | 2 ofertas destacadas |
| Rewards | 622–624 | Programa de fidelización |
| Social proof | 627–637 | Testimonios Booking 8.5+ |
| CTA + footer | 640–657 | Cierre y footer con enlaces |
| Extras | 659–696 | Sticky bar, toasts, chatbot |
| JS app | 733–1365 | Fotos, i18n, pricing, wizard, mapa, hoteles, chat |

## Funcionalidades

- **Wizard 3 pasos** — validación de fechas, límites de huéspedes, códigos promo (`CARIBE15`, `DIRECT10`, `REWARDS5`, `BCN20`), disponibilidad simulada, resumen con desglose de precio.
- **Pricing engine** — precio según destino, habitaciones, huéspedes, temporada y descuentos.
- **Mapa Leaflet** — 14 marcadores con popups, lazy-load al hacer scroll.
- **i18n ES/EN** — diccionario `data-i18n`, persistencia en `localStorage`.
- **Dark mode** — toggle con persistencia.
- **Chatbot** — FAQ con keywords + free text.
- **Accesibilidad** — skip link, `aria-label`, `alt`, `role`, `prefers-reduced-motion`.
- **SEO** — meta description, Open Graph, Twitter Card, canonical.

## Uso

Abre `index.html` en cualquier navegador moderno. No requiere instalación ni build.

## CDNs verificados

```
Leaflet 1.9.4        unpkg.com/leaflet@1.9.4
GSAP 3.12.5          cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5
Font Awesome 6.5.1   cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1
Three.js 0.160.0     unpkg.com/three@0.160.0
Google Fonts         fonts.googleapis.com
```

## Licencia

MIT — Pedro Belentani 2026
