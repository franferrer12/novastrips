# CSS Snippets - HiStrips Theme
## Código listo para copiar y usar en Shopify

---

## CUSTOM PROPERTIES VARIABLES

### Variables Principales para Personalizar
```css
/* Copiar esto en tu theme.css o en Shopify Theme Customizer */
:root {
  /* COLORES PRINCIPALES */
  --COLOR-PRIMARY: #000000;
  --COLOR-PRIMARY-HOVER: #333333;
  --COLOR-PRIMARY-FADE: rgba(0, 0, 0, 0.1);
  --COLOR-PRIMARY-LIGHT: #f5f5f5;
  --COLOR-PRIMARY-OPPOSITE: #ffffff;

  /* COLORES DE FONDO */
  --COLOR-BG: #ffffff;
  --COLOR-BG-SECONDARY: #f7f7f7;
  --COLOR-BG-SECONDARY-LIGHTEN: #fafafa;

  /* COLORES DE TEXTO */
  --COLOR-TEXT: #000000;
  --COLOR-TEXT-DARK: #1a1a1a;
  --COLOR-TEXT-LIGHT: #767676;
  --COLOR-A35: rgba(0, 0, 0, 0.35);
  --COLOR-A70: rgba(0, 0, 0, 0.70);
  --COLOR-A75: rgba(0, 0, 0, 0.75);

  /* ENLACES */
  --COLOR-LINK: #000000;
  --COLOR-LINK-HOVER: #666666;

  /* BORDES */
  --COLOR-BORDER: #e8e8e8;
  --COLOR-BORDER-HAIRLINE: #f2f2f2;

  /* SALE/DESCUENTO */
  --COLOR-SALE-BG: #ff0000;
  --COLOR-SALE-TEXT: #ffffff;
  --COLOR-SALE-TEXT-SECONDARY: #000000;

  /* ESTADOS */
  --COLOR-ERROR: #d02e2e;
  --COLOR-ERROR-BG: rgba(208, 46, 46, 0.1);

  /* TIPOGRAFÍA */
  --FONT-STACK-HEADING: 'Helvetica Now Display', -apple-system, sans-serif;
  --FONT-STACK-BODY: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --FONT-STACK-SUBHEADING: var(--FONT-STACK-BODY);
  --FONT-STACK-NAV: var(--FONT-STACK-BODY);
  --BTN-FONT-STACK: var(--FONT-STACK-BODY);

  /* LAYOUT */
  --LAYOUT-GUTTER: 20px;
  --LAYOUT-OUTER: 40px;
  --content-max: 1100px;
  --header-height: 80px;
  --btn-radius: 10px;

  /* SCALE TIPOGRÁFICA */
  --base: 16px;
  --font-2: 12px;
  --font-3: 14px;
  --font-4: 16px;
  --font-5: 19px;
  --font-6: 23px;
  --font-7: 27px;
  --font-8: 32px;
  --font-9: 37px;
  --font-10: 40px;
  --font-11: 43px;
  --font-12: 47px;
  --font-13: 50px;
  --font-14: 52px;
  --font-15: 55px;
}
```

---

## COMPONENTES LISTOS PARA USAR

