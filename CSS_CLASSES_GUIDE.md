# Guía de Clases CSS - HiStrips Theme

Esta guía proporciona una referencia rápida de las clases CSS más importantes del tema HiStrips, organizadas por caso de uso.

---

## LAYOUT & ESTRUCTURA

### Containers Principales
```html
<!-- Wrapper principal (máximo ancho) -->
<div class="wrapper">...</div>

<!-- Wrapper ancho completo -->
<div class="wrapper--full">...</div>

<!-- Wrapper ancho completo con padding -->
<div class="wrapper--full-padded">...</div>

<!-- Wrapper estrecho (contenido centrado) -->
<div class="wrapper--narrow">...</div>

<!-- Container genérico -->
<div class="container">...</div>
```

### Secciones
```html
<!-- Sección con padding estándar -->
<section class="section-padding">...</section>

<!-- Sección con sidebar -->
<div class="section-sidebar">
  <div class="section-sidebar__body">...</div>
  <aside class="section-sidebar__aside">...</aside>
</div>
```

---

## HEADER & NAVEGACIÓN

### Header Desktop
```html
<header class="header__desktop">
  <div class="header__desktop__upper">
    <div class="header__desktop__bar__l">Logo</div>
    <div class="header__desktop__bar__c">Navegación</div>
    <div class="header__desktop__bar__r">Acciones</div>
  </div>
  <div class="header__desktop__lower">Menú secundario</div>
</header>
```

### Header Mobile
```html
<header class="header__mobile">
  <div class="header__mobile__top">
    <button class="header__mobile__hamburger">☰</button>
    <div class="header__logo">...</div>
    <div class="header__mobile__button">Cart</div>
  </div>
  <div class="header__mobile__bottom">Search</div>
</header>
```

### Logo
```html
<div class="header__logo">
  <a href="/" class="header__logo__link">
    <span class="header__logo__text">NovaStrips</span>
  </a>
</div>
```

### Navegación
```html
<nav class="header__menu">
  <ul class="navmenu">
    <li class="navmenu__item">
      <a href="#" class="navmenu__link navlink navlink--toplevel">
        <span class="navtext navtext--parent">Products</span>
      </a>
    </li>
  </ul>
</nav>
```

### Dropdown Menu
```html
<div class="header__dropdown">
  <div class="header__dropdown__wrapper">
    <div class="header__dropdown__inner">
      <div class="header__dropdown__image">
        <img src="..." alt="...">
      </div>
      <!-- Contenido del dropdown -->
    </div>
  </div>
</div>
```

---

## HERO & BANNERS

### Hero Section
```html
<section class="hero__slide">
  <div class="hero__media">
    <div class="hero__bg">
      <img class="hero__image" src="..." alt="...">
    </div>
  </div>

  <div class="hero__content">
    <div class="hero__content__wrapper">
      <h2 class="hero__subheading">Subtitle</h2>
      <h1>Main Heading</h1>
      <div class="hero__rte">
        <p>Description text</p>
      </div>
      <div class="hero__button-group">
        <a href="#" class="btn">Shop Now</a>
      </div>
    </div>
  </div>
</section>
```

### Hero Variantes
```html
<!-- Hero compacto -->
<div class="hero__content hero__content--compact">...</div>

<!-- Hero sin padding -->
<div class="hero__content hero__content--no-padding">...</div>

<!-- Hero transparente -->
<div class="hero__content hero__content--transparent">...</div>
```

### Slideshow
```html
<div class="slideshow">
  <div class="slideshow__slide">...</div>
  <div class="slideshow__slide">...</div>
</div>

<!-- Controles del slider -->
<div class="slider__arrows">
  <button class="slider__button slider__button--prev">←</button>
  <button class="slider__button slider__button--next">→</button>
</div>
```

---

## GRID DE PRODUCTOS

### Grid Básico
```html
<!-- Grid de 3 columnas (responsive) -->
<div class="grid grid--3">
  <div class="grid-item">...</div>
  <div class="grid-item">...</div>
  <div class="grid-item">...</div>
</div>
```

### Grid Variantes
```html
<!-- 1 columna -->
<div class="grid grid--1">...</div>

<!-- 2 columnas -->
<div class="grid grid--2">...</div>

<!-- 3 columnas -->
<div class="grid grid--3">...</div>

<!-- Grid uniforme -->
<div class="grid grid--uniform">...</div>

<!-- Grid con sidebar -->
<div class="grid grid--sidebar">...</div>

<!-- Grid mobile slider -->
<div class="grid grid--mobile-slider">...</div>
```

---

## PRODUCT CARDS

