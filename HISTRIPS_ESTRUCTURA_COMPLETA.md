# HISTRIPS.COM - ANÁLISIS COMPLETO DE ESTRUCTURA

**Tema:** Broadcast V5.5.0 (Shopify)
**Archivo Analizado:** HiStrips_ Boost Performance & Live Healthier for Top Athletes.html (1.1MB)
**Fecha:** 2025-11-17

---

## 1. SECCIONES PRINCIPALES (en orden del body)

### 1.1 Header & Announcement Bar
- **Announcement Bar** (`sections--24785107222872__announcement`)
  - Fondo negro (#000000)
  - Texto blanco (#ffffff)
  - Slider con mensajes: "BLACK FRIDAY: 30% OFF + WIN 20,000$" y "30-day money-back guarantee"
  - Auto-rotate cada 7 segundos
  - Clase: `announcement__wrapper announcement__wrapper--top`

- **Header** (`sections--24785107222872__header`)
  - Logo centrado, menú izquierdo
  - Altura: 77px (desktop), 66px (medium), 60px (mobile)
  - Fondo: #ffffff
  - Clase: `header__wrapper`
  - Sticky header habilitado

### 1.2 Body Sections (Template)

#### Sección 1: Hero Principal
```
ID: section_hero_w7yQUA
Tipo: hero
Clases: index-hero wide-image
```
**Estructura:**
- Full-width hero image
- Enlace a `/collections/all`
- Imagen responsive (desktop: aspect-ratio 3.5, mobile: 1.27)
- Clases principales:
  - `hero__wrapper frame wrapper--full`
  - `hero__images frame__item`
  - `hero__split-image`

**HTML simplificado:**
```html
<div class="index-hero wide-image" data-section-type="hero">
  <div class="hero__wrapper frame wrapper--full">
    <a class="hero__images frame__item" href="/collections/all">
      <div class="hero__split-image">
        <div class="image__hero__frame image-height">
          <picture>
            <source media="(min-width: 750px)" srcset="[desktop]">
            <source media="(max-width: 749px)" srcset="[mobile]">
            <img src="[fallback]" loading="eager">
          </picture>
        </div>
      </div>
    </a>
  </div>
</div>
```

---

#### Sección 2: Logo Cloud - "WORN BY THE BEST"
```
ID: ss_scrolling_logo_cloud_iMiT9D
Tipo: Custom (Scrolling Logo Cloud)
```
**Características:**
- Título: "WORN BY THE BEST"
- Carousel infinito de logos
- Font: Archivo (600 weight)
- Tamaño de título: 21px
- Color título: #121212
- Slides width: 170px
- Dirección: horizontal (marquee)

**HTML simplificado:**
```html
<section id="ss-scrolling-logo-cloud" style="background: #fafafa;">
  <h2 class="scrolling-logo-cloud-title">WORN BY THE BEST</h2>
  <div class="scrolling-logo-cloud">
    <div class="marquee-horizontal">
      <div class="slide">
        <img src="[logo]" alt="[brand]">
      </div>
      <!-- Múltiples slides -->
    </div>
  </div>
</section>
```

---

#### Sección 3: Product Grid
```
ID: section_collection_bQj3kF
Tipo: product-grid
Clases: index-products section-padding
```
**Configuración Grid:**
- Desktop: 4 columnas (`--COLUMNS: 4`)
- Medium: 2 columnas (`--COLUMNS-MEDIUM: 2`)
- Mobile: 2 columnas (`--COLUMNS-MOBILE: 2`)
- Padding: 50px top/bottom

**Productos mostrados:**
1. Black Nasal Strips - €25,95 (antes €35,95)
2. Athlete's Favorite (Black Strips) - €43,95 (antes €59,95)
3. + otros productos

**HTML simplificado:**
```html
<section class="index-products section-padding" data-section-type="product-grid">
  <div class="grid-container wrapper">
    <div class="grid__items-holder">
      <div class="grid-outer">
        <div class="grid grid--mobile-vertical">

          <!-- Product Item -->
          <div class="grid-item product-item product-item--centered
                      product-item--outer-text product-item--has-quickbuy">

            <!-- Image -->
            <div class="product-item__image double__image">
              <a class="product-link" href="/products/[handle]">
                <div class="product-item__bg" data-product-image-default>
                  <figure class="image-wrapper lazy-image" style="--aspect-ratio: 1;">
                    <img src="[image]" loading="eager">
                  </figure>
                </div>
                <!-- Hover image -->
                <deferred-image class="product-item__bg__under">
                  <figure class="image-wrapper lazy-image">
                    <img src="[hover-image]" loading="lazy">
                  </figure>
                </deferred-image>
              </a>

              <!-- Quick Add -->
              <quick-add-product>
                <button class="quick-add__button caps">
                  <span class="btn__text">Quick add</span>
                  <span class="btn__plus"></span>
                </button>
              </quick-add-product>
            </div>

            <!-- Product Info -->
            <div class="product-information">
              <div class="product-item__info">
                <a class="product-link" href="/products/[handle]">
                  <p class="product-item__title">[Title]</p>
                  <div class="product-item__price">
                    <span class="price sale">
                      <span class="new-price">€25,95</span>
                      <span class="old-price">€35,95</span>
                    </span>
                  </div>
                </a>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</section>
```

---

#### Sección 4: Hero Section 2
```
ID: section_hero_4UhMak
Tipo: hero
```
Misma estructura que Hero Section 1

---

#### Sección 5: How it Works (Replo)
```
ID: replo_how_work_replo_jiCrmg
Tipo: Custom Replo Section
```
**Nota:** Contenido dinámico renderizado por Replo
- Sección explicativa de cómo funcionan los productos
- Renderizado client-side

---

#### Sección 6: Hero Section 3
```
ID: section_hero_3xdy8k
Tipo: hero
```
Tercera imagen hero full-width

---

#### Sección 7: Features (Custom)
```
ID: ss_feature_43_yxbm8a
Tipo: Custom Features Section
```
**Nota:** Sección custom para mostrar características del producto

---

#### Sección 8: Reviews/Testimonials (Replo)
```
ID: replo_reviews_section_JNggUd
Tipo: Custom Replo Section
```
**Nota:** Sección de testimonios y reseñas renderizada por Replo

---

#### Sección 9: Rich Text - "HiStrips Inside"
```
ID: section_rich_text_GNQx6b
Tipo: rich-text
Clases: index-rte section-padding
```
**Contenido:**
- Título: "HiStrips Inside" (heading-size-8)
- Texto: "More than just a simple bandaid. Designed with the strongest physical action layer and stickiest hypoallergenic adhesive in the market for maximum durability & comfort."
- Text-align: center
- Padding bottom: 0px

**HTML simplificado:**
```html
<section class="index-rte section-padding" data-section-type="rich-text">
  <div class="hero__content__wrapper text-center wrapper">
    <div class="hero__content hero__content--compact">
      <h2 class="hero__title heading-size-8 block-padding"
          data-aos="hero"
          style="--block-padding-bottom:16px;">
        HiStrips Inside
      </h2>
      <div class="hero__rte body-size-3 font-body block-padding"
           data-aos="hero"
           style="--block-padding-bottom:26px;">
        <p>[Contenido]</p>
      </div>
    </div>
  </div>
</section>
```

---

#### Sección 10: Before/After Image
```
ID: ss_before_after_image_xiHmcF
Tipo: Custom Before/After Comparison
```
**Nota:** Comparador de imágenes antes/después

---

## 2. VARIABLES CSS - COLORES

### 2.1 Paleta Principal
```css
:root {
  /* === Colores de Fondo === */
  --COLOR-BG: #fafafa;
  --COLOR-BG-BRIGHTER: #ededed;
  --COLOR-BG-SECONDARY: #f7f9fa;
  --COLOR-BG-SECONDARY-LIGHTEN: #ffffff;
  --COLOR-BG-TRANSPARENT: rgba(250, 250, 250, 0);
  --COLOR-BG-ALPHA-25: rgba(250, 250, 250, 0.25);
  --COLOR-BG-RGB: 250, 250, 250;
  --COLOR-VIDEO-BG: #ededed;

  /* === Colores de Texto === */
  --COLOR-TEXT: #000000;
  --COLOR-TEXT-DARK: #000000;
  --COLOR-TEXT-LIGHT: #4b4b4b;

  /* === Color Primario === */
  --COLOR-PRIMARY: #696969;
  --COLOR-PRIMARY-HOVER: #4a3c3c;
  --COLOR-PRIMARY-FADE: rgba(105, 105, 105, 0.05);
  --COLOR-PRIMARY-FADE-HOVER: rgba(105, 105, 105, 0.1);
  --COLOR-PRIMARY-LIGHT: #c4a7a7;
  --COLOR-PRIMARY-OPPOSITE: #ffffff;

  /* === Colores de Enlaces === */
  --COLOR-LINK: #494949;
  --COLOR-LINK-HOVER: rgba(73, 73, 73, 0.7);
  --COLOR-LINK-FADE: rgba(73, 73, 73, 0.05);
  --COLOR-LINK-FADE-HOVER: rgba(73, 73, 73, 0.1);
  --COLOR-LINK-OPPOSITE: #ffffff;

  /* === Colores de Bordes === */
  --COLOR-BORDER: rgb(240, 240, 240);
  --COLOR-BORDER-LIGHT: #f4f4f4;
  --COLOR-BORDER-HAIRLINE: #f2f2f2;
  --COLOR-BORDER-DARK: #bdbdbd;

  /* === Colores de Sale/Descuento === */
  --COLOR-SALE-BG: #ff0000;
  --COLOR-SALE-TEXT: #ffffff;
  --COLOR-SALE-TEXT-SECONDARY: #ff0000;
  --COLOR-SALE: #7a0000;

  /* === Colores de Badges === */
  --COLOR-BADGE-BG: #444444;
  --COLOR-BADGE-TEXT: #ffffff;

  /* === Colores de Error === */
  --COLOR-ERROR: #721C24;
  --COLOR-ERROR-BG: #F8D7DA;
  --COLOR-ERROR-BORDER: #F5C6CB;
}
```

### 2.2 Tonos de Gris con Opacidad
```css
:root {
  --COLOR-A5:  rgba(0, 0, 0, 0.05);
  --COLOR-A10: rgba(0, 0, 0, 0.1);
  --COLOR-A15: rgba(0, 0, 0, 0.15);
  --COLOR-A20: rgba(0, 0, 0, 0.2);
  --COLOR-A25: rgba(0, 0, 0, 0.25);
  --COLOR-A30: rgba(0, 0, 0, 0.3);
  --COLOR-A35: rgba(0, 0, 0, 0.35);
  --COLOR-A40: rgba(0, 0, 0, 0.4);
  --COLOR-A45: rgba(0, 0, 0, 0.45);
  --COLOR-A50: rgba(0, 0, 0, 0.5);
  --COLOR-A55: rgba(0, 0, 0, 0.55);
  --COLOR-A60: rgba(0, 0, 0, 0.6);
  --COLOR-A65: rgba(0, 0, 0, 0.65);
  --COLOR-A70: rgba(0, 0, 0, 0.7);
  --COLOR-A75: rgba(0, 0, 0, 0.75);
  --COLOR-A80: rgba(0, 0, 0, 0.8);
  --COLOR-A85: rgba(0, 0, 0, 0.85);
  --COLOR-A90: rgba(0, 0, 0, 0.9);
  --COLOR-A95: rgba(0, 0, 0, 0.95);
}
```

### 2.3 Colores de Header
```css
:root {
  --COLOR-HEADER-BG: #ffffff;
  --COLOR-HEADER-BG-TRANSPARENT: rgba(255, 255, 255, 0);
  --COLOR-HEADER-LINK: #2e2e2e;
  --COLOR-HEADER-LINK-HOVER: rgba(46, 46, 46, 0.7);
}
```

### 2.4 Colores de Menú
```css
:root {
  --COLOR-MENU-BG: #ffffff;
  --COLOR-MENU-LINK: #2e2e2e;
  --COLOR-MENU-LINK-HOVER: rgba(46, 46, 46, 0.7);
}
```

### 2.5 Otros
```css
:root {
  --RADIUS: 300px;
  --RADIUS-SELECT: 22px;

  --HEADER-HEIGHT: 77px;
  --HEADER-HEIGHT-MEDIUM: 66.0px;
  --HEADER-HEIGHT-MOBILE: 60.0px;
}
```

---

## 3. TIPOGRAFÍA

### 3.1 Familia Principal: HelveticaNowDisplay
**Archivos font-face:**
```css
@font-face {
  font-family: 'HelveticaNowDisplay';
  src: url('HelveticaNowDisplay-Light.ttf') format('truetype');
  font-weight: 300;
  font-style: normal;
}

@font-face {
  font-family: 'HelveticaNowDisplay';
  src: url('HelveticaNowDisplay-Regular.ttf') format('truetype');
  font-weight: 400;
  font-style: normal;
}

@font-face {
  font-family: 'HelveticaNowDisplay';
  src: url('HelveticaNowDisplay-Medium.ttf') format('truetype');
  font-weight: 500;
  font-style: normal;
}

@font-face {
  font-family: 'HelveticaNowDisplay';
  src: url('HelveticaNowDisplay-Bold.ttf') format('truetype');
  font-weight: 700;
  font-style: normal;
}

@font-face {
  font-family: 'HelveticaNowDisplay';
  src: url('HelveticaNowDisplay-ExtraBold.ttf') format('truetype');
  font-weight: 800;
  font-style: normal;
}

@font-face {
  font-family: 'HelveticaNowDisplay';
  src: url('HelveticaNowDisplay-Black.ttf') format('truetype');
  font-weight: 900;
  font-style: normal;
}
```

### 3.2 Familias Secundarias
- **Avenir Next** - Usado en elementos específicos
- **GTWalsheimPro** - Alternativa
- **GTStandard-M** - Alternativa
- **Archivo** (600 weight) - Específico para Logo Cloud section
- **Poppins** - Elementos específicos

---

## 4. CLASES CSS CLAVE

### 4.1 Clases de Layout
```
wrapper                    # Contenedor principal con max-width
wrapper--full             # Full width wrapper
section-padding           # Padding estándar de sección
grid-container            # Contenedor de grid
grid__items-holder        # Holder de items del grid
grid-outer                # Grid exterior
grid                      # Grid principal
grid--mobile-vertical     # Grid vertical en mobile
```

### 4.2 Clases de Hero
```
index-hero                # Hero principal
wide-image                # Imagen wide
hero__wrapper             # Wrapper del hero
hero__images              # Contenedor de imágenes
hero__split-image         # Imagen split
hero__content             # Contenido del hero
hero__content--compact    # Contenido compacto
hero__title               # Título del hero
hero__rte                 # Rich text del hero
```

### 4.3 Clases de Producto
```
grid-item                 # Item del grid
product-item              # Item de producto
product-item--centered    # Producto centrado
product-item--outer-text  # Texto exterior
product-item--has-quickbuy # Con quick buy
product-item__image       # Imagen del producto
double__image             # Imagen doble (hover)
product-item__bg          # Background de imagen
product-link              # Link del producto
product-item__title       # Título del producto
product-item__price       # Precio del producto
quick-add__button         # Botón quick add
```

### 4.4 Clases de Tipografía
```
heading-size-8            # Tamaño de heading
body-size-2               # Tamaño body 2
body-size-3               # Tamaño body 3
font-body                 # Font family body
block-padding             # Padding de bloque
text-center               # Texto centrado
```

### 4.5 Clases de Imagen
```
image-wrapper             # Wrapper de imagen
image-wrapper--cover      # Cover mode
lazy-image                # Lazy loading
lazy-image--backfill      # Con backfill
```

### 4.6 Clases de Precio
```
price                     # Precio base
price sale                # Precio en oferta
new-price                 # Precio nuevo
old-price                 # Precio anterior
```

---

## 5. ANIMACIONES

### 5.1 AOS (Animate On Scroll)
```html
data-aos="hero"
data-aos="img-in"
data-aos-delay="[ms]"
data-aos-duration="800"
data-aos-anchor="#[section-id]"
data-aos-easing="ease-out-quart"
data-aos-order="[number]"
```

**Valores comunes:**
- Duration: 800ms
- Easing: ease-out-quart
- Delays: 0, 100ms (para stagger)

---

## 6. COMPONENTES CUSTOM

### 6.1 Announcement Bar
```html
<announcement-bar class="announcement__bar-outer">
  <div class="announcement__bar-holder announcement__bar-holder--slider">
    <div class="announcement__slider flickity-enabled">
      <ticker-bar class="announcement__slide announcement__bar">
        <div class="announcement__message">
          <div class="announcement__text">
            <div class="body-size-2">
              <p><strong>[Mensaje]</strong></p>
            </div>
          </div>
        </div>
      </ticker-bar>
    </div>
  </div>
</announcement-bar>
```

### 6.2 Quick Add Product
```html
<quick-add-product>
  <div class="quick-add__holder" data-quick-add-holder="[product-id]">
    <form method="post" action="/cart/add">
      <input type="hidden" name="id" value="[variant-id]">
      <button class="quick-add__button caps" type="submit">
        <span class="btn__text">Quick add</span>
        <span class="btn__plus"></span>
        <span class="btn__added">&nbsp;</span>
        <span class="btn__loader">
          <svg height="18" width="18" class="svg-loader">
            <circle r="7" cx="9" cy="9"></circle>
            <circle stroke-dasharray="87.96..." r="7" cx="9" cy="9"></circle>
          </svg>
        </span>
        <span class="btn__error">&nbsp;</span>
      </button>
    </form>
  </div>
</quick-add-product>
```

### 6.3 Deferred Image (Hover effect)
```html
<deferred-image class="product-item__bg__under">
  <template></template>
  <figure class="image-wrapper lazy-image" style="--aspect-ratio: 1;">
    <img src="[hover-image]" loading="lazy">
  </figure>
</deferred-image>
```

---

## 7. RESPONSIVE BREAKPOINTS

```css
/* Desktop */
@media (min-width: 750px) { }

/* Medium */
@media screen and (min-width: 768px) { }

/* Mobile */
@media (max-width: 749px) { }

/* Mobile specific */
@media (min-width: 480px) { }
```

---

## 8. ASPECTOS TÉCNICOS

### 8.1 Lazy Loading
- Imágenes con `loading="lazy"` para imágenes no críticas
- `loading="eager"` para imágenes above-the-fold
- Clase `lazy-image` con `lazy-image--backfill`

### 8.2 Responsive Images
```html
<picture>
  <source media="(min-width: 750px)"
          sizes="100vw"
          srcset="[img]?width=180 180w, [img]?width=360 360w, ...">
  <source media="(max-width: 749px)"
          sizes="100vw"
          srcset="[img-mobile]?width=180 180w, ...">
  <img src="[fallback]" width="[w]" height="[h]">
</picture>
```

### 8.3 CSS Variables Dinámicas
```css
style="
  --aspect-ratio: 1;
  --PT: 50px;
  --PB: 50px;
  --COLUMNS: 4;
  --COLUMNS-MEDIUM: 2;
  --COLUMNS-MOBILE: 2;
  --block-padding-bottom: 16px;
"
```

---

## 9. SCRIPTS Y LIBRERÍAS

### 9.1 JavaScript Principal
```
vendor.js       # Librerías vendor
theme.js        # Script principal del tema
custom-js.js    # Scripts custom
custom.js       # Scripts adicionales custom
```

### 9.2 Librerías Externas
```
Flickity        # Carousels/sliders
Swiper          # Alternative slider
AOS             # Animate On Scroll
Replo           # Page builder
```

### 9.3 Apps de Shopify
- Loox (reviews)
- UpCart (cart drawer)
- Google Analytics
- Facebook Pixel
- Microsoft Clarity

---

## 10. RESUMEN PARA RECREACIÓN EN LIQUID

### 10.1 Archivos Liquid Necesarios

**Secciones:**
```
sections/
  ├── announcement.liquid
  ├── header.liquid
  ├── hero.liquid (reutilizable 3x)
  ├── scrolling-logo-cloud.liquid
  ├── product-grid.liquid
  ├── rich-text.liquid
  ├── before-after-image.liquid
  └── custom-features.liquid
```

**Snippets:**
```
snippets/
  ├── product-card.liquid
  ├── quick-add.liquid
  ├── deferred-image.liquid
  ├── responsive-image.liquid
  └── price.liquid
```

### 10.2 Settings Schema
```json
{
  "name": "Theme Settings",
  "settings": [
    {
      "type": "header",
      "content": "Colors"
    },
    {
      "type": "color",
      "id": "color_bg",
      "label": "Background",
      "default": "#fafafa"
    },
    {
      "type": "color",
      "id": "color_text",
      "label": "Text",
      "default": "#000000"
    },
    {
      "type": "color",
      "id": "color_primary",
      "label": "Primary",
      "default": "#696969"
    }
  ]
}
```

### 10.3 Orden de Implementación Recomendado
1. Setup CSS variables en `theme.liquid`
2. Crear `header.liquid` y `announcement.liquid`
3. Implementar `hero.liquid` section
4. Crear `product-card.liquid` snippet
5. Implementar `product-grid.liquid` section
6. Crear `scrolling-logo-cloud.liquid`
7. Implementar `rich-text.liquid`
8. Añadir animaciones AOS
9. Implementar Quick Add functionality
10. Testing responsive en todos los breakpoints

---

## 11. NOTAS IMPORTANTES

1. **Replo Sections:** Las secciones `replo_how_work` y `replo_reviews` son dinámicas y se renderizan client-side. Para recrear, necesitarás crear secciones Liquid equivalentes manualmente.

2. **Custom Sections:** Las secciones `ss_feature_43` y `ss_before_after_image` son secciones custom que requieren implementación específica.

3. **Tema Broadcast:** Este análisis está basado en el tema Broadcast V5.5.0. La estructura es característica de este tema premium de Shopify.

4. **Optimización de Imágenes:** Todas las imágenes usan srcset con múltiples tamaños (180w, 360w, 540w, 720w, etc.) para optimización.

5. **Font Loading:** Las fuentes se cargan con `font-display: swap` para mejor performance.

---

**Fin del Análisis**
