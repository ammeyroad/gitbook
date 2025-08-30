# 🔄 Design → Development Guide

{% hint style="info" %}
Panduan ini membantu menjembatani proses transisi dari desain ke implementasi, memastikan konsistensi antara desain dan produk akhir.
{% endhint %}

## 🎯 Design Handoff Process

{% tabs %}
{% tab title="Design Files" %}
### Figma Organization
1. Pages diorganisir berdasarkan product/feature
2. Components dalam shared library
3. Auto-layout untuk konsistensi spacing
4. Dokumentasi pada setiap component

### Asset Export
- SVG untuk icons & illustrations
- PNG/JPG untuk images
- PDF untuk dokumen print
{% endtab %}

{% tab title="Development Setup" %}
### Tech Stack
```json
{
  "frontend": {
    "framework": "Vue.js/Nuxt 3",
    "styling": "TailwindCSS",
    "components": "Custom UI Library"
  }
}
```

### Required Tools
- Node.js v16+
- Git
- VS Code + Extensions
{% endtab %}
{% endtabs %}

## 🎨 Style Implementation

### CSS Variables
```css
:root {
  /* Colors */
  --color-primary: #005BAC;
  --color-secondary: #F37021;
  
  /* Typography */
  --font-primary: 'Poppins', sans-serif;
  --font-size-base: 16px;
  
  /* Spacing */
  --spacing-unit: 8px;
  --spacing-md: calc(var(--spacing-unit) * 2);
}
```

### Tailwind Config
```javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: 'var(--color-primary)',
        secondary: 'var(--color-secondary)'
      },
      fontFamily: {
        sans: ['Poppins', 'sans-serif']
      },
      spacing: {
        md: 'var(--spacing-md)'
      }
    }
  }
}
```

## 🔄 Component Development

### Component Structure
```vue
<template>
  <button 
    class="btn btn-primary"
    :disabled="loading"
  >
    <slot />
  </button>
</template>

<script setup>
defineProps({
  loading: Boolean
})
</script>

<style scoped>
.btn {
  /* Base styles */
}
.btn-primary {
  /* Primary variant styles */
}
</style>
```

{% hint style="warning" %}
### Best Practices
1. Gunakan props untuk variasi
2. Dokumentasi komponen
3. Unit testing
4. Accessibility checks
{% endhint %}

## 📱 Responsive Implementation

### Media Queries
```scss
// Mobile First Approach
@media (min-width: 768px) {
  // Tablet styles
}

@media (min-width: 1024px) {
  // Desktop styles
}
```

### Tailwind Breakpoints
```html
<div class="
  w-full          <!-- Mobile -->
  md:w-1/2       <!-- Tablet -->
  lg:w-1/3       <!-- Desktop -->
">
  Content
</div>
```

## ♿ Accessibility Implementation

### ARIA Labels
```html
<button
  aria-label="Close modal"
  aria-pressed="false"
  class="btn-icon"
>
  <icon name="close" />
</button>
```

### Keyboard Navigation
```javascript
// Focus trap for modals
const trapFocus = (element) => {
  const focusableEls = element.querySelectorAll(
    'a[href], button, textarea, input[type="text"]'
  )
}
```

## 🔍 QA Checklist

{% tabs %}
{% tab title="Visual QA" %}
### Visual Testing
- [ ] Match with design specs
- [ ] Responsive behavior
- [ ] Animations & transitions
- [ ] Color contrast
- [ ] Typography scaling
{% endtab %}

{% tab title="Functional QA" %}
### Functional Testing
- [ ] Component behaviors
- [ ] State management
- [ ] Error handling
- [ ] Loading states
- [ ] Form validation
{% endtab %}

{% tab title="Accessibility QA" %}
### A11y Testing
- [ ] Screen reader compatibility
- [ ] Keyboard navigation
- [ ] ARIA labels
- [ ] Color contrast
- [ ] Focus management
{% endtab %}
{% endtabs %}

## 📦 Asset Management

### Image Optimization
```javascript
// Next.js Image component example
import Image from 'next/image'

export default function OptimizedImage() {
  return (
    <Image
      src="/hero.jpg"
      alt="Hero section"
      width={1200}
      height={600}
      priority
    />
  )
}
```

### Icon System
```javascript
// Icon component
const Icon = ({ name, size = 24 }) => {
  return (
    <svg
      width={size}
      height={size}
      aria-hidden="true"
    >
      <use href={`/icons.svg#${name}`} />
    </svg>
  )
}
```

{% hint style="success" %}
### Performance Tips
1. Lazy load images
2. Use SVG sprite sheets
3. Optimize bundle size
4. Enable caching
{% endhint %}