### Product Item Completo
```html
<article class="product-item">
  <div class="product-item__image-container">
    <a href="/products/..." class="product-item__link">
      <div class="product-item__image">
        <img src="..." alt="...">
      </div>
    </a>

    <!-- Badge (opcional) -->
    <div class="product-item__badge">Sale</div>
  </div>

  <div class="product-item__info">
    <div class="product-item__vendor">Brand Name</div>

    <h3 class="product-item__title">
      <a href="/products/...">Product Name</a>
    </h3>

    <div class="product-item__price">
      <span class="new-price">$29.99</span>
      <span class="old-price">$39.99</span>
    </div>

    <!-- Swatches de color (opcional) -->
    <div class="product-item__swatch">...</div>
  </div>
</article>
```

### Grid Product (Alternativa)
```html
<div class="grid-product">
  <div class="grid-product__image-mask">
    <a href="..." class="grid-product__link">
      <img class="grid-product__image" src="..." alt="...">
    </a>
  </div>

  <div class="grid-product__content">
    <div class="grid-product__vendor">Brand</div>
    <div class="grid-product__title">Product Name</div>
    <div class="grid-product__price">$29.99</div>
  </div>
</div>
```

---

## PÁGINA DE PRODUCTO

### Product Page Structure
```html
<div class="product__section">
  <!-- Galería de imágenes -->
  <div class="product__gallery">
    <div class="product__media-container">
      <div class="product__media-item">
        <img class="product__media" src="..." alt="...">
      </div>
    </div>

    <!-- Thumbnails -->
    <div class="product__images">
      <button class="product__thumb is-active">
        <img src="..." alt="...">
      </button>
      <button class="product__thumb">
        <img src="..." alt="...">
      </button>
    </div>
  </div>

  <!-- Información del producto -->
  <div class="product__content">
    <div class="product__header">
      <div class="product__vendor">Brand Name</div>
      <h1 class="product__title">Product Name</h1>
    </div>

    <div class="product__price">
      <span class="new-price">$29.99</span>
      <span class="old-price">$39.99</span>
    </div>

    <!-- Formulario -->
    <div class="product__form-wrapper">
      <form class="product__form">
        <!-- Variantes -->
        <div class="product__swatches">...</div>

        <!-- Cantidad -->
        <div class="product__quantity">
          <input type="number" value="1">
        </div>

        <!-- Botón submit -->
        <button type="submit" class="product__submit btn">
          Add to Cart
        </button>
      </form>
    </div>

    <!-- Meta información -->
    <div class="product__meta">...</div>
  </div>
</div>
```

### Product Title Custom (HiStrips)
```html
<!-- Título específico de producto template -->
<h1 class="product__title template-product">
  ENERGY STRIPS
</h1>
```

### Alert Box (Custom HiStrips)
```html
<div class="red_part_pdp">
  <div class="icon_box">
    <img src="icon.svg" alt="">
  </div>
  <div>
    <h4>Important Notice</h4>
    <p>Free shipping on orders over $50</p>
  </div>
</div>
```

### Mobile Back Button (Custom HiStrips)
```html
<div class="mobe_back">
  <img src="arrow-left.svg" alt="">
  <h4><strong>Back to</strong> Products</h4>
</div>
```

---

## PRODUCT UPSELL (Custom HiStrips)

```html
<div class="product__upsell">
  <div class="product-upsell__holder">
    <h3 class="product-upsell__holder__title">
      You may also <strong>like</strong>
    </h3>

    <div class="upsell-swiper">
      <div class="swiper-wrapper">
        <div class="product-upsell">
          <div class="product-upsell__content">
            <h4 class="product-upsell__title">Product Name</h4>
            <div class="product-upsell__price">$19.99</div>
          </div>
          <form>
            <button class="product-upsell__btn btn">Add</button>
          </form>
        </div>
      </div>
    </div>
  </div>
</div>
```

---

## COLLECTIONS

### Collection Header
```html
<div class="collection__title-wrapper">
  <div class="collection__image">
    <img src="..." alt="...">
  </div>
  <h1 class="collection__title">Collection Name</h1>
</div>
```

### Collection Navigation
```html
<div class="collection__nav collection__nav--both">
  <!-- Filtros -->
  <div class="collection__nav--filter">
    <button class="collection__filters__btn">Filter</button>
  </div>

  <!-- Ordenamiento -->
  <div class="collection__nav--sort">
    <select>
      <option>Best Selling</option>
      <option>Price: Low to High</option>
      <option>Price: High to Low</option>
    </select>
  </div>
</div>
```

### Collection Sidebar
```html
<div class="collection__sidebar">
  <div class="collection__sidebar__head">
    <h3>Filter</h3>
    <button class="collection__sidebar__close">×</button>
  </div>

  <div class="collection__sidebar__slide-out">
    <!-- Filtros aquí -->
  </div>

  <div class="collection__sidebar__buttons">
    <button class="btn">Apply</button>
  </div>
</div>
```

### Active Filters
```html
<div class="collection__active__filters">
  <span>Color: Blue</span>
  <button>×</button>
</div>
```

### Collection Block
```html
<div class="collection-block">
  <div class="collection-block__wrapper">
    <div class="collection-block__image">
      <img src="..." alt="...">
    </div>

    <div class="collection-block__content">
      <h2>Collection Title</h2>
      <a href="..." class="collection-block__button btn">Shop Now</a>
    </div>
  </div>
</div>
```

