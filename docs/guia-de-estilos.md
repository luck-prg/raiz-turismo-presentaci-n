# Guía de estilos — Presentación Raíz Turismo

Estilo **Moderno Minimalista**, modo claro, pensado para proyectar en aula.
Formato: 1920 × 1080 px (16:9). Todo en español.

---

## 1. Color

| Rol | Hex | Uso |
|---|---|---|
| Fondo principal | `#fbfbf9` | Casi-blanco cálido. Fondo por defecto de las slides. |
| Fondo alterno | `#eef1e8` | Salvia muy claro. Para dar ritmo (1 de cada ~3 slides). |
| Panel/tarjeta | `#f1f1ea` | Bloques y tarjetas sobre fondo principal. |
| Panel sobre alterno | `#fbfbf9` | Tarjetas cuando el fondo es `#eef1e8`. |
| Tinta principal | `#111111` | Títulos y números grandes. |
| Tinta secundaria | `#3a3d38` | Cuerpo de texto. |
| Gris apagado | `#767a72` | Etiquetas, subtítulos, pies. |
| Gris texto en tarjeta | `#5a5f55` | Descripciones dentro de tarjetas. |
| **Acento salvia** | `#7c8f6b` | Eyebrows, signos, highlights, barras. |
| Acento salvia oscuro | `#5f7050` | Números clave, slide de cierre, texto de énfasis. |
| Bordes/reglas | `#e2e2d6` · `#dcdccf` · `#d6dccb` | Líneas divisorias finas. |

**Escala de barras** (gráficos), de claro a oscuro:
`#cdd7c0` → `#b6c3a4` → `#9aad84` → `#84996d` → `#5f7050`

Sin gradientes. Sin sombras. Sin emojis.

---

## 2. Tipografía

Única familia: **Space Grotesk** (Google Fonts, pesos 400/500/600/700).

```
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
```

| Elemento | Tamaño | Peso | Extra |
|---|---|---|---|
| Título portada / cierre | 96–104px | 500 | `letter-spacing:-.025em; line-height:1.0` |
| Título de sección | 62–76px | 500 | `letter-spacing:-.02em; line-height:1.04` |
| Número mega (métrica hero) | 130–200px | 600 | `letter-spacing:-.03/-.04em; line-height:.82–.9` |
| Número grande (tarjeta) | 60–104px | 600 | `letter-spacing:-.02/-.03em` |
| Eyebrow (etiqueta superior) | 30px | 600 | `letter-spacing:.14em; text-transform:uppercase; color:#7c8f6b` |
| Cuerpo | 34–40px | 400 | `line-height:1.35–1.4; color:#3a3d38` |
| Texto en tarjeta | 26–31px | 400 | `line-height:1.35; color:#5a5f55` |
| Pie / dato menor | 28–30px | 400 | `color:#767a72` |
| Wordmark | 38px | 700 | `letter-spacing:-.01em` |

**Nunca** bajar de 26px (mínimo de legibilidad en aula).

---

## 3. Layout de slide

- Padding estándar: `100px 120px` (usar `90px` arriba/abajo en slides muy densas).
- Cada `<section>` es `display:flex; flex-direction:column; justify-content:space-between` — el contenido se reparte de arriba a abajo, dejando aire.
- Estructura recurrente: **eyebrow + título** arriba → bloque de datos al medio → cierre/nota abajo.
- Radio de tarjetas: `18–22px`. Padding interno de tarjeta: `40–56px`.
- Separación entre tarjetas: `gap:24–40px`.

### Encabezado de sección (patrón fijo)

```html
<p style="margin:0 0 20px; font-family:'Space Grotesk'; font-weight:600; font-size:30px;
   letter-spacing:.14em; text-transform:uppercase; color:#7c8f6b;">EL PROBLEMA</p>
<h2 style="margin:0; font-family:'Space Grotesk'; font-weight:500; font-size:76px;
   line-height:1.04; letter-spacing:-.02em; color:#111;">Título de la slide.</h2>
```

### Tarjeta de dato

```html
<div style="flex:1; background:#f1f1ea; border-radius:20px; padding:48px;">
  <div style="font-weight:600; font-size:32px; color:#5f7050; margin-bottom:20px;">Rótulo</div>
  <p style="margin:0; font-size:34px; line-height:1.4; color:#3a3d38;">Contenido.</p>
</div>
```

### Gráfico de barras (columnas)

Barras = `<div>` con ancho 100% dentro de columna flex, altura en px proporcional al valor, `border-radius:8px 8px 0 0`, color de la escala salvia. Valor arriba (600), etiqueta de eje abajo (`#767a72`). La barra mayor usa `#5f7050`.

---

## 4. Ritmo de fondos

Alternar para dar variedad, sin salir del modo claro:

- Mayoría de slides: `#fbfbf9`.
- Slides de respiro (Qué es, Diferenciadores, La inversión, Riesgo, Por qué invertir): `#eef1e8`.
- **Slide de cierre "El pedido"**: fondo salvia oscuro `#5f7050` con texto `#fbfbf9`/`#fff` — único fondo saturado de todo el deck, reservado para el remate.

---

## 5. Copywriting

- Títulos = frases-tópico cortas y declarativas, en tono sobrio (nada de suspenso ni "punchlines").
- Números siempre destacados en tinta principal o salvia oscuro; el texto que los acompaña, en gris.
- Formato de cifras: `USD 71.430`, `TIR 63%`, `3,3 años` (coma decimal, punto de miles — convención AR).
- Un dato por bloque; evitar saturar. Mucho aire.

---

## 6. Secuencia de slides (16)

1. Portada · 2. El problema · 3. La oportunidad · 4. Qué es Raíz · 5. El ecosistema (4 actores A/B/C/D) · 6. Cómo ganamos dinero · 7. Diferenciadores · 8. El mercado en números (TAM/SAM) · 9. Plan de captación (barras) · 10. La inversión · 11. El retorno (métrica hero + barras) · 12. Frente a las alternativas (barras horizontales) · 13. Riesgo acotado · 14. Impacto en la región · 15. Por qué invertir · 16. El pedido (cierre salvia).

Acentos de color por actor/segmento: la tarjeta del **inversor** (Segmento D) se pinta en salvia `#7c8f6b` con texto claro, para destacarla frente a las otras tres.
