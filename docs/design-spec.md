# Soc Ops Bingo — Design Spec

## Design Rationale: 3D Shiny Lavender Buttons

- **Theme:** Playful, tactile, and modern with a soft lavender pastel palette.
- **Buttons:** All interactive elements (buttons, clickable divs, modal actions) use a 3D, shiny style for visual delight and accessibility.
- **Techniques:**
  - Layered box-shadows for depth
  - Gradients and gloss overlays for shine
  - Animated highlight for extra pop
  - Responsive, accessible, and keyboard-friendly
- **Primary Color:** Lavender (#b57cf6)
- **Accent Colors:** Soft white, pale blue, gentle pinks for highlights and shadows

## Example CSS Snippet

```css
.lavender-3d-btn {
  @apply px-6 py-2 rounded-xl font-bold shadow-[0_4px_0_0_#a78bfa] bg-gradient-to-b from-[#e9d8fd] to-[#b57cf6] border-2 border-[#a78bfa] text-[#4b2994] transition-all duration-200 ease-in-out relative overflow-hidden;
}
.lavender-3d-btn::after {
  content: '';
  position: absolute;
  left: 0; top: 0; right: 0; height: 45%;
  background: linear-gradient(90deg,rgba(255,255,255,0.5),rgba(255,255,255,0.1));
  border-radius: inherit;
  pointer-events: none;
}
.lavender-3d-btn:active {
  @apply shadow-inner scale-95 brightness-105;
}
.lavender-3d-btn:focus-visible {
  @apply ring-2 ring-[#c4b5fd] ring-offset-2;
}
```

---

- Use this class (or similar Tailwind+custom CSS) for all interactive elements.
- Adjust color tokens in index.css for consistency.
- Test for color contrast and keyboard navigation.
