# Navigation Components

{% hint style="info" %}
Sistem navigasi yang intuitif membantu pengguna menjelajahi aplikasi dengan mudah. Komponen navigasi kami dirancang untuk memberikan pengalaman yang konsisten dan user-friendly.
{% endhint %}

## 📱 Navbar

{% tabs %}
{% tab title="Basic Navbar" %}
#### Main Navigation

```html
<nav class="navbar">
  <div class="navbar-brand">
    <img src="/logo.svg" alt="Clipan Finance" />
  </div>
  
  <ul class="navbar-menu">
    <li class="navbar-item">
      <a href="/products" class="navbar-link">Products</a>
    </li>
    <li class="navbar-item">
      <a href="/about" class="navbar-link">About</a>
    </li>
  </ul>
  
  <div class="navbar-actions">
    <button class="btn btn-primary">Login</button>
  </div>
</nav>
```

```css
.navbar {
  display: flex;
  align-items: center;
  padding: 1rem 2rem;
  background: white;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.navbar-menu {
  display: flex;
  gap: 2rem;
  margin: 0 auto;
}
```
{% endtab %}

{% tab title="Responsive Navbar" %}
#### Mobile Navigation

```html
<nav class="navbar">
  <button class="navbar-toggle" aria-label="Menu">
    <icon name="menu" />
  </button>
  
  <div class="navbar-mobile" id="mobileMenu">
    <!-- Mobile menu content -->
  </div>
</nav>
```

```css
@media (max-width: 768px) {
  .navbar-menu {
    display: none;
  }
  
  .navbar-mobile {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: white;
    padding: 2rem;
  }
}
```
{% endtab %}
{% endtabs %}

## 📑 Sidebar

### Basic Sidebar

```html
<aside class="sidebar">
  <div class="sidebar-header">
    <img src="/logo.svg" alt="Logo" />
  </div>
  
  <nav class="sidebar-nav">
    <a href="/dashboard" class="sidebar-link">
      <icon name="home" />
      <span>Dashboard</span>
    </a>
    
    <a href="/transactions" class="sidebar-link">
      <icon name="transfer" />
      <span>Transactions</span>
    </a>
  </nav>
</aside>
```

```css
.sidebar {
  width: 280px;
  height: 100vh;
  background: var(--color-surface);
  border-right: 1px solid var(--color-border);
  padding: 1.5rem;
}

.sidebar-link {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.75rem 1rem;
  border-radius: 8px;
  color: var(--color-text);
  transition: all 0.2s;
}

.sidebar-link:hover,
.sidebar-link.active {
  background: var(--color-primary-light);
  color: var(--color-primary);
}
```

## 🔤 Tabs

{% tabs %}
{% tab title="Basic Tabs" %}
#### Horizontal Tabs

```html
<div class="tabs">
  <nav class="tabs-nav">
    <button class="tab-button active">Overview</button>
    <button class="tab-button">Details</button>
    <button class="tab-button">History</button>
  </nav>
  
  <div class="tab-content">
    <!-- Tab panels -->
  </div>
</div>
```

```css
.tabs-nav {
  display: flex;
  border-bottom: 2px solid var(--color-border);
}

.tab-button {
  padding: 1rem 2rem;
  border-bottom: 2px solid transparent;
  margin-bottom: -2px;
}

.tab-button.active {
  border-bottom-color: var(--color-primary);
  color: var(--color-primary);
}
```
{% endtab %}

{% tab title="Vertical Tabs" %}
#### Vertical Layout

```html
<div class="tabs-vertical">
  <nav class="tabs-nav-vertical">
    <!-- Tab buttons -->
  </nav>
  
  <div class="tab-content">
    <!-- Tab panels -->
  </div>
</div>
```

```css
.tabs-vertical {
  display: flex;
  gap: 2rem;
}

.tabs-nav-vertical {
  display: flex;
  flex-direction: column;
  border-right: 2px solid var(--color-border);
}
```
{% endtab %}
{% endtabs %}

## 🔍 Breadcrumbs

```html
<nav aria-label="Breadcrumb" class="breadcrumb">
  <ol class="breadcrumb-list">
    <li class="breadcrumb-item">
      <a href="/">Home</a>
    </li>
    <li class="breadcrumb-item">
      <a href="/products">Products</a>
    </li>
    <li class="breadcrumb-item active">
      Details
    </li>
  </ol>
</nav>
```

```css
.breadcrumb-list {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.breadcrumb-item:not(:last-child):after {
  content: '/';
  margin-left: 0.5rem;
  color: var(--color-text-light);
}
```

## 📱 Bottom Navigation

```html
<nav class="bottom-nav">
  <a href="/home" class="bottom-nav-item active">
    <icon name="home" />
    <span>Home</span>
  </a>
  
  <a href="/search" class="bottom-nav-item">
    <icon name="search" />
    <span>Search</span>
  </a>
</nav>
```

```css
.bottom-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: space-around;
  background: white;
  padding: 0.75rem;
  box-shadow: 0 -2px 4px rgba(0,0,0,0.1);
}
```

## 🔄 Dropdown Menu

```html
<div class="dropdown">
  <button class="dropdown-trigger">
    Menu
    <icon name="chevron-down" />
  </button>
  
  <ul class="dropdown-menu">
    <li><a href="#" class="dropdown-item">Profile</a></li>
    <li><a href="#" class="dropdown-item">Settings</a></li>
    <li><a href="#" class="dropdown-item">Logout</a></li>
  </ul>
</div>
```

## ♿ Accessibility

{% hint style="warning" %}
#### Navigation Accessibility

* Use semantic HTML (`<nav>`, `<button>`)
* Include ARIA labels
* Support keyboard navigation
* Provide skip links
* Ensure proper focus management
{% endhint %}

## 📱 Responsive Patterns

{% tabs %}
{% tab title="Mobile" %}
#### Mobile Navigation

* Hamburger menu
* Bottom navigation
* Simplified breadcrumbs
* Collapsible sidebar
{% endtab %}

{% tab title="Tablet" %}
#### Tablet Navigation

* Expandable sidebar
* Horizontal tabs
* Full breadcrumbs
{% endtab %}

{% tab title="Desktop" %}
#### Desktop Navigation

* Persistent sidebar
* Horizontal navbar
* Multiple level dropdowns
{% endtab %}
{% endtabs %}

{% hint style="success" %}
#### Best Practices

1. Keep navigation consistent
2. Provide visual feedback
3. Use clear labels
4. Maintain hierarchy
5. Consider mobile-first
{% endhint %}