### 1. Product Card Moderno
```html
<article class="product-card">
  <a href="{{ product.url }}" class="product-card__link">
    <div class="product-card__image-wrapper">
      <img
        src="{{ product.featured_image | img_url: '600x' }}"
        alt="{{ product.title }}"
        class="product-card__image"
        loading="lazy"
      >
      {% if product.compare_at_price > product.price %}
        <span class="product-card__badge">Sale</span>
      {% endif %}
    </div>

    <div class="product-card__info">
      <span class="product-card__vendor">{{ product.vendor }}</span>
      <h3 class="product-card__title">{{ product.title }}</h3>

      <div class="product-card__price">
        <span class="price">{{ product.price | money }}</span>
        {% if product.compare_at_price > product.price %}
          <span class="price--compare">{{ product.compare_at_price | money }}</span>
        {% endif %}
      </div>
    </div>
  </a>
</article>

<style>
.product-card {
  position: relative;
  display: flex;
  flex-direction: column;
}

.product-card__link {
  text-decoration: none;
  color: inherit;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.product-card__image-wrapper {
  position: relative;
  aspect-ratio: 1;
  overflow: hidden;
  border-radius: 8px;
  margin-bottom: 12px;
}

.product-card__image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.product-card__link:hover .product-card__image {
  transform: scale(1.05);
}

.product-card__badge {
  position: absolute;
  top: 10px;
  right: 10px;
  background: var(--COLOR-SALE-BG, #ff0000);
  color: var(--COLOR-SALE-TEXT, #fff);
  padding: 4px 12px;
  border-radius: 4px;
  font-size: 12px;
  font-weight: 600;
  text-transform: uppercase;
}

.product-card__info {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.product-card__vendor {
  font-size: 12px;
  color: var(--COLOR-TEXT-LIGHT, #767676);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.product-card__title {
  font-size: 16px;
  font-weight: 600;
  line-height: 1.3;
  margin: 0;
}

.product-card__price {
  display: flex;
  gap: 8px;
  align-items: baseline;
  font-weight: 600;
  margin-top: 4px;
}

.price--compare {
  text-decoration: line-through;
  color: var(--COLOR-TEXT-LIGHT, #767676);
  font-size: 14px;
}
</style>
```

---

### 2. Alert Box (HiStrips Custom)
```html
<div class="alert-box alert-box--warning">
  <div class="alert-box__icon">
    <svg width="20" height="20" viewBox="0 0 20 20">
      <path d="M10 0C4.48 0 0 4.48 0 10s4.48 10 10 10 10-4.48 10-10S15.52 0 10 0zm1 15H9v-2h2v2zm0-4H9V5h2v6z"/>
    </svg>
  </div>
  <div class="alert-box__content">
    <h4 class="alert-box__title">Important Notice</h4>
    <p class="alert-box__text">Free shipping on orders over $50</p>
  </div>
</div>

<style>
.alert-box {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 12px 16px;
  border-radius: 8px;
  border: 1px dashed;
}

.alert-box--warning {
  background-color: #ffdce2;
  border-color: #a40001;
  color: #a50000;
}

.alert-box--info {
  background-color: #e3f2fd;
  border-color: #1976d2;
  color: #0d47a1;
}

.alert-box--success {
  background-color: #e8f5e9;
  border-color: #388e3c;
  color: #1b5e20;
}

.alert-box__icon {
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 20px;
  height: 20px;
}

.alert-box__icon svg {
  fill: currentColor;
}

.alert-box__content {
  flex: 1;
}

.alert-box__title {
  font-size: 14px;
  font-weight: 700;
  margin: 0 0 4px 0;
}

.alert-box__text {
  font-size: 13px;
  margin: 0;
  line-height: 1.4;
}
</style>
```

---

