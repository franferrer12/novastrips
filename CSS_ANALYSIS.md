# Análisis Completo del CSS - HiStrips Theme

**Archivo:** `/Users/franferrer/novastrips-analysis/assets/histrips-complete.css`
**Tamaño:** 462KB
**Tema Base:** Broadcast Theme by Invisible Themes
**Fecha de análisis:** 2025-11-17

---

## 1. RESUMEN EJECUTIVO

El tema HiStrips utiliza el framework Broadcast Theme, un tema profesional para Shopify con un sistema de diseño robusto basado en:
- Variables CSS (CSS Custom Properties) para personalización
- Sistema responsive con breakpoints estratégicos
- 43 animaciones CSS personalizadas
- Arquitectura modular y escalable

---

## 2. VARIABLES CSS (CSS CUSTOM PROPERTIES)

### 2.1 Variables Principales (69 variables identificadas)

#### Colores
```css
--bg: var(--COLOR-BG)
--bg-accent: var(--COLOR-BG-SECONDARY)
--bg-accent-lighten: var(--COLOR-BG-SECONDARY-LIGHTEN)
--text-dark: var(--COLOR-TEXT-DARK)
--text: var(--COLOR-TEXT)
--text-light: var(--COLOR-TEXT-LIGHT)
--text-a35: var(--COLOR-A35)
--text-a70: var(--COLOR-A70)
--text-a75: var(--COLOR-A75)
--text-black: #000
--text-white: #FFF
--link: var(--COLOR-LINK)
--link-hover: var(--COLOR-LINK-HOVER)
--border: var(--COLOR-BORDER)
--hairline: var(--COLOR-BORDER-HAIRLINE)
--primary: var(--COLOR-PRIMARY)
--primary-hover: var(--COLOR-PRIMARY-HOVER)
--primary-fade: var(--COLOR-PRIMARY-FADE)
--primary-light: var(--COLOR-PRIMARY-LIGHT)
--primary-opposite: var(--COLOR-PRIMARY-OPPOSITE)
--contrast: #000
--error: var(--COLOR-ERROR)
--error-bg: var(--COLOR-ERROR-BG)
--success: #56AD6A
--success-bg: rgba(86, 173, 106, .2)
--sale-bg: var(--COLOR-SALE-BG)
--sale-text: var(--COLOR-SALE-TEXT)
--sale-text-secondary: var(--COLOR-SALE-TEXT-SECONDARY)
```

#### Tipografía (Sistema de escala modular)
```css
--base: 16px
--font-2: 12px
--font-3: 14px
--font-4: 16px
--font-5: 19px
--font-6: 23px
--font-7: 27px
--font-8: 32px
--font-9: 37px
--font-10: 40px
--font-11: 43px
--font-12: 47px
--font-13: 50px
--font-14: 52px
--font-15: 55px
```

#### Layout & Spacing
```css
--gutter: var(--LAYOUT-GUTTER)
--gutter-offset: calc(var(--gutter) * -1)
--outer: var(--LAYOUT-OUTER)
--outer-offset: calc(var(--outer) * -1)
--gap: var(--gutter)
--inner: 20px
--line: 1rem
--line-offset: calc(var(--line) * -1)
--content-max: 1100px
--content-full: 90vh
--full-height: 100vh
--full-screen: var(--full-height)
--one-half: 50vh
--one-third: 33vh
```

#### Header & Navigation
```css
--header-height: 80px
--header-sticky-height: 0px
--announcement-height: 0px
--footer-height: 500px
```

#### Componentes
```css
--btn-radius: 10px
--btn-top: 11px
--form-left: 12px
--form-top: 10px
--form-margin: 32px
```

---

## 3. BREAKPOINTS RESPONSIVE

### 3.1 Media Queries Principales

