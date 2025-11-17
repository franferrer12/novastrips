# QUICK START - INSTALACIÓN RÁPIDA

**Proyecto:** NovaStrips - Réplica de HiStrips.com
**Tiempo estimado:** 30-60 minutos

---

## PASO 1: VERIFICAR ARCHIVOS

Asegúrate de tener todos los archivos necesarios:

```
✅ 8 secciones Liquid en /sections/
✅ 1 archivo CSS en /assets/
✅ 1 template index.json en /templates/
✅ Documentación completa
```

Para verificar:
```bash
cd /Users/franferrer/novastrips-analysis/
ls -lh sections/*histrips*.liquid
ls -lh assets/histrips-complete.css
ls -lh templates/index.json
```

---

## PASO 2: CONECTAR CON SHOPIFY

### Opción A: Shopify CLI (Recomendado)

```bash
# Instalar Shopify CLI si no lo tienes
brew tap shopify/shopify
brew install shopify-cli

# Autenticar
shopify login

# Conectar con tu tienda
shopify theme dev
```

### Opción B: Manual (Admin)

1. Ir a Shopify Admin → Online Store → Themes
2. Hacer click en "Add theme" → "Upload ZIP file"
3. O usar el editor de código online

---

## PASO 3: SUBIR ARCHIVOS

### Con Shopify CLI:

```bash
cd /Users/franferrer/novastrips-analysis/

# Subir todo
shopify theme push

# O subir archivos específicos
shopify theme push --only sections/
shopify theme push --only assets/
shopify theme push --only templates/
```

### Manual:

1. Copiar cada archivo .liquid a la carpeta correspondiente
2. Subir histrips-complete.css a Assets
3. Actualizar index.json en Templates

---

## PASO 4: CONFIGURAR THEME

### 4.1 Incluir el CSS

Editar `layout/theme.liquid` y agregar antes de `</head>`:

```liquid
{{ 'histrips-complete.css' | asset_url | stylesheet_tag }}
```

### 4.2 Verificar JavaScript

Asegúrate de que estén cargados:
- vendor.js (Flickity para sliders)
- theme.js (funcionalidad del tema)

En `layout/theme.liquid` antes de `</body>`:

```liquid
<script src="{{ 'vendor.js' | asset_url }}" defer></script>
<script src="{{ 'theme.js' | asset_url }}" defer></script>
```

---

## PASO 5: CONFIGURAR HOMEPAGE

1. Ir a **Themes → Customize**
2. Seleccionar **Homepage**
3. El template `index.json` ya tiene todas las secciones en orden

### Verificar que aparezcan estas secciones:
- ✅ Announcement Bar HiStrips
- ✅ Header HiStrips
- ✅ Hero Secondary HiStrips (×3)
- ✅ Logo Cloud HiStrips
- ✅ Product Grid HiStrips
- ✅ Features HiStrips
- ✅ Reviews HiStrips
- ✅ Rich Text HiStrips
- ✅ Footer HiStrips

---

## PASO 6: AGREGAR CONTENIDO

### 6.1 Announcement Bar

En Customizer → Announcement Bar HiStrips:
- Los mensajes ya están configurados
- Puedes editar texto, colores y velocidad
- Por defecto: "BLACK FRIDAY: 30% OFF" y "30-day guarantee"

### 6.2 Header

En Customizer → Header HiStrips:
1. Subir logo (PNG o SVG)
2. Ajustar tamaño (80px desktop, 120px mobile)
3. Seleccionar menú principal

**Crear menú principal:**
- Navigation → Main Menu
- Agregar links: Shop, About, Contact, etc.

### 6.3 Hero Images

Para cada Hero Section:
1. Subir imagen desktop (mínimo 2000px ancho)
2. Subir imagen mobile (mínimo 750px ancho)
3. Agregar link (opcional): `/collections/all`
4. Alt text: "Hero image"

**Recomendaciones:**
- Hero 1: Imagen principal de producto
- Hero 2: Lifestyle/atleta usando el producto
- Hero 3: Close-up de producto o beneficios

### 6.4 Logo Cloud ("WORN BY THE BEST")

1. Preparar 6 logos de marcas (formato PNG transparente)
2. Tamaño recomendado: 200×100px
3. Subir en cada bloque de logo
4. Agregar alt text descriptivo

**Ejemplo de logos:**
- Nike
- Adidas
- Reebok
- Under Armour
- Puma
- New Balance