### 3. Button System Completo
```html
<!-- Botones Primarios -->
<button class="btn-modern">Primary Button</button>
<button class="btn-modern btn-modern--secondary">Secondary</button>
<button class="btn-modern btn-modern--outline">Outline</button>

<!-- Botones con Estados -->
<button class="btn-modern btn-modern--loading">
  <span class="btn-modern__spinner"></span>
  <span>Loading...</span>
</button>

<button class="btn-modern btn-modern--success">
  <svg class="btn-modern__icon" width="16" height="16">
    <path d="M6 12L2 8l1.4-1.4L6 9.2l6.6-6.6L14 4l-8 8z"/>
  </svg>
  <span>Added to Cart</span>
</button>

<style>
.btn-modern {
  /* Base */
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 12px 24px;
  font-family: var(--FONT-STACK-BODY);
  font-size: 16px;
  font-weight: 600;
  line-height: 1;
  text-decoration: none;
  border: 2px solid transparent;
  border-radius: var(--btn-radius, 10px);
  cursor: pointer;
  transition: all 0.2s ease;
  position: relative;
  overflow: hidden;

  /* Primary colors */
  background-color: var(--COLOR-PRIMARY, #000);
  color: var(--COLOR-PRIMARY-OPPOSITE, #fff);
}

.btn-modern:hover {
  background-color: var(--COLOR-PRIMARY-HOVER, #333);
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.btn-modern:active {
  transform: translateY(0);
}

.btn-modern:disabled {
  opacity: 0.5;
  cursor: not-allowed;
  pointer-events: none;
}

/* Secondary */
.btn-modern--secondary {
  background-color: var(--COLOR-BG-SECONDARY, #f7f7f7);
  color: var(--COLOR-TEXT, #000);
}

.btn-modern--secondary:hover {
  background-color: #e8e8e8;
}

/* Outline */
.btn-modern--outline {
  background-color: transparent;
  color: var(--COLOR-PRIMARY, #000);
  border-color: var(--COLOR-PRIMARY, #000);
}

.btn-modern--outline:hover {
  background-color: var(--COLOR-PRIMARY, #000);
  color: var(--COLOR-PRIMARY-OPPOSITE, #fff);
}

/* Loading */
.btn-modern--loading {
  pointer-events: none;
}

.btn-modern__spinner {
  display: inline-block;
  width: 16px;
  height: 16px;
  border: 2px solid currentColor;
  border-right-color: transparent;
  border-radius: 50%;
  animation: spinner-rotate 0.6s linear infinite;
}

@keyframes spinner-rotate {
  to { transform: rotate(360deg); }
}

/* Success */
.btn-modern--success {
  background-color: #56AD6A;
  color: white;
}

.btn-modern__icon {
  fill: currentColor;
}

/* Sizes */
.btn-modern--small {
  padding: 8px 16px;
  font-size: 14px;
}

.btn-modern--large {
  padding: 16px 32px;
  font-size: 18px;
}

.btn-modern--full {
  width: 100%;
}
</style>
```

---

### 4. Hero Section Responsive
```html
<section class="hero-section">
  <div class="hero-section__media">
    <picture>
      <source
        media="(min-width: 750px)"
        srcset="{{ section.settings.image_desktop | img_url: '1800x' }}"
      >
      <img
        src="{{ section.settings.image_mobile | img_url: '800x' }}"
        alt="{{ section.settings.heading }}"
        class="hero-section__image"
      >
    </picture>
  </div>

  <div class="hero-section__content">
    <div class="hero-section__inner">
      {% if section.settings.subheading %}
        <p class="hero-section__subheading">{{ section.settings.subheading }}</p>
      {% endif %}

      <h1 class="hero-section__heading">{{ section.settings.heading }}</h1>

      {% if section.settings.text %}
        <div class="hero-section__text">{{ section.settings.text }}</div>
      {% endif %}

      {% if section.settings.button_label %}
        <a href="{{ section.settings.button_link }}" class="btn-modern">
          {{ section.settings.button_label }}
        </a>
      {% endif %}
    </div>
  </div>
</section>

<style>
.hero-section {
  position: relative;
  min-height: 500px;
  display: flex;
  align-items: center;
  overflow: hidden;
}

.hero-section__media {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.hero-section__image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.hero-section__content {
  position: relative;
  z-index: 1;
  width: 100%;
  padding: 60px 20px;
  max-width: var(--content-max, 1100px);
  margin: 0 auto;
}

.hero-section__inner {
  max-width: 600px;
  background: rgba(255, 255, 255, 0.95);
  padding: 40px;
  border-radius: 12px;
  backdrop-filter: blur(10px);
}

.hero-section__subheading {
  font-size: 14px;
  text-transform: uppercase;
  letter-spacing: 1px;
  color: var(--COLOR-TEXT-LIGHT);
  margin: 0 0 12px 0;
}

.hero-section__heading {
  font-size: clamp(32px, 5vw, 55px);
  font-weight: 700;
  line-height: 1.1;
  margin: 0 0 20px 0;
  font-family: var(--FONT-STACK-HEADING);
}

.hero-section__text {
  font-size: 16px;
  line-height: 1.6;
  margin: 0 0 24px 0;
  color: var(--COLOR-TEXT);
}

/* Responsive */
@media (min-width: 750px) {
  .hero-section {
    min-height: 600px;
  }

  .hero-section__inner {
    padding: 60px;
  }
}
</style>
```

---

