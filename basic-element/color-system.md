# Color System

{% hint style="info" %}
Warna utama Clipan Finance mencerminkan profesionalisme, kepercayaan, dan semangat modern. Sistem warna ini dirancang untuk menciptakan pengalaman visual yang konsisten dan aksesibel.
{% endhint %}

## 🔵 Warna Primer

{% tabs %}
{% tab title="Biru Clipan" %}
#### ![](<../.gitbook/assets/Screenshot 2025-08-30 at 17.25.14.png>)

#### Biru Clipan

* **HEX:** `#005BAC`
* **RGB:** (0, 91, 172)
* **HSL:** 208, 100%, 34%

**Variasi Opacity**

| Opacity | Use Case                  |
| ------- | ------------------------- |
| 100%    | Primary buttons, Headers  |
| 75%     | Icons, Secondary elements |
| 50%     | Backgrounds, Hover states |
| 25%     | Disabled states           |
{% endtab %}

{% tab title="Oranye Clipan" %}
#### Oranye Clipan

* **HEX:** `#F37021`
* **RGB:** (243, 112, 33)
* **HSL:** 23, 89%, 54%

**Variasi Opacity**

| Opacity | Use Case          |
| ------- | ----------------- |
| 100%    | CTAs, Highlights  |
| 75%     | Accent elements   |
| 50%     | Hover effects     |
| 25%     | Subtle indicators |
{% endtab %}
{% endtabs %}

## ⚪ Warna Sekunder

{% tabs %}
{% tab title="Abu-abu" %}
#### Sistem Grayscale

| Tone     | HEX       | Use Case           |
| -------- | --------- | ------------------ |
| White    | `#FFFFFF` | Background         |
| Gray-50  | `#F5F5F5` | Section Background |
| Gray-200 | `#E0E0E0` | Borders            |
| Gray-500 | `#9E9E9E` | Disabled Text      |
| Gray-900 | `#212121` | Body Text          |
{% endtab %}

{% tab title="Status Colors" %}
#### Warna Status

| Status  | HEX       | Contoh Penggunaan    |
| ------- | --------- | -------------------- |
| Success | `#4CAF50` | Konfirmasi, Berhasil |
| Error   | `#F44336` | Error, Delete        |
| Warning | `#FFC107` | Peringatan           |
| Info    | `#2196F3` | Informasi            |
{% endtab %}
{% endtabs %}

## 🎯 Panduan Penggunaan

{% hint style="warning" %}
#### Rules & Guidelines

1. Warna primer harus digunakan untuk:
   * Call-to-action utama
   * Headers dan navigasi
   * Elemen brand penting
2. Warna sekunder digunakan untuk:
   * Background sections
   * Text dan borders
   * Status indicators
{% endhint %}

## ♿ Aksesibilitas

{% hint style="success" %}
#### WCAG Compliance

* Rasio kontras minimal **4.5:1** untuk teks regular
* Rasio kontras minimal **3:1** untuk teks besar (18pt+)
* Pastikan warna tidak menjadi satu-satunya indikator untuk informasi penting
{% endhint %}

### Color Combinations Matrix

| Background    | Text Color | Ratio | Status |
| ------------- | ---------- | ----- | ------ |
| Biru Clipan   | White      | 5.2:1 | ✅ Pass |
| Oranye Clipan | Black      | 4.8:1 | ✅ Pass |
| Gray-50       | Gray-900   | 16:1  | ✅ Pass |

{% hint style="info" %}
**Tools untuk checking:**

* [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)
* [Colorable](https://colorable.jxnblk.com/)
{% endhint %}
