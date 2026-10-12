# Profile & Mini-Portfolio Page (Practical Assignment 2)

**Course:** Web Technologies (CIS2103)  
**Programme:** SE & CIS – Year 2, Sem 1  
**Institution:** Africa University  
**Lecturer:** Ms. Elizabeth Mafu  

---

## Responsive Notes

### 1. Tested Breakpoints
The page was systematically tested across three core viewport dimensions using browser developer tools:
- **Mobile (~375px):** Content flows in a single stacked column with generous padding, custom button styling, and vertical navigation stack.
- **Tablet (~768px):** The hero layout shifts horizontally via custom flex directives, skills arrange in 3 columns, and form fields split into two equal-width columns using Tailwind responsive prefixes (`sm:` / `md:`).
- **Desktop (~1280px):** Full-width layout centered with `max-width`, 3-column project grid distribution, and fixed top navigation.

### 2. Layout Strategy: Flexbox vs. CSS Grid
- **Flexbox (`.hero-flex` & Navigation):** Applied for one-dimensional layouts where alignment and content alignment along an axis are required. Utilizes `display: flex`, `flex-direction`, `align-items`, `gap`, and `justify-content`.
- **CSS Grid (`.grid-skills`, `.grid-projects`):** Applied for multi-column structured grid views. Utilizes `repeat()`, `1fr` fraction units, and `gap` spacing to build scalable responsive layouts without requiring extra inline styling.

### 3. Tailwind Utility-First Integration
- **Header Section (`<header>`):** Rebuilt using utility classes (`bg-slate-900`, `flex-col`, `md:flex-row`, `space-x-6`) leveraging responsive variant breakpoints (`md:`).
- **Contact Form (`#contact`):** Form container and elements use Tailwind utilities (`bg-white`, `rounded-xl`, `shadow-md`, `focus:ring-2`, `sm:flex-row`).
- **CSS/Tailwind Split Rationale:** Core grid structures and base CSS box-model styling reside in `css/style.css` to demonstrate native CSS master concepts, whereas interactive dynamic components use Tailwind CSS utilities for rapid and scalable presentation.