### 6.5 Product Grid

1. **Crear colección:**
   - Products → Collections → Create collection
   - Nombre: "All Products" (handle: `all`)
   - Agregar productos

2. **En Customizer → Product Grid:**
   - Collection: "All Products"
   - Products limit: 8
   - Columns: 4 (desktop), 2 (mobile)

3. **Crear productos:**
   - Products → Add product
   - Título: "Black Nasal Strips"
   - Precio: €25,95
   - Compare at price: €35,95 (para mostrar descuento)
   - Agregar 2 imágenes (main + hover)

### 6.6 Features

En Customizer → Features HiStrips:

1. **Feature 1:**
   - Icon: Subir SVG o PNG (60×60px)
   - Title: "Premium Quality"
   - Text: "Made with the highest quality materials..."

2. **Feature 2:**
   - Icon: Subir icono
   - Title: "Enhanced Performance"
   - Text: "Designed to boost your athletic performance..."

3. **Feature 3:**
   - Icon: Subir icono
   - Title: "Hypoallergenic"
   - Text: "Safe for sensitive skin..."

### 6.7 Reviews

En Customizer → Reviews HiStrips:

1. **Review 1:**
   - Rating: 5 stars
   - Text: "These strips have completely transformed..."
   - Author image: Subir foto (100×100px, circular)
   - Author name: "Sarah Johnson"
   - Author title: "Professional Runner"

2. **Review 2 y 3:**
   - Seguir mismo formato
   - Variar testimonios

### 6.8 Rich Text

En Customizer → Rich Text HiStrips:
- Title: "HiStrips Inside"
- Text: Ya está configurado
- Ajustar alineación y tamaños si necesario

### 6.9 Footer

En Customizer → Footer HiStrips:

1. **Menu Block 1 (Shop):**
   - Crear menú "Footer" en Navigation
   - Links: Products, Collections, New Arrivals

2. **Menu Block 2 (Support):**
   - Links: FAQ, Shipping, Returns, Contact

3. **Text Block (About):**
   - Title: "About HiStrips"
   - Text: Descripción de la marca

4. **Newsletter Block:**
   - Ya configurado
   - Editar texto si necesario

5. **Social Links:**
   - Agregar URLs de redes sociales
   - Facebook, Instagram, Twitter, YouTube

6. **Copyright:**
   - Text: "© 2024 HiStrips. All rights reserved."

---

## PASO 7: VERIFICAR RESPONSIVE

### Mobile Testing (< 750px)
- [ ] Announcement bar legible
- [ ] Hamburger menu funciona
- [ ] Hero images se ven bien
- [ ] Logo cloud se desplaza
- [ ] Product grid: 2 columnas
- [ ] Features: 1 columna
- [ ] Reviews: scrollable
- [ ] Footer organizado verticalmente

### Desktop Testing (> 1024px)
- [ ] Header con logo centrado
- [ ] Navegación visible
- [ ] Hero full-width
- [ ] Product grid: 4 columnas
- [ ] Features: 3 columnas
- [ ] Reviews: 3 visibles
- [ ] Footer: 4 columnas

### Herramientas:
```bash
# Abrir en diferentes dispositivos
# Desktop: Chrome DevTools (F12)
# Mobile: Chrome → Device Toolbar (Cmd+Shift+M)
```

---

## PASO 8: OPTIMIZAR IMÁGENES

### Herramientas recomendadas:

1. **TinyPNG** - https://tinypng.com/
   - Comprimir JPG/PNG sin pérdida de calidad

2. **Squoosh** - https://squoosh.app/
   - Convertir a WebP para mejor performance

3. **ImageOptim** (Mac) - https://imageoptim.com/
   - Optimización batch local

### Tamaños recomendados:

- **Hero Desktop:** 2000×800px (aspect 2.5:1)
- **Hero Mobile:** 750×590px (aspect 1.27:1)
- **Logo:** 400×200px max
- **Logo Cloud:** 200×100px
- **Product Images:** 1000×1000px
- **Feature Icons:** 100×100px
- **Review Avatars:** 100×100px

---

## PASO 9: PERFORMANCE CHECK

### Usar Google PageSpeed Insights

```
https://pagespeed.web.dev/
```

1. Ingresar URL de tu tienda
2. Esperar análisis
3. Aplicar recomendaciones

### Checklist:
- [ ] Imágenes optimizadas
- [ ] CSS minificado
- [ ] JavaScript defer/async
- [ ] Fonts optimizadas
- [ ] Lazy loading activado