| Breakpoint | Query | Uso | Frecuencia |
|------------|-------|-----|------------|
| **Mobile** | `max-width: 749px` | Dispositivos móviles | 229x |
| **Tablet** | `min-width: 750px` | Tablets y superiores | 167x |
| **Desktop Small** | `min-width: 750px and max-width: 989px` | Tablets landscape | 21x |
| **Desktop** | `min-width: 990px` | Escritorio estándar | 24x |
| **Desktop Large** | `min-width: 1400px` | Pantallas grandes | 6x |
| **Extra Small** | `max-width: 479px` | Móviles pequeños | 23x |
| **Hover Support** | `hover: hover` | Dispositivos con hover | 38x |

### 3.2 Breakpoints Específicos
```css
/* Mobile muy pequeño */
@media only screen and (max-width: 420px)

/* Mobile estándar */
@media only screen and (max-width: 479px)

/* Hasta tablet */
@media only screen and (max-width: 749px)

/* Tablet hasta desktop pequeño */
@media only screen and (max-width: 989px)

/* Desde tablet */
@media only screen and (min-width: 750px)

/* Desktop pequeño */
@media only screen and (min-width: 990px)

/* Desktop grande */
@media only screen and (min-width: 1400px)

/* Hover capaz */
@media (hover: hover)

/* Touch devices */
@media (hover: none) and (pointer: coarse)
```

---

## 4. CLASES CSS POR CATEGORÍA

### 4.1 Layout & Containers (15 clases)

```css
.container
.wrapper
.wrapper--full
.wrapper--full-padded
.wrapper--narrow
.section-padding
.section-sidebar
.section-sidebar__aside
.section-sidebar__body
.section-sidebar__content
.section-sidebar__title
.section-sidebar__widget
.section-before-after
.section-columns
.section-countdown
```

**Uso:** Estructuras principales de página, contenedores y secciones.

---

### 4.2 Header & Navegación (47 clases)

#### Header Principal
```css
.header__backfill
.header__desktop
.header__desktop__bar__c
.header__desktop__bar__l
.header__desktop__bar__r
.header__desktop__buttons
.header__desktop__buttons--icons
.header__desktop__buttons--text
.header__desktop__lower
.header__desktop__upper
.header__mobile
.header__mobile__bottom
.header__mobile__button
.header__mobile__button--desktop
.header__mobile__hamburger
.header__mobile__menu
.header__mobile__search
.header__mobile__top
```

#### Logo
```css
.header-logo
.header__logo
.header__logo__link
.header__logo__text
.header__logo__text--break
.header__logo__text--long
```

#### Menú y Navegación
```css
.header__menu
.header__dropdown
.header__dropdown__image
.header__dropdown__inner
.header__dropdown__wrapper
.header__grandparent__links
.navigation
.navlink
.navlink--button
.navlink--grandparent
.navlink--parent
.navlink--toplevel
.navmenu
.navmenu__button
.navmenu__item
.navmenu__link
.navtext
.navtext--child
.navtext--parent
```

#### Cart Header
```css
.header__cart__status
.header__cart__status__holder
```

**Uso:** Sistema completo de navegación con soporte para menús multinivel, dropdown con imágenes y estados activos.

---

### 4.3 Hero & Slideshow (36 clases)

```css
.hero__bg
.hero__button
.hero__button-group
.hero__collections
.hero__content
.hero__content--compact
.hero__content--no-padding
.hero__content--transparent
.hero__content__wrapper
.hero__image
.hero__media
.hero__rte
.hero__slide
.hero__split-image
.hero__subheading
.hero__video

.slideshow
.slideshow__slide
.slideshow__slide--onboarding

.slider__arrows
.slider__button
.slider__button--next
.slider__button--prev

.sliderow
.sliderow--back
.sliderow__back-button
.sliderow__links
.sliderow__title
.sliderow__title--highlight
.sliderow__title--secondary

.sliderule__chevron--left
.sliderule__chevron--right
.sliderule__panel
.sliderule__wrapper
.sliderule__wrapper--secondary
```

**Uso:** Banners hero, slideshows de imágenes, carousels de productos con controles de navegación.

---

### 4.4 Product Grid & Collections (186+ clases)

