# 📚 Typography System

{% hint style="info" %}
Tipografi membantu menjaga konsistensi visual dan nada komunikasi brand. Sistem ini dirancang untuk memastikan keterbacaan dan hirarki yang jelas di seluruh platform.
{% endhint %}

## 🎯 Font Utama

<table>
<tr>
<th>Penggunaan</th>
<th>Font</th>
<th>Contoh</th>
</tr>
<tr>
<td>Heading</td>
<td>Poppins Bold</td>
<td><h1 style="font-family: Poppins; font-weight: 700">Aa Bb Cc</h1></td>
</tr>
<tr>
<td>Body Text</td>
<td>Poppins Regular</td>
<td><p style="font-family: Poppins;">Aa Bb Cc</p></td>
</tr>
<tr>
<td>Alternative</td>
<td>Arial, Helvetica, sans-serif</td>
<td><p style="font-family: Arial;">Aa Bb Cc</p></td>
</tr>
</table>

## 📏 Hierarki & Ukuran

{% tabs %}
{% tab title="Headings" %}
### H1: Judul Utama
- Ukuran: 32–40px
- Weight: Bold
- Use case: Halaman utama, judul artikel

### H2: Subjudul
- Ukuran: 24–28px
- Weight: Semi-bold
- Use case: Bagian utama, section breaks

### H3: Section
- Ukuran: 18–20px
- Weight: Medium
- Use case: Sub-section, grup konten
{% endtab %}

{% tab title="Body Text" %}
### Body Text
- Ukuran: 14–16px
- Weight: Regular
- Line height: 1.5
- Use case: Paragraf utama, deskripsi

### Small Text
- Ukuran: 12px
- Weight: Regular
- Use case: Caption, footnote, metadata
{% endtab %}
{% endtabs %}

## 🎨 Best Practices

{% hint style="warning" %}
### Case Usage
- Gunakan **Sentence case** untuk hampir semua konten
- ALL CAPS hanya untuk:
  - Akronim (NASA, WHO)
  - Logo type
  - CTA khusus
{% endhint %}

## 📱 Responsive Behavior

| Breakpoint | H1 | H2 | H3 | Body |
|------------|----|----|----|----|
| Desktop    | 40px | 28px | 20px | 16px |
| Tablet     | 36px | 24px | 18px | 16px |
| Mobile     | 32px | 22px | 18px | 14px |

{% hint style="success" %}
**Pro Tips:**
- Selalu test keterbacaan pada berbagai ukuran layar
- Gunakan relative units (rem) untuk scaling yang lebih baik
- Pastikan contrast ratio minimal 4.5:1 untuk accessibility
{% endhint %}