---

## BUTTONS

### Button Variants
```html
<!-- Botón primario (default) -->
<button class="btn">Primary Button</button>

<!-- Botón secundario -->
<button class="btn btn--secondary">Secondary</button>

<!-- Botón outline -->
<button class="btn btn--outline">Outline</button>

<!-- Botón de texto -->
<button class="btn btn--text">Text Button</button>

<!-- Botón blanco -->
<button class="btn btn--white">White</button>

<!-- Botón negro -->
<button class="btn btn--black">Black</button>
```

### Button Sizes
```html
<!-- Pequeño -->
<button class="btn btn--small">Small</button>

<!-- Normal (default) -->
<button class="btn">Normal</button>

<!-- Grande -->
<button class="btn btn--large">Large</button>

<!-- Ancho completo -->
<button class="btn btn--full">Full Width</button>

<!-- Medio ancho -->
<button class="btn btn--half">Half Width</button>
```

### Button with Icon/Arrow
```html
<!-- Con flecha -->
<button class="btn btn--arrow">
  <span class="btn__text">Continue</span>
  →
</button>

<!-- Con loader -->
<button class="btn">
  <span class="btn__inner">
    <span class="btn__text">Add to Cart</span>
    <span class="btn__loader"></span>
  </span>
</button>
```

### Button States
```html
<!-- Loading -->
<button class="btn btn__loading">
  <span class="btn__loader"></span>
  Loading...
</button>

<!-- Added to cart -->
<button class="btn btn__added">
  ✓ Added
</button>

<!-- Error -->
<button class="btn btn__error">
  Error - Try Again
</button>
```

---

## CART

### Cart Header Icon
```html
<div class="header__cart__status">
  <div class="header__cart__status__holder">
    <span class="cart-count">3</span>
  </div>
</div>
```

---

## UTILITY CLASSES

### Color Palettes
```html
<!-- Contraste -->
<div class="palette--contrast">...</div>

<!-- Primario -->
<div class="palette--primary">...</div>

<!-- Contraste oscuro -->
<div class="palette--contrast--dark">...</div>
```

---

## RESPONSIVE UTILITIES

### Breakpoints en HTML
```html
<!-- Visible solo en mobile -->
<div class="mobile-only">...</div>

<!-- Visible solo en desktop -->
<div class="desktop-only">...</div>
```

### Grid Responsive
```html
<!-- Grid que se adapta automáticamente -->
<div class="grid grid--3">
  <!-- En mobile: 1 columna -->
  <!-- En tablet: 2 columnas -->
  <!-- En desktop: 3 columnas -->
</div>
```

---

## FLICKITY CAROUSEL

### Carousel Básico
```html
<div class="flickity-enabled">
  <div class="flickity-viewport">
    <div class="flickity-slider">
      <div class="flickity-cell">Item 1</div>
      <div class="flickity-cell">Item 2</div>
      <div class="flickity-cell">Item 3</div>
    </div>
  </div>

  <!-- Botones de navegación -->
  <button class="flickity-prev-next-button flickity-button--prev">
    ←
  </button>
  <button class="flickity-prev-next-button flickity-button--next">
    →
  </button>
</div>
```

---

## TIPS DE USO

### 1. Combinación de Clases
```html
<!-- ✅ Correcto -->
<button class="btn btn--large btn--outline">Large Outline</button>

<!-- ❌ Evitar conflictos -->
<button class="btn btn--primary btn--secondary">Conflicto</button>
```

### 2. Modificadores BEM
```html
<!-- Block -->
<div class="product">
  <!-- Element -->
  <h3 class="product__title">Title</h3>

  <!-- Element con Modifier -->
  <div class="product__price product__price--sale">$19.99</div>
</div>
```

### 3. Estados
```html
<!-- Usar clases de estado para interacciones -->
<button class="product__thumb is-active">...</button>
<div class="navmenu__item is-open">...</div>
```

### 4. Responsive Classes
```html
<!-- Mobile first approach -->
<div class="grid grid--1 grid--2@tablet grid--3@desktop">
  <!-- 1 columna mobile, 2 tablet, 3 desktop -->
</div>
```

---

## NOTAS IMPORTANTES

1. **BEM Methodology:** El tema usa BEM consistentemente
2. **Mobile First:** Los estilos base son para mobile
3. **Variables CSS:** Usa `var(--variable-name)` para personalización
4. **Clases Custom:** Las clases con prefijos específicos (red_part_pdp, mobe_back) son customizaciones de HiStrips
5. **Flickity:** Biblioteca de carrusel integrada
6. **Breakpoint Principal:** 750px separa mobile de desktop

---

**Última actualización:** 2025-11-17
**Archivo CSS completo:** `/Users/franferrer/novastrips-analysis/assets/histrips-complete.css`