#### Grid System
```css
.grid
.grid--1
.grid--2
.grid--3
.grid--account
.grid--article
.grid--mobile-slider
.grid--sidebar
.grid--uniform
.grid-item
.grid-overflow-wrapper
.grid-product
.grid-product__content
.grid-product__image
.grid-product__image-mask
.grid-product__link
.grid-product__meta
.grid-product__price
.grid-product__tag
.grid-product__title
.grid-product__vendor
```

#### Product Cards
```css
.product-grid-item
.product-item
.product-item__badge
.product-item__bg
.product-item__cutline
.product-item__header
.product-item__hover
.product-item__image
.product-item__image-container
.product-item__info
.product-item__link
.product-item__price
.product-item__swatch
.product-item__title
.product-item__vendor
```

#### Product Page
```css
.product__block
.product__content
.product__form
.product__form-wrapper
.product__gallery
.product__header
.product__images
.product__info
.product__media
.product__media-container
.product__media-item
.product__meta
.product__price
.product__quantity
.product__section
.product__slide
.product__submit
.product__swatches
.product__thumb
.product__title
.product__upsell
.product__vendor
```

#### Collections
```css
.collection-block
.collection-block__button
.collection-block__content
.collection-block__image
.collection-block__image-bg
.collection-block__products
.collection-block__wrapper

.collection-item
.collection-item--transparent
.collection-item__content
.collection-item__image
.collection-item__info

.collection__active__filters
.collection__filters
.collection__filters__btn
.collection__image
.collection__image-inline
.collection__nav
.collection__nav--both
.collection__nav--filter
.collection__nav--sort
.collection__products
.collection__sidebar
.collection__sidebar__actions
.collection__sidebar__buttons
.collection__sidebar__close
.collection__sidebar__head
.collection__sidebar__link
.collection__sidebar__slide-out
.collection__sidebar__slider
.collection__title--no-image
.collection__title-wrapper
```

**Uso:** Sistema completo de visualización de productos con grids responsivas, filtros, ordenamiento y vistas detalladas.

---

### 4.5 Buttons & CTAs (23 clases)

```css
.btn                    /* Botón base */
.btn--primary           /* Botón primario (implícito) */
.btn--secondary         /* Botón secundario */
.btn--outline           /* Botón con borde */
.btn--text              /* Botón de texto */
.btn--white             /* Botón blanco */
.btn--black             /* Botón negro */
.btn--large             /* Botón grande */
.btn--small             /* Botón pequeño */
.btn--full              /* Ancho completo */
.btn--half              /* Medio ancho */
.btn--arrow             /* Con flecha */
.btn--ar                /* Aspect ratio */
.btn--scroll-top        /* Scroll to top */

/* Estados y componentes internos */
.btn__inner
.btn__outer
.btn__text
.btn__loader
.btn__loading
.btn__added
.btn__error
.btn__plus

/* Especializados */
.btn-full
.btn-size-chart
```

**Características:**
- Radio de borde: `--btn-radius: 10px`
- Sistema de estados (loading, added, error)
- Variantes de tamaño y color
- Soporte para iconos y flechas

---

### 4.6 Typography Classes

```css
/* Headings */
h1, .h1
h2, .h2
h3, .h3
h4, .h4
h5, .h5
h6, .h6
.heading

/* Font Families */
--FONT-STACK-BODY: var(...)
--FONT-STACK-HEADING: var(...)
--FONT-STACK-SUBHEADING: var(...)
--FONT-STACK-NAV: var(...)
--BTN-FONT-STACK: var(...)

/* Fuentes utilizadas */
- Helvetica Now Display, sans-serif
- Inter
- Enter, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, sans-serif
```

**Sistema de tamaños:** 15 niveles (font-2 a font-15) con escala modular desde 12px hasta 55px.

---

## 5. ANIMACIONES Y KEYFRAMES (43 animaciones)

### 5.1 Fade Animations
```css
@keyframes fadeIn
@keyframes fadeInUp
@keyframes fadeOut
@keyframes fadeOutDown
@keyframes fadein
@keyframes fakeFade
@keyframes heroFade
@keyframes imageFadeIn
@keyframes imageFadeOut
```

