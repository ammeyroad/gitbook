# Form Components

{% hint style="info" %}
Form components adalah elemen penting dalam interaksi user. Sistem form kita dirancang untuk kemudahan penggunaan dan aksesibilitas.
{% endhint %}

## 🔤 Text Input

{% tabs %}
{% tab title="Basic Input" %}
#### Text Input

```html
<div class="form-group">
  <label for="name" class="form-label">Nama Lengkap</label>
  <input 
    type="text" 
    id="name"
    class="form-input"
    placeholder="Masukkan nama lengkap"
  />
  <span class="form-hint">Sesuai KTP/Passport</span>
</div>
```

```css
.form-input {
  width: 100%;
  padding: 12px 16px;
  border: 1px solid var(--color-border);
  border-radius: 8px;
  font-size: 16px;
  transition: all 0.2s;
}

.form-input:focus {
  border-color: var(--color-primary);
  box-shadow: 0 0 0 3px rgba(0,91,172,0.1);
}
```
{% endtab %}

{% tab title="Validation States" %}
#### Input States

```html
<!-- Success State -->
<div class="form-group">
  <input class="form-input is-valid" />
  <span class="form-feedback success">✓ Data valid</span>
</div>

<!-- Error State -->
<div class="form-group">
  <input class="form-input is-invalid" />
  <span class="form-feedback error">⚠ Data tidak valid</span>
</div>
```
{% endtab %}
{% endtabs %}

## 🔘 Select & Dropdown

```html
<div class="form-group">
  <label for="province" class="form-label">Provinsi</label>
  <select id="province" class="form-select">
    <option value="">Pilih Provinsi</option>
    <option value="DKI">DKI Jakarta</option>
    <option value="JB">Jawa Barat</option>
  </select>
</div>
```

```css
.form-select {
  appearance: none;
  background-image: url('data:image/svg+xml...');
  background-repeat: no-repeat;
  background-position: right 12px center;
}
```

## ✅ Checkbox & Radio

{% tabs %}
{% tab title="Checkbox" %}
#### Checkbox Input

```html
<label class="checkbox-wrapper">
  <input type="checkbox" class="checkbox-input" />
  <span class="checkbox-label">
    Saya setuju dengan syarat dan ketentuan
  </span>
</label>
```

```css
.checkbox-input {
  position: absolute;
  opacity: 0;
}

.checkbox-label {
  position: relative;
  padding-left: 32px;
  cursor: pointer;
}

.checkbox-label:before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  width: 20px;
  height: 20px;
  border: 2px solid var(--color-border);
  border-radius: 4px;
}
```
{% endtab %}

{% tab title="Radio" %}
#### Radio Input

```html
<div class="radio-group">
  <label class="radio-wrapper">
    <input type="radio" name="payment" value="credit" />
    <span class="radio-label">Kartu Kredit</span>
  </label>
  
  <label class="radio-wrapper">
    <input type="radio" name="payment" value="transfer" />
    <span class="radio-label">Transfer Bank</span>
  </label>
</div>
```
{% endtab %}
{% endtabs %}

## 📅 Date & Time

### Date Picker

```html
<div class="form-group">
  <label class="form-label">Tanggal Lahir</label>
  <input 
    type="date" 
    class="form-input date-input"
    min="1900-01-01"
  />
</div>
```

## 📱 File Upload

```html
<div class="upload-area">
  <input 
    type="file" 
    id="document" 
    class="upload-input"
    accept=".pdf,.jpg,.png"
  />
  <label for="document" class="upload-label">
    <icon name="upload" />
    <span>Upload Dokumen</span>
  </label>
</div>
```

## 🔍 Search Input

```html
<div class="search-wrapper">
  <icon name="search" class="search-icon" />
  <input 
    type="search"
    class="search-input"
    placeholder="Cari..."
  />
</div>
```

## 📝 Text Area

```html
<div class="form-group">
  <label class="form-label">Deskripsi</label>
  <textarea 
    class="form-textarea"
    rows="4"
    placeholder="Tulis deskripsi..."
  ></textarea>
</div>
```

## 🎯 Form Layout

{% tabs %}
{% tab title="Grid Layout" %}
#### Form Grid

```html
<form class="form-grid">
  <div class="form-col-6">
    <input type="text" placeholder="Nama Depan" />
  </div>
  <div class="form-col-6">
    <input type="text" placeholder="Nama Belakang" />
  </div>
</form>
```

```css
.form-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: var(--spacing-md);
}

.form-col-6 {
  grid-column: span 6;
}
```
{% endtab %}

{% tab title="Responsive" %}
#### Responsive Form

```css
@media (max-width: 768px) {
  .form-col-6 {
    grid-column: span 12;
  }
}
```
{% endtab %}
{% endtabs %}

## ♿ Accessibility

{% hint style="warning" %}
#### Accessibility Checklist

* Use semantic HTML
* Include proper labels
* Provide error messages
* Support keyboard navigation
* Use ARIA attributes when needed
{% endhint %}

## 🔄 Form Validation

```javascript
const validateForm = {
  required: (value) => !!value || 'Field is required',
  email: (value) => {
    const pattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
    return pattern.test(value) || 'Invalid email'
  },
  phone: (value) => {
    const pattern = /^[0-9]{10,13}$/
    return pattern.test(value) || 'Invalid phone number'
  }
}
```

{% hint style="success" %}
#### Best Practices

1. Validate in real-time
2. Show clear error messages
3. Maintain form state
4. Provide success feedback
{% endhint %}
