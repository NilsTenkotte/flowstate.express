# Flowstate Express — Design Tokens
Quelle: Flowstate_Express_Brand_Guideline.pdf v0.1 (Juni 2026)

## Fonts
| Rolle | Font | Gewichte |
|---|---|---|
| Display / Headlines | Fraunces | Light, Regular, SemiBold, Black |
| Body / Interface | DM Sans | Light, Regular, Medium, Bold |
| Accent / Quotes | Caveat | Medium, Bold |

## Colours
| Name | Hex | RGB | Rolle |
|---|---|---|---|
| Sky | #4DD2F6 | 77, 210, 246 | Wahrnehmung · Weite |
| Orange | #FF7A2E | 255, 122, 46 | Ausdruck · Primary CTA |
| Fire | #FB343B | 251, 52, 59 | Gefühl · sparsam einsetzen |
| Creme | #FAF1E6 | 250, 241, 230 | Bühne · Hintergrund (Light Mode) |
| Atelier | #1C1130 | 28, 17, 48 | Rückzug · Dark Mode Background |
| White | #FFFFFF | 255, 255, 255 | Leerraum |
| Text | #111827 | 17, 24, 39 | Fließtext / UI |
| Muted | #6B7280 | 107, 114, 128 | Sekundäre Labels |

## Signature Gradient
Linear: Sky (#4DD2F6) → Orange (#FF7A2E) → Fire (#FB343B)
Einsatz: sparsam, für Bühnen-Momente (Hero, Signature-Elemente) — nicht als Flächenfüllung im UI.

## Logo
- 4 Varianten: Light/Default, Symbol/Favicon (nur Symbol, ohne Wortmarke), Atelier/Dark, Signature Gradient
- Clearspace: mind. halbe Symbol-Höhe rundherum, frei von Text/Grafik
- Mindestgröße: 32px (digital) / 12mm (print)
- Bei kleinen Anwendungen (Favicon, App-Icon, Avatar): ausschließlich Symbol, keine Wortmarke

## Tailwind-Vorschlag (als Ausgangspunkt, nicht bindend)
```js
colors: {
  sky: '#4DD2F6',
  orange: '#FF7A2E',
  fire: '#FB343B',
  creme: '#FAF1E6',
  atelier: '#1C1130',
  text: '#111827',
  muted: '#6B7280',
},
fontFamily: {
  display: ['Fraunces', 'serif'],
  body: ['DM Sans', 'sans-serif'],
  accent: ['Caveat', 'cursive'],
}
```