### 5.2 Slide Animations
```css
@keyframes slideInLeft
@keyframes slideInRight
@keyframes slideInUp
@keyframes slideOutDown
@keyframes slideOutLeft
@keyframes slideOutRight
@keyframes slideToggle
@keyframes slideUp
@keyframes slideup
@keyframes container-slide
```

### 5.3 Cart Animations
```css
@keyframes cartDrawerItemsFadeIn
@keyframes cartDrawerItemsFadeInLeft
@keyframes cartDrawerItemsFadeInRight
@keyframes cartDrawerItemsFadeOut
@keyframes cartDrawerItemsFadeOutLeft
@keyframes cartDrawerItemsFadeOutRight
@keyframes cartItemRemoved
@keyframes cartItemsFadeIn
```

### 5.4 UI & Utility Animations
```css
@keyframes animate-svg
@keyframes clipPathFromRight
@keyframes dash
@keyframes indeterminate
@keyframes indeterminate-short
@keyframes popup
@keyframes pulseDot
@keyframes pulseDotHover
@keyframes shimmer
@keyframes showMessage
@keyframes ticker-ltr
@keyframes ticker-rtl
@keyframes tooltip-opacity
@keyframes tooltip-top
@keyframes translateDown
@keyframes translateUp
```

**Uso:** Transiciones suaves, efectos de carga, animaciones de carrito, tooltips y efectos visuales.

---

## 6. PATRONES DE DISEÑO IDENTIFICADOS

### 6.1 Arquitectura BEM
El tema utiliza la metodología BEM (Block Element Modifier):
```css
/* Block */
.product

/* Element */
.product__title
.product__price
.product__image

/* Modifier */
.product--featured
.product--sold-out
```

### 6.2 Sistema de Utilidades
```css
/* Paletas de color */
.palette--contrast
.palette--primary
.palette--contrast--dark

/* Espaciado */
.section-padding

/* Responsive utilities */
.mobile-only
.desktop-only
```

### 6.3 Componentes Modulares
- **Header:** Desktop/Mobile separados con componentes reutilizables
- **Grid System:** Flexible con variantes (1-6 columnas)
- **Cards:** Sistema unificado para productos/colecciones
- **Forms:** Componentes consistentes de formularios

### 6.4 Sistema de Carrusel (Flickity)
```css
.flickity-enabled
.flickity-viewport
.flickity-slider
.flickity-cell
.flickity-button
.flickity-prev-next-button
```

### 6.5 Mobile-First Approach
Las media queries priorizan mobile (`max-width: 749px`) con 229 ocurrencias, indicando un enfoque mobile-first.

---

## 7. CUSTOMIZACIONES ESPECÍFICAS HISTRIPS

### 7.1 Product Page Custom
```css
.template-product h1.product__title {
  font-weight: 700;
  font-size: 36px;
  line-height: 120%;
  letter-spacing: -1px;
  vertical-align: middle;
  text-transform: uppercase;
}
```

### 7.2 Alert Boxes
```css
.red_part_pdp {
  display: flex;
  align-items: flex-start;
  border: 3px dashed #A40001;
  background-color: #ffdce2;
  gap: 10px;
  border-radius: 7px;
  padding: 10px;
  border-width: 1px;
  border-style: dashed;
}

.red_part_pdp h4 {
  font-size: 13px;
  font-weight: 700;
  color: #a50000;
  margin-bottom: 5px;
}
```

### 7.3 Mobile Back Navigation
```css
.mobe_back {
  display: flex;
  justify-content: center;
  gap: 5px;
  align-items: center;
}

.mobe_back img {
  width: 14px;
  height: 14px;
  line-height: 14px;
}
```

### 7.4 Product Upsell Swiper
```css
.upsell-swiper .product-upsell {
  justify-content: center;
  align-items: center;
  border-radius: 10px;
}

.upsell-swiper .product-upsell__btn {
  width: 100%;
  background-color: #1e1e1e;
  color: #fff;
}

.upsell-swiper .product-upsell__title {
  font-size: 15px;
  font-weight: 700;
  color: #151718;
  line-height: 15px;
  margin-bottom: 0;
}
```