---

## PASO 10: TESTING FINAL

### Funcionalidad:
- [ ] Announcement bar cambia mensajes (7 seg)
- [ ] Header sticky funciona
- [ ] Logo cloud se anima infinitamente
- [ ] Product grid muestra precios correctos
- [ ] Quick add funciona (si implementado)
- [ ] Reviews son legibles
- [ ] Newsletter form acepta emails
- [ ] Footer links funcionan
- [ ] Social icons van a URLs correctas

### Cross-browser:
- [ ] Chrome
- [ ] Firefox
- [ ] Safari
- [ ] Edge
- [ ] Mobile Safari
- [ ] Mobile Chrome

### Accesibilidad:
- [ ] Alt text en todas las imágenes
- [ ] Labels en forms
- [ ] Contraste de colores adecuado
- [ ] Navegación por teclado funciona

---

## PASO 11: LANZAMIENTO

### Pre-launch Checklist:

1. **SEO:**
   - [ ] Títulos de página configurados
   - [ ] Meta descriptions agregadas
   - [ ] Open Graph images
   - [ ] Sitemap generado

2. **Legal:**
   - [ ] Privacy Policy
   - [ ] Terms of Service
   - [ ] Refund Policy
   - [ ] Cookie notice

3. **Analytics:**
   - [ ] Google Analytics instalado
   - [ ] Facebook Pixel configurado
   - [ ] Shopify Analytics activo

4. **Pagos:**
   - [ ] Payment providers configurados
   - [ ] Test orders realizados
   - [ ] Shipping zones configurados

### Go Live:

```bash
# Remover password page
Shopify Admin → Online Store → Preferences
→ Desmarcar "Enable password"
```

---

## TROUBLESHOOTING RÁPIDO

### Problema: CSS no se aplica
```liquid
<!-- Verificar en theme.liquid -->
{{ 'histrips-complete.css' | asset_url | stylesheet_tag }}

<!-- Limpiar caché del navegador: Cmd+Shift+R -->
```

### Problema: Secciones no aparecen en Customizer
```bash
# Re-push de secciones
shopify theme push --only sections/

# Verificar errores de sintaxis en {% schema %}
```

### Problema: Imágenes rotas
```liquid
<!-- Verificar que las imágenes estén subidas -->
<!-- En Shopify Admin → Content → Files -->
```

### Problema: Slider no funciona
```liquid
<!-- Verificar vendor.js incluye Flickity -->
<!-- O agregar CDN en theme.liquid: -->
<link rel="stylesheet" href="https://unpkg.com/flickity@2/dist/flickity.min.css">
<script src="https://unpkg.com/flickity@2/dist/flickity.pkgd.min.js"></script>
```

---

## RECURSOS DE AYUDA

### Documentación del proyecto:
- `SECCIONES_HISTRIPS_RESUMEN.md` - Detalle de cada sección
- `INDEX_COMPLETO.md` - Índice del proyecto
- `HISTRIPS_ESTRUCTURA_COMPLETA.md` - Análisis original
- `CSS_CLASSES_GUIDE.md` - Guía de clases CSS

### Enlaces útiles:
- [Shopify Theme Docs](https://shopify.dev/themes)
- [Liquid Cheat Sheet](https://www.shopify.com/partners/shopify-cheat-sheet)
- [Theme Kit](https://shopify.dev/themes/tools/theme-kit)

---

## SIGUIENTE NIVEL

Una vez que todo funcione:

1. **Agregar apps:**
   - Loox (Reviews)
   - Klaviyo (Email)
   - Yotpo (UGC)

2. **Mejorar performance:**
   - Lazy loading avanzado
   - Critical CSS inline
   - Image CDN

3. **A/B Testing:**
   - Headlines
   - CTA buttons
   - Product images

4. **Marketing:**
   - Email flows
   - Abandoned cart
   - Social proof

---

## RESUMEN EJECUTIVO

**Tiempo por paso:**
- Paso 1-3 (Setup): 10 min
- Paso 4-5 (Configuración): 15 min
- Paso 6 (Contenido): 30-60 min
- Paso 7-10 (Testing): 20 min

**TOTAL: 1-2 horas**

---

**¡Listo para empezar!**

Si tienes algún problema, revisa la documentación completa en los archivos .md del proyecto.

---

**Última actualización: 2025-11-17**
