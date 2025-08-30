# 📊 Data Display Components

{% hint style="info" %}
Komponen data display dirancang untuk menampilkan informasi dengan cara yang terorganisir dan mudah dibaca. Sistem ini mencakup cards, tables, lists, dan komponen display lainnya.
{% endhint %}

## 🎴 Cards

{% tabs %}
{% tab title="Basic Card" %}
### Basic Card
```html
<div class="card">
  <div class="card-header">
    <h3 class="card-title">Card Title</h3>
  </div>
  
  <div class="card-body">
    Content goes here
  </div>
  
  <div class="card-footer">
    <button class="btn btn-primary">Action</button>
  </div>
</div>
```

```css
.card {
  background: white;
  border-radius: 12px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  overflow: hidden;
}

.card-header {
  padding: 1rem 1.5rem;
  border-bottom: 1px solid var(--color-border);
}

.card-body {
  padding: 1.5rem;
}
```
{% endtab %}

{% tab title="Interactive Card" %}
### Interactive Card
```html
<a href="#" class="card interactive">
  <img src="/image.jpg" class="card-image" alt="..." />
  <div class="card-overlay">
    <h3 class="card-title">Interactive Card</h3>
    <p class="card-text">Click to learn more</p>
  </div>
</a>
```

```css
.card.interactive {
  transition: transform 0.2s;
}

.card.interactive:hover {
  transform: translateY(-4px);
}
```
{% endtab %}
{% endtabs %}

## 📋 Tables

### Basic Table
```html
<div class="table-container">
  <table class="table">
    <thead>
      <tr>
        <th>ID</th>
        <th>Name</th>
        <th>Status</th>
        <th>Actions</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>#001</td>
        <td>John Doe</td>
        <td>
          <span class="badge success">Active</span>
        </td>
        <td>
          <button class="btn btn-icon">
            <icon name="edit" />
          </button>
        </td>
      </tr>
    </tbody>
  </table>
</div>
```

```css
.table {
  width: 100%;
  border-collapse: collapse;
}

.table th,
.table td {
  padding: 1rem;
  text-align: left;
  border-bottom: 1px solid var(--color-border);
}

.table tbody tr:hover {
  background: var(--color-background-hover);
}
```

### Data Table Features
```html
<div class="data-table">
  <!-- Table Controls -->
  <div class="table-controls">
    <div class="table-search">
      <input type="search" placeholder="Search..." />
    </div>
    
    <div class="table-filters">
      <!-- Filters -->
    </div>
  </div>
  
  <!-- Table Content -->
  <table class="table">
    <!-- ... -->
  </table>
  
  <!-- Pagination -->
  <div class="table-pagination">
    <!-- ... -->
  </div>
</div>
```

## 📝 Lists

{% tabs %}
{% tab title="Basic List" %}
### Simple List
```html
<ul class="list">
  <li class="list-item">
    <span class="list-content">List item one</span>
  </li>
  <li class="list-item">
    <span class="list-content">List item two</span>
  </li>
</ul>
```

```css
.list {
  border: 1px solid var(--color-border);
  border-radius: 8px;
  overflow: hidden;
}

.list-item {
  padding: 1rem;
  border-bottom: 1px solid var(--color-border);
}
```
{% endtab %}

{% tab title="Interactive List" %}
### Interactive List
```html
<ul class="list interactive">
  <li class="list-item">
    <div class="list-content">
      <img src="/avatar.jpg" class="avatar" />
      <div class="list-text">
        <h4>John Doe</h4>
        <p>john@example.com</p>
      </div>
    </div>
    <button class="btn btn-icon">
      <icon name="chevron-right" />
    </button>
  </li>
</ul>
```
{% endtab %}
{% endtabs %}

## 📊 Stats & Metrics

```html
<div class="stats-grid">
  <div class="stat-card">
    <div class="stat-header">
      <icon name="users" />
      <h4>Total Users</h4>
    </div>
    <div class="stat-value">1,234</div>
    <div class="stat-footer">
      <span class="trend positive">+5.2%</span>
      vs last month
    </div>
  </div>
</div>
```

```css
.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.5rem;
}

.stat-card {
  padding: 1.5rem;
  background: white;
  border-radius: 12px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
```

## 🏷️ Tags & Badges

```html
<span class="badge">Default</span>
<span class="badge success">Success</span>
<span class="badge warning">Warning</span>
<span class="badge error">Error</span>

<div class="tag">
  Tag Label
  <button class="tag-remove">×</button>
</div>
```

```css
.badge {
  display: inline-flex;
  padding: 0.25rem 0.75rem;
  border-radius: 999px;
  font-size: 0.875rem;
  font-weight: 500;
}

.tag {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.5rem 1rem;
  background: var(--color-background-light);
  border-radius: 8px;
}
```

## 📈 Progress Indicators

{% tabs %}
{% tab title="Progress Bar" %}
```html
<div class="progress">
  <div 
    class="progress-bar" 
    style="width: 75%"
    role="progressbar"
    aria-valuenow="75"
    aria-valuemin="0"
    aria-valuemax="100"
  ></div>
</div>
```
{% endtab %}

{% tab title="Loading States" %}
```html
<div class="skeleton"></div>
<div class="skeleton"></div>
<div class="skeleton"></div>

<div class="spinner">
  <!-- Loading animation -->
</div>
```
{% endtab %}
{% endtabs %}

## ♿ Accessibility

{% hint style="warning" %}
### Accessibility Guidelines
- Use semantic HTML
- Include proper ARIA labels
- Ensure keyboard navigation
- Provide adequate color contrast
- Support screen readers
{% endhint %}

## 📱 Responsive Behavior

{% tabs %}
{% tab title="Mobile" %}
### Mobile Adaptations
- Stack cards vertically
- Scrollable tables
- Simplified lists
- Full-width elements
{% endtab %}

{% tab title="Desktop" %}
### Desktop Features
- Grid layouts
- Fixed tables
- Hover states
- Side-by-side layouts
{% endtab %}
{% endtabs %}

{% hint style="success" %}
### Best Practices
1. Keep data organized
2. Use clear hierarchy
3. Show loading states
4. Handle empty states
5. Support interactions
{% endhint %}
