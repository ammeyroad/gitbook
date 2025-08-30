# Feedback Components

{% hint style="info" %}
Komponen feedback memberikan respons visual kepada pengguna tentang aksi yang mereka lakukan. Komponen ini mencakup modal, toast notifications, tooltips, dan indikator status lainnya.
{% endhint %}

## 🪟 Modal

{% tabs %}
{% tab title="Basic Modal" %}
#### Basic Modal

```html
<div class="modal" role="dialog" aria-modal="true">
  <div class="modal-backdrop"></div>
  
  <div class="modal-content">
    <div class="modal-header">
      <h3 class="modal-title">Modal Title</h3>
      <button class="modal-close" aria-label="Close">×</button>
    </div>
    
    <div class="modal-body">
      Content goes here
    </div>
    
    <div class="modal-footer">
      <button class="btn btn-secondary">Cancel</button>
      <button class="btn btn-primary">Confirm</button>
    </div>
  </div>
</div>
```

```css
.modal {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
}

.modal-backdrop {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0,0,0,0.5);
}

.modal-content {
  position: relative;
  background: white;
  border-radius: 12px;
  width: 100%;
  max-width: 500px;
  margin: 2rem;
}
```
{% endtab %}

{% tab title="Modal Variants" %}
#### Modal Types

```html
<!-- Side Sheet -->
<div class="modal modal-side">
  <!-- Content -->
</div>

<!-- Full Screen -->
<div class="modal modal-full">
  <!-- Content -->
</div>

<!-- Alert Modal -->
<div class="modal modal-alert">
  <!-- Content -->
</div>
```
{% endtab %}
{% endtabs %}

## 🍞 Toast Notifications

```html
<div class="toast-container">
  <div class="toast success">
    <icon name="check" />
    <div class="toast-content">
      <h4>Success</h4>
      <p>Action completed successfully</p>
    </div>
    <button class="toast-close">×</button>
  </div>
</div>
```

```css
.toast-container {
  position: fixed;
  bottom: 2rem;
  right: 2rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  z-index: 1000;
}

.toast {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  background: white;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  animation: slideIn 0.3s ease-out;
}
```

## 💭 Tooltips

{% tabs %}
{% tab title="Basic Tooltip" %}
```html
<div class="tooltip-wrapper">
  <button class="btn">
    Hover me
  </button>
  
  <div class="tooltip" role="tooltip">
    Tooltip content
  </div>
</div>
```

```css
.tooltip {
  position: absolute;
  padding: 0.5rem 1rem;
  background: var(--color-dark);
  color: white;
  border-radius: 4px;
  font-size: 0.875rem;
  z-index: 100;
}

.tooltip::before {
  content: '';
  position: absolute;
  border: 6px solid transparent;
}
```
{% endtab %}

{% tab title="Tooltip Positions" %}
```css
.tooltip-top::before {
  bottom: -12px;
  border-top-color: var(--color-dark);
}

.tooltip-bottom::before {
  top: -12px;
  border-bottom-color: var(--color-dark);
}

/* Similar for left/right */
```
{% endtab %}
{% endtabs %}

## ⚡ Alert Messages

```html
<div class="alert info">
  <icon name="info" />
  <div class="alert-content">
    <h4>Information</h4>
    <p>This is an informational message.</p>
  </div>
  <button class="alert-close">×</button>
</div>

<div class="alert warning">
  <!-- Similar structure -->
</div>

<div class="alert error">
  <!-- Similar structure -->
</div>
```

```css
.alert {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  padding: 1rem;
  border-radius: 8px;
  margin-bottom: 1rem;
}

.alert.info {
  background: var(--color-info-light);
  border: 1px solid var(--color-info);
}
```

## 🔄 Loading States

{% tabs %}
{% tab title="Spinners" %}
#### Loading Spinner

```html
<div class="spinner" role="status">
  <span class="sr-only">Loading...</span>
</div>
```

```css
.spinner {
  width: 24px;
  height: 24px;
  border: 3px solid var(--color-border);
  border-top-color: var(--color-primary);
  border-radius: 50%;
  animation: spin 1s linear infinite;
}
```
{% endtab %}

{% tab title="Skeleton" %}
#### Skeleton Loading

```html
<div class="skeleton-wrapper">
  <div class="skeleton-line"></div>
  <div class="skeleton-line"></div>
  <div class="skeleton-line"></div>
</div>
```

```css
.skeleton-line {
  height: 20px;
  background: linear-gradient(
    90deg,
    var(--color-skeleton) 25%,
    var(--color-skeleton-highlight) 50%,
    var(--color-skeleton) 75%
  );
  background-size: 200% 100%;
  animation: shimmer 1.5s infinite;
  border-radius: 4px;
  margin-bottom: 0.5rem;
}
```
{% endtab %}
{% endtabs %}

## 📊 Progress Indicators

```html
<div class="progress-wrapper">
  <div class="progress-label">
    <span>Uploading...</span>
    <span>75%</span>
  </div>
  
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
</div>
```

## ♿ Accessibility

{% hint style="warning" %}
#### Accessibility Guidelines

* Use proper ARIA roles
* Manage focus
* Support keyboard interaction
* Provide screen reader text
* Handle animations responsibly
{% endhint %}

## 📱 Responsive Behavior

{% tabs %}
{% tab title="Mobile" %}
#### Mobile Adaptations

* Full-screen modals
* Bottom sheet dialogs
* Compact toasts
* Touch-friendly targets
{% endtab %}

{% tab title="Desktop" %}
#### Desktop Features

* Centered modals
* Multiple toasts
* Hover tooltips
* Rich interactions
{% endtab %}
{% endtabs %}

## 🎯 Usage Guidelines

{% hint style="success" %}
#### Best Practices

1. Keep feedback clear and concise
2. Use appropriate timing
3. Position feedback logically
4. Maintain consistency
5. Allow user control
{% endhint %}

### Animation Guidelines

```css
:root {
  --animation-duration: 0.3s;
  --animation-timing: cubic-bezier(0.4, 0, 0.2, 1);
}

@keyframes slideIn {
  from {
    transform: translateY(100%);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
```
