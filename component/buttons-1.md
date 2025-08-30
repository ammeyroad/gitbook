# Buttons

{% hint style="info" %}
Buttons are critical interactive elements that help users take actions throughout their journey. Our button system is designed to be clear, consistent, and accessible.
{% endhint %}

## 🎯 Button Types

{% tabs %}
{% tab title="Primary" %}
#### Primary Button

```html
<button class="btn btn-primary">
  Primary Action
</button>
```

```css
.btn-primary {
  background: var(--color-primary);
  color: white;
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 600;
}

.btn-primary:hover {
  background: var(--color-primary-dark);
}
```

Used for:

* Main call-to-action
* Form submissions
* Confirmation actions
{% endtab %}

{% tab title="Secondary" %}
#### Secondary Button

```html
<button class="btn btn-secondary">
  Secondary Action
</button>
```

```css
.btn-secondary {
  background: white;
  color: var(--color-primary);
  border: 2px solid var(--color-primary);
  padding: 12px 24px;
  border-radius: 8px;
}
```

Used for:

* Alternative actions
* Less prominent choices
* Cancel options
{% endtab %}

{% tab title="Text" %}
#### Text Button

```html
<button class="btn btn-text">
  Text Action
</button>
```

```css
.btn-text {
  background: none;
  color: var(--color-primary);
  padding: 12px 24px;
  text-decoration: underline;
}
```

Used for:

* Tertiary actions
* Links within text
* Minor actions
{% endtab %}
{% endtabs %}

## 📏 Sizes

### Button Sizes

```css
.btn-sm {
  padding: 8px 16px;
  font-size: 14px;
}

.btn-md {
  padding: 12px 24px;
  font-size: 16px;
}

.btn-lg {
  padding: 16px 32px;
  font-size: 18px;
}
```

| Size   | Use Case                |
| ------ | ----------------------- |
| Small  | Dense UIs, tight spaces |
| Medium | Default size            |
| Large  | Hero sections, CTAs     |

## 🎨 States

{% tabs %}
{% tab title="Interactive States" %}
#### Button States

```css
/* Hover */
.btn:hover {
  transform: translateY(-1px);
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

/* Active */
.btn:active {
  transform: translateY(0);
}

/* Focus */
.btn:focus {
  outline: none;
  ring: 2px solid var(--color-primary);
  ring-offset: 2px;
}
```
{% endtab %}

{% tab title="Disabled State" %}
#### Disabled Button

```css
.btn:disabled {
  opacity: 0.5;
  cursor: not-allowed;
  pointer-events: none;
}
```
{% endtab %}
{% endtabs %}

## 🔄 Loading State

```html
<button class="btn btn-primary is-loading">
  <span class="spinner"></span>
  Loading...
</button>
```

```css
.btn.is-loading {
  position: relative;
  cursor: wait;
}

.spinner {
  /* Loading animation styles */
}
```

## 🎯 Icon Buttons

### With Icons

```html
<!-- Left Icon -->
<button class="btn btn-primary">
  <icon name="plus" />
  Add Item
</button>

<!-- Right Icon -->
<button class="btn btn-primary">
  Next
  <icon name="arrow-right" />
</button>
```

{% hint style="warning" %}
#### Icon Guidelines

* Keep icons simple and clear
* Maintain 16px spacing between icon and text
* Use consistent icon size (usually 20px)
{% endhint %}

## ♿ Accessibility

{% hint style="success" %}
#### Accessibility Checklist

* Use semantic `<button>` elements
* Include aria-labels where needed
* Ensure 3:1 contrast ratio minimum
* Support keyboard navigation
* Provide visual feedback
{% endhint %}

```html
<!-- Accessible Button Example -->
<button 
  class="btn btn-primary"
  aria-label="Add new item"
  role="button"
>
  <icon aria-hidden="true" name="plus" />
  Add Item
</button>
```

## 📱 Responsive Behavior

| Screen Size | Padding   | Font Size | Min Width |
| ----------- | --------- | --------- | --------- |
| Mobile      | 12px 20px | 14px      | 100%      |
| Tablet      | 12px 24px | 16px      | auto      |
| Desktop     | 16px 32px | 16px      | auto      |

## 🎨 Usage Examples

### Common Patterns

```html
<!-- Primary CTA -->
<button class="btn btn-primary btn-lg">
  Start Free Trial
</button>

<!-- Form Submit -->
<button class="btn btn-primary" type="submit">
  Save Changes
</button>

<!-- Cancel Action -->
<button class="btn btn-secondary">
  Cancel
</button>

<!-- Text Link -->
<button class="btn btn-text">
  Learn More
</button>
```

{% hint style="info" %}
For implementation examples and code snippets, visit the Code Snippets section.
{% endhint %}