### 5. Product Grid Responsive
```html
<div class="products-grid">
  {% for product in collection.products %}
    <!-- Usar el Product Card del snippet #1 -->
  {% endfor %}
</div>

<style>
.products-grid {
  display: grid;
  gap: 24px;
  padding: 20px;
  max-width: var(--content-max, 1100px);
  margin: 0 auto;

  /* Mobile: 1 columna */
  grid-template-columns: 1fr;
}

/* Tablet: 2 columnas */
@media (min-width: 750px) {
  .products-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
  }
}

/* Desktop: 3 columnas */
@media (min-width: 990px) {
  .products-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 40px;
  }
}

/* Large Desktop: 4 columnas */
@media (min-width: 1400px) {
  .products-grid {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>
```

---

### 6. Mobile Navigation
```html
<div class="mobile-nav">
  <button class="mobile-nav__toggle" aria-label="Toggle menu">
    <span class="hamburger">
      <span></span>
      <span></span>
      <span></span>
    </span>
  </button>

  <nav class="mobile-nav__menu">
    <div class="mobile-nav__header">
      <h2>Menu</h2>
      <button class="mobile-nav__close">×</button>
    </div>

    <ul class="mobile-nav__list">
      {% for link in linklists.main-menu.links %}
        <li class="mobile-nav__item">
          <a href="{{ link.url }}" class="mobile-nav__link">
            {{ link.title }}
          </a>
        </li>
      {% endfor %}
    </ul>
  </nav>

  <div class="mobile-nav__overlay"></div>
</div>

<style>
.mobile-nav__toggle {
  background: none;
  border: none;
  padding: 10px;
  cursor: pointer;
  display: none;
}

.hamburger {
  display: flex;
  flex-direction: column;
  gap: 4px;
  width: 24px;
}

.hamburger span {
  display: block;
  height: 2px;
  background: currentColor;
  transition: all 0.3s ease;
}

.mobile-nav__menu {
  position: fixed;
  top: 0;
  left: -100%;
  width: 280px;
  height: 100vh;
  background: white;
  z-index: 1000;
  transition: left 0.3s ease;
  overflow-y: auto;
}

.mobile-nav__menu.is-open {
  left: 0;
}

.mobile-nav__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  border-bottom: 1px solid var(--COLOR-BORDER);
}

.mobile-nav__header h2 {
  margin: 0;
  font-size: 20px;
}

.mobile-nav__close {
  background: none;
  border: none;
  font-size: 32px;
  line-height: 1;
  cursor: pointer;
  padding: 0;
  width: 32px;
  height: 32px;
}

.mobile-nav__list {
  list-style: none;
  margin: 0;
  padding: 0;
}

.mobile-nav__item {
  border-bottom: 1px solid var(--COLOR-BORDER-HAIRLINE);
}

.mobile-nav__link {
  display: block;
  padding: 16px 20px;
  text-decoration: none;
  color: var(--COLOR-TEXT);
  font-weight: 500;
}

.mobile-nav__link:hover {
  background: var(--COLOR-BG-SECONDARY);
}

.mobile-nav__overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  z-index: 999;
  opacity: 0;
  visibility: hidden;
  transition: all 0.3s ease;
}

.mobile-nav__overlay.is-visible {
  opacity: 1;
  visibility: visible;
}

/* Mobile only */
@media (max-width: 749px) {
  .mobile-nav__toggle {
    display: block;
  }
}
</style>

<script>
document.addEventListener('DOMContentLoaded', () => {
  const toggle = document.querySelector('.mobile-nav__toggle');
  const menu = document.querySelector('.mobile-nav__menu');
  const overlay = document.querySelector('.mobile-nav__overlay');
  const close = document.querySelector('.mobile-nav__close');

  function openMenu() {
    menu.classList.add('is-open');
    overlay.classList.add('is-visible');
    document.body.style.overflow = 'hidden';
  }

  function closeMenu() {
    menu.classList.remove('is-open');
    overlay.classList.remove('is-visible');
    document.body.style.overflow = '';
  }

  toggle?.addEventListener('click', openMenu);
  close?.addEventListener('click', closeMenu);
  overlay?.addEventListener('click', closeMenu);
});
</script>
```

---

