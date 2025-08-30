# 📏 Grid & Layout System

{% hint style="info" %}
Sistem grid dan layout yang konsisten membantu menciptakan hierarki visual dan pengalaman pengguna yang lebih baik di seluruh platform digital Clipan Finance.
{% endhint %}

## 🎯 Grid System

{% tabs %}
{% tab title="Base Grid" %}
### 12-Column Grid
```css
.container {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: var(--spacing-md);
  max-width: 1440px;
  margin: 0 auto;
  padding: 0 var(--spacing-lg);
}
```

- 12 kolom untuk fleksibilitas maksimal
- Gutter width: 24px
- Margin luar: 24px (mobile) - 64px (desktop)
{% endtab %}

{% tab title="Breakpoints" %}
### Responsive Breakpoints

```css
--breakpoint-xs: 320px;  /* Mobile S */
--breakpoint-sm: 375px;  /* Mobile M */
--breakpoint-md: 768px;  /* Tablet */
--breakpoint-lg: 1024px; /* Desktop */
--breakpoint-xl: 1440px; /* Large Desktop */
```

#### Container Widths
| Breakpoint | Max Width | Padding |
|------------|-----------|---------|
| Mobile     | 100%      | 16px    |
| Tablet     | 768px     | 24px    |
| Desktop    | 1024px    | 32px    |
| Large      | 1440px    | 64px    |
{% endtab %}
{% endtabs %}

## 📐 Layout Components

### Container Types

{% tabs %}
{% tab title="Fixed Width" %}
```css
.container-fixed {
  width: 100%;
  max-width: var(--container-width);
  margin: 0 auto;
  padding: 0 var(--spacing-container);
}
```

Used for:
- Main content areas
- Article pages
- Form sections
{% endtab %}

{% tab title="Fluid Width" %}
```css
.container-fluid {
  width: 100%;
  padding: 0 var(--spacing-container);
}
```

Used for:
- Full-width headers
- Hero sections
- Background elements
{% endtab %}
{% endtabs %}

## 🔄 Spacing System

### Base Units
```css
--spacing-unit: 8px;

--spacing-xs: calc(var(--spacing-unit) * 0.5);  /* 4px */
--spacing-sm: var(--spacing-unit);              /* 8px */
--spacing-md: calc(var(--spacing-unit) * 2);    /* 16px */
--spacing-lg: calc(var(--spacing-unit) * 3);    /* 24px */
--spacing-xl: calc(var(--spacing-unit) * 4);    /* 32px */
--spacing-xxl: calc(var(--spacing-unit) * 6);   /* 48px */
```

{% hint style="warning" %}
### Spacing Guidelines
- Gunakan variabel spacing untuk konsistensi
- Pertahankan vertical rhythm
- Sesuaikan spacing dengan breakpoint
{% endhint %}

## 📱 Responsive Patterns

### Layout Shifts

| Component | Mobile | Tablet | Desktop |
|-----------|--------|--------|---------|
| Navigation | Stack  | Horizontal | Horizontal + Dropdown |
| Grid      | 1 Column | 2 Columns | 4 Columns |
| Sidebar   | Hidden  | Overlay | Fixed |
| Forms     | Full Width | 75% Width | 50% Width |

### CSS Example
```css
.grid-layout {
  display: grid;
  gap: var(--spacing-md);
  
  /* Mobile: 1 column */
  grid-template-columns: 1fr;
  
  /* Tablet: 2 columns */
  @media (min-width: 768px) {
    grid-template-columns: repeat(2, 1fr);
  }
  
  /* Desktop: 4 columns */
  @media (min-width: 1024px) {
    grid-template-columns: repeat(4, 1fr);
  }
}
```

## 🎨 Layout Components

{% tabs %}
{% tab title="Card Grid" %}
### Card Layout
```css
.card-grid {
  display: grid;
  gap: var(--spacing-md);
  grid-template-columns: repeat(
    auto-fit, 
    minmax(300px, 1fr)
  );
}
```
{% endtab %}

{% tab title="Form Layout" %}
### Form Layout
```css
.form-layout {
  display: grid;
  gap: var(--spacing-lg);
  max-width: 600px;
  margin: 0 auto;
}
```
{% endtab %}
{% endtabs %}

{% hint style="success" %}
### Best Practices
1. Gunakan sistem grid yang konsisten
2. Pertahankan hierarki visual
3. Perhatikan white space
4. Optimasi untuk berbagai device
{% endhint %}

## 📏 Layout Utilities

### Margin & Padding Classes
```css
.m-0 { margin: 0; }
.m-1 { margin: var(--spacing-xs); }
.m-2 { margin: var(--spacing-sm); }
.m-3 { margin: var(--spacing-md); }
.m-4 { margin: var(--spacing-lg); }
.m-5 { margin: var(--spacing-xl); }

/* Similar patterns for padding */
```

{% hint style="info" %}
Complete documentation of utility classes can be found in the [Design Tokens](design-tokens.md) section.
{% endhint %}
