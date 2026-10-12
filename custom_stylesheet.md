/* ==========================================================================
   PART A — CSS3 Fundamentals & Box Model
   ========================================================================== */

:root {
    --color-bg-card: #ffffff;
    --color-primary: #0f172a;
    --color-accent: #f59e0b;
    --color-text-main: #334155;
    --border-radius: 12px;
    --spacing-unit: 1.5rem;
}

.container-main {
    max-width: 1100px;
    margin: 0 auto;
    padding: var(--spacing-unit);
}

.section-card {
    background-color: var(--color-bg-card);
    border: 1px solid #e2e8f0;
    border-radius: var(--border-radius);
    padding: var(--spacing-unit);
    margin-bottom: 2rem;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
}

h2 {
    color: var(--color-primary);
    font-size: 1.5rem;
    margin-bottom: 1rem;
    border-bottom: 2px solid #f1f5f9;
    padding-bottom: 0.5rem;
}

/* ==========================================================================
   PART B — Flexbox Layout
   ========================================================================== */

.hero-flex {
    display: flex;
    flex-direction: column; /* Mobile-first default */
    align-items: center;
    gap: 1.5rem;
    justify-content: center;
}

.profile-img {
    width: 130px;
    height: 130px;
    border-radius: 50%;
    border: 4px solid var(--color-accent);
    object-fit: cover;
}

.hero-content {
    text-align: center;
}

.subtitle {
    color: #64748b;
    font-weight: 600;
    margin-bottom: 0.5rem;
}

/* ==========================================================================
   PART C — CSS Grid Layout
   ========================================================================== */

.grid-skills,
.grid-projects {
    display: grid;
    /* Mobile-first: single full-width column */
    grid-template-columns: 1fr;
    gap: 1.25rem;
}

.skill-card,
.project-card {
    background-color: #f8fafc;
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    padding: 1rem;
    transition: transform 0.2s ease;
}

.skill-card:hover,
.project-card:hover {
    transform: translateY(-2px);
}

.skill-card h3,
.project-card h3 {
    color: var(--color-primary);
    margin-bottom: 0.25rem;
}

/* ==========================================================================
   PART D — Responsive Design & Media Queries (Mobile-First)
   ========================================================================== */

/* Tablet Breakpoint (~768px) */
@media screen and (min-width: 768px) {
    .hero-flex {
        flex-direction: row;
        text-align: left;
        align-items: flex-start;
    }

    .hero-content {
        text-align: left;
    }

    .grid-skills {
        grid-template-columns: repeat(3, 1fr);
    }

    .grid-projects {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Desktop Breakpoint (~1280px) */
@media screen and (min-width: 1280px) {
    .grid-projects {
        grid-template-columns: repeat(3, 1fr);
    }

    .container-main {
        padding-left: 0;
        padding-right: 0;
    }
}