### 7. Sticky Header
```html
<header class="site-header" id="siteHeader">
  <div class="site-header__inner">
    <a href="/" class="site-header__logo">
      {{ shop.name }}
    </a>

    <nav class="site-header__nav">
      <!-- Navigation here -->
    </nav>

    <div class="site-header__actions">
      <a href="/cart" class="site-header__cart">
        Cart ({{ cart.item_count }})
      </a>
    </div>
  </div>
</header>

<style>
.site-header {
  position: sticky;
  top: 0;
  width: 100%;
  background: white;
  border-bottom: 1px solid var(--COLOR-BORDER);
  z-index: 100;
  transition: all 0.3s ease;
}

.site-header.is-scrolled {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.site-header__inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px;
  max-width: var(--content-max, 1100px);
  margin: 0 auto;
  gap: 20px;
}

.site-header__logo {
  font-size: 24px;
  font-weight: 700;
  text-decoration: none;
  color: var(--COLOR-TEXT);
}

.site-header__nav {
  flex: 1;
  display: none;
}

.site-header__actions {
  display: flex;
  gap: 16px;
  align-items: center;
}

@media (min-width: 750px) {
  .site-header__nav {
    display: block;
  }
}
</style>

<script>
window.addEventListener('scroll', () => {
  const header = document.getElementById('siteHeader');
  if (window.scrollY > 50) {
    header.classList.add('is-scrolled');
  } else {
    header.classList.remove('is-scrolled');
  }
});
</script>
```

---

### 8. Loading Skeleton (Product Card)
```html
<div class="skeleton-product-card">
  <div class="skeleton skeleton--image"></div>
  <div class="skeleton skeleton--text skeleton--text-short"></div>
  <div class="skeleton skeleton--text"></div>
  <div class="skeleton skeleton--text skeleton--text-medium"></div>
</div>

<style>
.skeleton {
  background: linear-gradient(
    90deg,
    #f0f0f0 25%,
    #e8e8e8 50%,
    #f0f0f0 75%
  );
  background-size: 200% 100%;
  animation: skeleton-loading 1.5s infinite;
  border-radius: 4px;
}

@keyframes skeleton-loading {
  0% { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}

.skeleton--image {
  aspect-ratio: 1;
  border-radius: 8px;
  margin-bottom: 12px;
}

.skeleton--text {
  height: 16px;
  margin-bottom: 8px;
}

.skeleton--text-short {
  width: 40%;
}

.skeleton--text-medium {
  width: 60%;
}
</style>
```

---

## ANIMACIONES ÚTILES

### Fade In on Scroll
```html
<div class="fade-in-scroll">Content here</div>

<style>
.fade-in-scroll {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.fade-in-scroll.is-visible {
  opacity: 1;
  transform: translateY(0);
}
</style>

<script>
const observerOptions = {
  threshold: 0.1,
  rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('is-visible');
    }
  });
}, observerOptions);

document.querySelectorAll('.fade-in-scroll').forEach(el => {
  observer.observe(el);
});
</script>
```

---

## UTILITY CLASSES

```css
/* Display */
.hide { display: none !important; }
.show { display: block !important; }

/* Responsive visibility */
@media (max-width: 749px) {
  .hide-mobile { display: none !important; }
}

@media (min-width: 750px) {
  .hide-desktop { display: none !important; }
}

/* Text alignment */
.text-left { text-align: left; }
.text-center { text-align: center; }
.text-right { text-align: right; }

/* Spacing */
.mt-0 { margin-top: 0; }
.mt-1 { margin-top: 8px; }
.mt-2 { margin-top: 16px; }
.mt-3 { margin-top: 24px; }
.mt-4 { margin-top: 32px; }

.mb-0 { margin-bottom: 0; }
.mb-1 { margin-bottom: 8px; }
.mb-2 { margin-bottom: 16px; }
.mb-3 { margin-bottom: 24px; }
.mb-4 { margin-bottom: 32px; }

/* Container */
.container {
  max-width: var(--content-max, 1100px);
  margin-left: auto;
  margin-right: auto;
  padding-left: 20px;
  padding-right: 20px;
}

.container--wide {
  max-width: 1400px;
}

.container--narrow {
  max-width: 800px;
}
```

---

**Nota:** Todos estos snippets están optimizados para Shopify y son totalmente responsivos. Puedes copiarlos directamente en tus archivos de tema.
