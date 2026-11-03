# Keepsake — Landing Page
Live Demo [https://udalovivanw.github.io/landing-keepsake/](https://udalovivanw.github.io/landing-keepsake/)
---

## Технології

- **HTML5**: Семантична структура (`header`, `nav`, `main`, `section`, `article`, `footer`, `form`), ARIA-атрибути
- **CSS3**: Змінні `:root`, Flexbox, CSS Grid, Media Queries
- **Шрифти**: Google Fonts (Oswald, Open Sans, Dancing Script) з `font-display: swap`
- **Графіка**: Вбудовані інлайн SVG-іконки, WebP-зображення з `loading="lazy"`

---

## Структура макета та CSS-розкладка (Flex / Grid)

- **Header (`.header-container`)**: `Flexbox`, `flex-direction: row`, `align-items: center`, `justify-content: space-between`.
- **Hero (`.hero`)**: `Flexbox`, `flex-direction: column`, `align-items: flex-start`
- **Works Grid (`.works-grid`)**: `CSS Grid`
  - Mobile: 1 колонка (`grid-template-columns: 1fr`)
  - Tablet: 2 колонки (`repeat(2, 1fr)`).
  - Desktop: 3 колонки (`repeat(3, 1fr)`).
- **Filter Chips (`.filter-chips`)**: `Flexbox`, `flex-direction: row`:
  - Mobile: `flex-wrap: nowrap` із горизонтальною прокруткою.
  - Tablet / Desktop: `flex-wrap: wrap`, `justify-content: flex-end`.
- **Services (`.services-grid`)**: `Flexbox`, `flex-direction: row`, `flex-wrap: wrap`:
  - Mobile / Tablet: 2 в рядок (`width: calc((100% - 24px) / 2)`).
  - Desktop: 4 в рядок (`width: calc((100% - 3 * 24px) / 4)`).
- **Stats (`.stats-grid`)**: `Flexbox`, `flex-direction: row`, `flex-wrap: wrap`:
  - Mobile: 2×2 (`width: 50%`).
  - Tablet / Desktop: 4 в рядок (`width: 25%`).
- **Journal (`.journal-grid`)**: `Flexbox`, `flex-direction: row`, `flex-wrap: wrap`, `gap: 40px`:
  - Mobile / Tablet: 1 колонка (`width: 100%`).
  - Desktop: 2 колонки (`width: calc((100% - 40px) / 2)`).
- **Clients (`.client-logos`)**: `Flexbox`, `flex-direction: row`, `flex-wrap: wrap:
  - Mobile: 2 в рядок (`width: 50%`).
  - Tablet: 3 в рядок (`width: 33.333%`).
  - Desktop: 6 в рядок (`width: 16.666%`).
- **Newsletter Form (`.newsletter-form`)**: `Flexbox`, `flex-direction: column`, `gap: 14px.
- **Footer Top (`.footer-top`)**: `Flexbox`:
  - Mobile: `flex-direction: column.
  - Tablet / Desktop: `flex-direction: row`, `justify-content: space-between`.

---

## Інтерактивність та стани

- **Newsletter Form**: підтримка станів Default, Focus (`border: 1px solid var(--color-teal)`), Error (`:user-invalid` + `:has()`) та Success (приховання форми через `:target`).
- **Hover & Focus на картках**: оверлей показується при `:hover`, `:focus-visible` та `:focus-within`.
- **Мобільне меню та фільтрація**: реалізовано без JavaScript - використано `checkbox` / `radio` та псевдоклас `:checked`.
- **Кнопка «Вгору»**: `position: fixed`, розмір 44×44px, доступна на всіх брекпоінтах.

---

## Структура проєкту

```text
landing-keepsake/
├── index.html
├── style.css
├── README.md
└── images/
    ├── 1.webp
    ├── 2.webp
    └── validator w3 result.png