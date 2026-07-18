# Task 3 · Temperature Converter

An interactive Celsius / Fahrenheit / Kelvin temperature converter with real-time input validation, simultaneous multi-unit results, and a 3D animated thermometer gauge that visually reflects the value. Built with vanilla HTML, CSS, and JavaScript — no libraries or frameworks.

## File

- `temp-converter.html` — the entire tool (HTML + embedded CSS + inline `<script>`)

## How it works

1. Type a numeric value into the input field.
2. Pick which unit that value is in (°C / °F / K) using the segmented control.
3. Click **Convert** (or press **Enter**).
4. All three units (Celsius, Fahrenheit, Kelvin) display at once, with the tile matching your chosen input unit highlighted.
5. A glass-and-mercury thermometer graphic fills and shifts color (blue → red) to visually represent the value.

## Validation & edge cases

- **Live validation while typing:** only digits, one decimal point, and a leading minus sign are allowed — anything else shows an inline error immediately.
- **Empty input:** shows "Please enter a temperature value."
- **Non-numeric input on Convert:** shows "Please enter a valid number…" and blocks calculation.
- **Below absolute zero:** the entered value is converted to Celsius internally and checked against −273.15°C. If it's lower, a friendly message explains absolute zero instead of showing a nonsensical result — this check works no matter which unit you entered in (e.g. entering `-500` in Fahrenheit is still correctly caught).
- Note: the thermometer graphic's fill is visually clamped to a −50°C–110°C display range so extreme values don't break the gauge artwork — the actual numeric results shown in the tiles are **never** clamped or altered.

## Design

- **Layout:** centered card on a dark gradient-mesh background, so the light card reads with real depth
- **3D touches:**
  - The whole card gently tilts toward your cursor (subtle `rotateX`/`rotateY` on mousemove; disabled on touch devices and when `prefers-reduced-motion` is set)
  - Neumorphic inset shadows on the input and unit selector (embossed/pressed look)
  - The Convert button has a glossy gradient and physically "presses down" on click
  - The thermometer uses SVG linear/radial gradients for a glass-tube and glass-bulb look, with a highlight streak and a mercury color that blends from blue to red based on the value
- **Typography:** Space Grotesk (heading), Inter (body/labels), JetBrains Mono (numeric input, results, gauge caption)
- **Palette:** neutral parchment card (`#F4F2ED`), ink (`#20232A`), cold blue (`#3B7DC4`) and hot red (`#D1495B`) as the two temperature-driven accents

## Responsiveness

At `700px` and below: the card switches to a single column, the thermometer moves above the form and shrinks, result tiles stack vertically, and the 3D tilt effect is disabled (since there's no mouse on touch devices).

## How to run

Open `temp-converter.html` directly in any browser — everything is self-contained, no build step or server required.

## Checklist coverage

- [x] Numeric input with validation (rejects non-numeric input, shows error message)
- [x] Unit selector (segmented radio control: °C / °F / K)
- [x] All output units shown simultaneously (auto-conversion on Convert)
- [x] Convert button triggers calculation (Enter key also works)
- [x] Result display area with correct unit labels
- [x] Absolute zero edge case handled with a friendly message
- [x] Clean, centered UI with clear labels