### 7.5 Product Thumbnails
```css
.product__thumb.is-active img {
  border: 1px solid #BDBDBD;
  border-radius: 3px;
}
```

---

## 8. RECOMENDACIONES PARA SHOPIFY

### 8.1 Variables a Personalizar
Para adaptar el tema a NovaStrips, enfócate en estas variables:

```css
:root {
  /* Colores principales */
  --COLOR-PRIMARY: #TU_COLOR_PRIMARIO;
  --COLOR-PRIMARY-HOVER: #TU_COLOR_HOVER;
  --COLOR-BG: #TU_COLOR_FONDO;
  --COLOR-TEXT: #TU_COLOR_TEXTO;

  /* Tipografía */
  --FONT-STACK-HEADING: 'Tu fuente heading', sans-serif;
  --FONT-STACK-BODY: 'Tu fuente body', sans-serif;

  /* Layout */
  --content-max: 1100px; /* Ancho máximo del contenido */
  --header-height: 80px;
  --btn-radius: 10px;
}
```

### 8.2 Clases Críticas para E-commerce
```css
/* Product Grid */
.grid-product
.product-item
.product-item__image
.product-item__price

/* Product Page */
.product__title
.product__price
.product__form
.product__submit

/* Buttons */
.btn
.btn--primary
.btn--outline

/* Cart */
.cart-drawer
.cart-item
```

### 8.3 Optimizaciones Sugeridas
1. **Lazy Loading:** Aplicar a `.product-item__image`, `.hero__image`
2. **Critical CSS:** Extraer estilos de header, hero y above-the-fold
3. **Purge CSS:** Eliminar clases no utilizadas (puede reducir 30-40%)
4. **Minificación adicional:** El archivo ya está minificado pero se puede comprimir con Brotli

---

## 9. ESTRUCTURA DE ARCHIVOS RECOMENDADA

Para uso en Shopify, organizar así:

```
theme/
├── assets/
│   ├── histrips-complete.css (462KB - archivo completo)
│   ├── critical.css (extraer <15KB para inline)
│   ├── variables.css (solo variables)
│   └── components/
│       ├── buttons.css
│       ├── header.css
│       ├── product-grid.css
│       └── animations.css
├── sections/
│   └── (Liquid templates que usen las clases)
└── snippets/
    └── (Componentes reutilizables)
```

---

## 10. COMPATIBILIDAD

### 10.1 Navegadores Soportados
- Chrome/Edge (moderno)
- Firefox
- Safari (iOS/macOS)
- Mobile browsers (iOS Safari, Chrome Mobile)

### 10.2 Features Modernas Utilizadas
- CSS Grid
- CSS Flexbox
- CSS Custom Properties (variables)
- CSS Calc()
- CSS Animations/Keyframes
- CSS Transforms
- Media Queries Level 4 (`hover: hover`)

---

## 11. RESUMEN DE NÚMEROS

| Métrica | Valor |
|---------|-------|
| **Tamaño total** | 462KB |
| **Variables CSS** | 69 |
| **Media Queries** | 18 únicos |
| **Animaciones** | 43 keyframes |
| **Clases Header** | 47 |
| **Clases Hero** | 36 |
| **Clases Product** | 186+ |
| **Clases Button** | 23 |
| **Clases Layout** | 15 |
| **Breakpoint principal** | 750px |

---

## 12. PRÓXIMOS PASOS

1. **Auditoría de uso:** Identificar qué clases se usan realmente en el sitio
2. **Customización:** Ajustar variables CSS para branding de NovaStrips
3. **Optimización:** Eliminar clases no utilizadas
4. **Testing:** Verificar responsive en todos los breakpoints
5. **Performance:** Implementar critical CSS y lazy loading

---

**Documento generado:** 2025-11-17
**Analista:** Claude Code
**Archivo fuente:** `/Users/franferrer/Downloads/HiStrips_ Boost Performance & Live Healthier for Top Athletes_files/theme.css`
**Archivo completo guardado en:** `/Users/franferrer/novastrips-analysis/assets/histrips-complete.css`
