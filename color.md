# 🎨 Color System

{% hint style="info" %}
Warna utama Clipan Finance mencerminkan profesionalisme, kepercayaan, dan semangat modern. Sistem warna ini dirancang untuk menciptakan pengalaman visual yang konsisten dan aksesibel.
{% endhint %}

## 🔵 Warna Primer

{% tabs %}
{% tab title="Biru Clipan" %}
<div style="background-color: #005BAC; width: 200px; height: 100px; border-radius: 8px; margin-bottom: 16px;"></div>

### Biru Clipan
- **HEX:** `#005BAC`
- **RGB:** (0, 91, 172)
- **HSL:** 208, 100%, 34%

#### Variasi Opacity
| Opacity | Use Case |
|---------|----------|
| 100% | Primary buttons, Headers |
| 75% | Icons, Secondary elements |
| 50% | Backgrounds, Hover states |
| 25% | Disabled states |
{% endtab %}

{% tab title="Oranye Clipan" %}
<div style="background-color: #F37021; width: 200px; height: 100px; border-radius: 8px; margin-bottom: 16px;"></div>

### Oranye Clipan
- **HEX:** `#F37021`
- **RGB:** (243, 112, 33)
- **HSL:** 23, 89%, 54%

#### Variasi Opacity
| Opacity | Use Case |
|---------|----------|
| 100% | CTAs, Highlights |
| 75% | Accent elements |
| 50% | Hover effects |
| 25% | Subtle indicators |
{% endtab %}
{% endtabs %}

## ⚪ Warna Sekunder

{% tabs %}
{% tab title="Abu-abu" %}
### Sistem Grayscale

| Tone | HEX | Use Case |
|------|-----|----------|
| <div style="background-color: #FFFFFF; width: 20px; height: 20px; border: 1px solid #ccc;"></div> White | `#FFFFFF` | Background |
| <div style="background-color: #F5F5F5; width: 20px; height: 20px; border: 1px solid #ccc;"></div> Gray-50 | `#F5F5F5` | Section Background |
| <div style="background-color: #E0E0E0; width: 20px; height: 20px; border: 1px solid #ccc;"></div> Gray-200 | `#E0E0E0` | Borders |
| <div style="background-color: #9E9E9E; width: 20px; height: 20px; border: 1px solid #ccc;"></div> Gray-500 | `#9E9E9E` | Disabled Text |
| <div style="background-color: #212121; width: 20px; height: 20px; border: 1px solid #ccc;"></div> Gray-900 | `#212121` | Body Text |
{% endtab %}

{% tab title="Status Colors" %}
### Warna Status

| Status | HEX | Contoh Penggunaan |
|--------|-----|-------------------|
| <div style="background-color: #4CAF50; width: 20px; height: 20px; border-radius: 4px;"></div> Success | `#4CAF50` | Konfirmasi, Berhasil |
| <div style="background-color: #F44336; width: 20px; height: 20px; border-radius: 4px;"></div> Error | `#F44336` | Error, Delete |
| <div style="background-color: #FFC107; width: 20px; height: 20px; border-radius: 4px;"></div> Warning | `#FFC107` | Peringatan |
| <div style="background-color: #2196F3; width: 20px; height: 20px; border-radius: 4px;"></div> Info | `#2196F3` | Informasi |
{% endtab %}
{% endtabs %}

## 🎯 Panduan Penggunaan

{% hint style="warning" %}
### Rules & Guidelines
1. Warna primer harus digunakan untuk:
   - Call-to-action utama
   - Headers dan navigasi
   - Elemen brand penting

2. Warna sekunder digunakan untuk:
   - Background sections
   - Text dan borders
   - Status indicators
{% endhint %}

## ♿ Aksesibilitas

{% hint style="success" %}
### WCAG Compliance
- Rasio kontras minimal **4.5:1** untuk teks regular
- Rasio kontras minimal **3:1** untuk teks besar (18pt+)
- Pastikan warna tidak menjadi satu-satunya indikator untuk informasi penting
{% endhint %}

### Color Combinations Matrix

| Background | Text Color | Ratio | Status |
|------------|------------|-------|---------|
| Biru Clipan | White | 5.2:1 | ✅ Pass |
| Oranye Clipan | Black | 4.8:1 | ✅ Pass |
| Gray-50 | Gray-900 | 16:1 | ✅ Pass |

{% hint style="info" %}
**Tools untuk checking:**
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [Colorable](https://colorable.jxnblk.com/)
{% endhint %}
