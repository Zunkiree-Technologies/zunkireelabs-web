# Zunkiree Labs Design System & Style Guide

A comprehensive design system for the Zunkiree Labs website, featuring a clean light theme with bold red (#eb1600) brand accents.

---

## Brand Overview

**Primary Brand Color:** `#eb1600` (Zunkiree Red)
**Theme:** Light, professional, modern
**Inspiration:** Databricks-style clean enterprise design

---

## Color Palette

### Primary Colors (Zunkiree Red)

| Token | Hex | Usage |
|-------|-----|-------|
| `zunkiree-50` | `#fff1f0` | Light backgrounds, hover states |
| `zunkiree-100` | `#ffe1df` | Light borders, subtle backgrounds |
| `zunkiree-200` | `#ffc9c5` | Disabled button backgrounds |
| `zunkiree-300` | `#ffa299` | Light accents |
| `zunkiree-400` | `#ff6b5c` | Secondary accents |
| `zunkiree-500` | `#ff3d2a` | Lighter primary variant |
| `zunkiree-600` | `#eb1600` | **Main brand color** - CTAs, links |
| `zunkiree-700` | `#c21200` | Hover states for buttons |
| `zunkiree-800` | `#a01410` | Active/pressed states |
| `zunkiree-900` | `#841815` | Dark accents |
| `zunkiree-950` | `#480806` | Darkest - text on light bg |

### Neutral Colors (Grays)

| Token | Hex | Usage |
|-------|-----|-------|
| `gray-50` | `#f9fafb` | Page background, section alternates |
| `gray-100` | `#f3f4f6` | Card backgrounds, inputs |
| `gray-200` | `#e5e7eb` | Borders, dividers |
| `gray-300` | `#d1d5db` | Disabled states |
| `gray-400` | `#9ca3af` | Placeholder text |
| `gray-500` | `#6b7280` | Secondary text, captions |
| `gray-600` | `#4b5563` | Body text (light) |
| `gray-700` | `#374151` | Body text (default) |
| `gray-800` | `#1f2937` | Headings, emphasis |
| `gray-900` | `#111827` | Primary text, titles |
| `gray-950` | `#030712` | Darkest text, dark sections |

### Semantic Colors

| Purpose | Color | Hex |
|---------|-------|-----|
| Success | Green | `#22c55e` |
| Warning | Amber | `#f59e0b` |
| Error | Red | `#ef4444` |
| Info | Blue | `#3b82f6` |

---

## Typography

### Font Stack

```css
/* Primary font for all text */
font-family: 'DM Sans', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;

/* Monospace for code */
font-family: 'DM Mono', 'Fira Code', 'Consolas', monospace;
```

### Font Weights

| Weight | Usage |
|--------|-------|
| 400 (Regular) | Body text, paragraphs |
| 500 (Medium) | Subtle emphasis, labels |
| 600 (Semibold) | Subheadings, buttons |
| 700 (Bold) | Headings, strong emphasis |

### Type Scale

| Element | Size (Desktop) | Line Height | Weight |
|---------|----------------|-------------|--------|
| Display | 72px (4.5rem) | 1.1 | 700 |
| H1 | 48px (3rem) | 1.2 | 700 |
| H2 | 36px (2.25rem) | 1.25 | 700 |
| H3 | 24px (1.5rem) | 1.35 | 600 |
| H4 | 20px (1.25rem) | 1.4 | 600 |
| Body | 16px (1rem) | 1.5 | 400 |
| Body Large | 18px (1.125rem) | 1.6 | 400 |
| Small | 14px (0.875rem) | 1.5 | 400 |
| Caption | 12px (0.75rem) | 1.4 | 500 |

### Tailwind Classes

```html
<!-- Display -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900">Display</h1>

<!-- H1 -->
<h1 class="text-4xl md:text-5xl font-bold text-gray-900">Heading 1</h1>

<!-- H2 -->
<h2 class="text-3xl md:text-4xl font-bold text-gray-900">Heading 2</h2>

<!-- H3 -->
<h3 class="text-xl md:text-2xl font-semibold text-gray-800">Heading 3</h3>

<!-- Body -->
<p class="text-base text-gray-700 leading-relaxed">Body text</p>

<!-- Small -->
<p class="text-sm text-gray-500">Small text</p>
```

---

## Spacing System

Based on an 8px grid for consistent rhythm.

| Token | Size | Tailwind |
|-------|------|----------|
| 1 | 8px | `p-2`, `m-2` |
| 2 | 16px | `p-4`, `m-4` |
| 3 | 24px | `p-6`, `m-6` |
| 4 | 32px | `p-8`, `m-8` |
| 5 | 40px | `p-10`, `m-10` |
| 6 | 48px | `p-12`, `m-12` |
| 8 | 64px | `p-16`, `m-16` |
| 10 | 80px | `p-20`, `m-20` |
| 12 | 96px | `p-24`, `m-24` |

### Section Spacing

```html
<!-- Standard section -->
<section class="py-16 lg:py-24">

<!-- Large section (hero, CTA) -->
<section class="py-20 lg:py-32">

<!-- Compact section -->
<section class="py-12 lg:py-16">
```

---

## Layout

### Container

```html
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
  <!-- Content -->
</div>
```

- Max width: 1280px (max-w-7xl)
- Horizontal padding: 16px mobile, 24px tablet, 32px desktop

### Grid System

```html
<!-- 12-column grid -->
<div class="grid grid-cols-12 gap-6">
  <div class="col-span-12 md:col-span-6 lg:col-span-4">Column</div>
</div>

<!-- Common layouts -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">Cards</div>
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">Two columns</div>
<div class="grid grid-cols-1 lg:grid-cols-3 gap-8">Three columns</div>
```

---

## Components

### Buttons

#### Primary Button
```html
<button class="inline-flex items-center justify-center gap-2 px-6 py-3 bg-zunkiree-600 text-white font-semibold rounded-lg hover:bg-zunkiree-700 transition-all duration-200 shadow-sm hover:shadow-md">
  Get Started
</button>
```

#### Secondary Button
```html
<button class="inline-flex items-center justify-center gap-2 px-6 py-3 bg-white text-zunkiree-600 font-semibold rounded-lg border-2 border-zunkiree-600 hover:bg-zunkiree-50 transition-all duration-200">
  Learn More
</button>
```

#### Outline Button
```html
<button class="inline-flex items-center justify-center gap-2 px-6 py-3 bg-transparent text-gray-700 font-semibold rounded-lg border border-gray-300 hover:border-gray-400 hover:bg-gray-50 transition-all duration-200">
  View Details
</button>
```

#### Ghost Button
```html
<button class="inline-flex items-center justify-center gap-2 px-4 py-2 text-zunkiree-600 font-medium hover:bg-zunkiree-50 rounded-lg transition-all duration-200">
  Learn More <span>&rarr;</span>
</button>
```

#### Button Sizes

| Size | Padding | Font Size |
|------|---------|-----------|
| Small | `px-4 py-2` | `text-sm` |
| Default | `px-6 py-3` | `text-base` |
| Large | `px-8 py-4` | `text-lg` |

### Cards

#### Basic Card
```html
<div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6 hover:shadow-md transition-shadow duration-200">
  <h3 class="text-xl font-semibold text-gray-900 mb-2">Card Title</h3>
  <p class="text-gray-600">Card description goes here.</p>
</div>
```

#### Card with Hover Lift
```html
<div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6 hover:shadow-lg hover:-translate-y-1 transition-all duration-300">
  <!-- Content -->
</div>
```

#### Service Card
```html
<div class="bg-white rounded-xl shadow-sm border border-gray-200 p-8 group hover:shadow-lg hover:border-zunkiree-200 transition-all duration-300">
  <div class="w-12 h-12 bg-zunkiree-100 rounded-lg flex items-center justify-center text-zunkiree-600 mb-6 group-hover:bg-zunkiree-600 group-hover:text-white transition-colors duration-300">
    <!-- Icon -->
  </div>
  <h3 class="text-xl font-semibold text-gray-900 mb-3">Service Title</h3>
  <p class="text-gray-600 mb-4">Service description.</p>
  <a href="#" class="text-zunkiree-600 font-medium inline-flex items-center gap-1 hover:gap-2 transition-all">
    Learn more <span>&rarr;</span>
  </a>
</div>
```

#### Testimonial Card
```html
<div class="bg-white rounded-xl shadow-sm border border-gray-200 p-8">
  <div class="flex items-center gap-1 mb-4">
    <!-- 5 stars -->
    <svg class="w-5 h-5 text-yellow-400 fill-current">...</svg>
  </div>
  <blockquote class="text-gray-700 text-lg mb-6">
    "Quote text here..."
  </blockquote>
  <div class="flex items-center gap-4">
    <img src="avatar.jpg" class="w-12 h-12 rounded-full" alt="">
    <div>
      <p class="font-semibold text-gray-900">Name</p>
      <p class="text-sm text-gray-500">Title, Company</p>
    </div>
  </div>
</div>
```

### Navigation

#### Header
```html
<header class="fixed top-0 left-0 right-0 z-50 bg-white/80 backdrop-blur-md border-b border-gray-200">
  <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex items-center justify-between h-16 lg:h-20">
      <!-- Logo -->
      <a href="/" class="flex items-center gap-2">
        <img src="/logo.svg" alt="Zunkiree Labs" class="h-8">
      </a>

      <!-- Nav Links -->
      <div class="hidden lg:flex items-center gap-8">
        <a href="/about" class="text-gray-600 hover:text-gray-900 font-medium transition-colors">About</a>
        <a href="/services" class="text-gray-600 hover:text-gray-900 font-medium transition-colors">Services</a>
        <a href="/projects" class="text-gray-600 hover:text-gray-900 font-medium transition-colors">Projects</a>
        <a href="/contact" class="text-zunkiree-600 hover:text-zunkiree-700 font-medium transition-colors">Contact</a>
      </div>

      <!-- CTA -->
      <a href="/contact" class="hidden lg:inline-flex px-5 py-2.5 bg-zunkiree-600 text-white font-semibold rounded-lg hover:bg-zunkiree-700 transition-colors">
        Get Started
      </a>
    </div>
  </nav>
</header>
```

### Form Elements

#### Text Input
```html
<div>
  <label class="block text-sm font-medium text-gray-700 mb-2">Label</label>
  <input type="text" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-zunkiree-500 focus:ring-2 focus:ring-zunkiree-500/20 outline-none transition-all" placeholder="Placeholder">
</div>
```

#### Textarea
```html
<textarea class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-zunkiree-500 focus:ring-2 focus:ring-zunkiree-500/20 outline-none transition-all resize-none" rows="4"></textarea>
```

#### Select
```html
<select class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-zunkiree-500 focus:ring-2 focus:ring-zunkiree-500/20 outline-none transition-all bg-white">
  <option>Option 1</option>
</select>
```

### Tags/Badges

```html
<!-- Primary Tag -->
<span class="inline-flex items-center px-3 py-1 text-sm font-medium bg-zunkiree-100 text-zunkiree-700 rounded-full">
  Tag
</span>

<!-- Neutral Tag -->
<span class="inline-flex items-center px-3 py-1 text-sm font-medium bg-gray-100 text-gray-700 rounded-full">
  Tag
</span>

<!-- Success Tag -->
<span class="inline-flex items-center px-3 py-1 text-sm font-medium bg-green-100 text-green-700 rounded-full">
  Active
</span>
```

---

## Shadows

| Name | CSS | Usage |
|------|-----|-------|
| `shadow-sm` | `0 1px 2px rgba(0,0,0,0.05)` | Subtle depth |
| `shadow` | `0 1px 3px rgba(0,0,0,0.1)` | Default cards |
| `shadow-md` | `0 4px 6px rgba(0,0,0,0.07)` | Elevated cards |
| `shadow-lg` | `0 10px 15px rgba(0,0,0,0.1)` | Modals, dropdowns |
| `shadow-xl` | `0 20px 25px rgba(0,0,0,0.1)` | Prominent elements |

### Custom Shadows

```css
/* Card shadow */
.shadow-card {
  box-shadow: 0 4px 24px rgba(0, 0, 0, 0.06);
}

/* Hover shadow */
.shadow-hover {
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.12);
}

/* Button shadow */
.shadow-btn {
  box-shadow: 0 4px 14px rgba(235, 22, 0, 0.25);
}
```

---

## Border Radius

| Token | Size | Usage |
|-------|------|-------|
| `rounded-sm` | 4px | Small elements |
| `rounded` | 6px | Inputs, small buttons |
| `rounded-md` | 8px | Tags, chips |
| `rounded-lg` | 12px | Buttons, inputs |
| `rounded-xl` | 16px | Cards |
| `rounded-2xl` | 24px | Large cards, modals |
| `rounded-full` | 9999px | Pills, avatars |

---

## Animations

### Transition Defaults

```html
<!-- Standard transition -->
<div class="transition-all duration-200">

<!-- Slow transition -->
<div class="transition-all duration-300">

<!-- Fast transition -->
<div class="transition-colors duration-150">
```

### Hover Effects

```html
<!-- Scale up -->
<div class="hover:scale-105 transition-transform duration-200">

<!-- Lift up -->
<div class="hover:-translate-y-1 transition-transform duration-200">

<!-- Shadow increase -->
<div class="hover:shadow-lg transition-shadow duration-200">
```

### Scroll Animations (GSAP)

```javascript
// Fade up on scroll
gsap.from('[data-reveal]', {
  scrollTrigger: {
    trigger: '[data-reveal]',
    start: 'top 80%'
  },
  y: 30,
  opacity: 0,
  duration: 0.6,
  ease: 'power2.out'
});
```

---

## Responsive Breakpoints

| Breakpoint | Min Width | Usage |
|------------|-----------|-------|
| `sm` | 640px | Large phones |
| `md` | 768px | Tablets |
| `lg` | 1024px | Small laptops |
| `xl` | 1280px | Desktops |
| `2xl` | 1536px | Large screens |

### Common Patterns

```html
<!-- Hide on mobile, show on desktop -->
<div class="hidden lg:block">Desktop only</div>

<!-- Stack on mobile, row on desktop -->
<div class="flex flex-col lg:flex-row">

<!-- Responsive text size -->
<h1 class="text-3xl md:text-4xl lg:text-5xl">

<!-- Responsive grid -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
```

---

## Accessibility

### Color Contrast

All text must meet WCAG 2.1 AA standards:
- Normal text: 4.5:1 contrast ratio minimum
- Large text (18px+ or 14px+ bold): 3:1 minimum

### Focus States

```html
<button class="focus:outline-none focus:ring-2 focus:ring-zunkiree-500 focus:ring-offset-2">
```

### Keyboard Navigation

- All interactive elements must be focusable
- Tab order should follow visual order
- Focus indicators must be visible

### Screen Readers

```html
<!-- Decorative icons -->
<svg aria-hidden="true">

<!-- Skip link -->
<a href="#main" class="sr-only focus:not-sr-only">Skip to content</a>

<!-- Descriptive labels -->
<button aria-label="Close menu">
```

---

## Icon Usage

Use Heroicons (outline style) for consistency.

### Icon Sizes

| Context | Size | Tailwind |
|---------|------|----------|
| Inline with text | 20px | `w-5 h-5` |
| Buttons | 20px | `w-5 h-5` |
| Cards | 24px | `w-6 h-6` |
| Feature icons | 48px | `w-12 h-12` |

### Icon Colors

```html
<!-- Primary icon -->
<svg class="w-6 h-6 text-zunkiree-600">

<!-- Secondary icon -->
<svg class="w-6 h-6 text-gray-500">

<!-- Icon in button -->
<button class="inline-flex items-center gap-2">
  <svg class="w-5 h-5">...</svg>
  Button Text
</button>
```

---

## Section Patterns

### Hero Section
- Full viewport height or large padding
- Bold headline with subtext
- 1-2 CTA buttons
- Optional visual element (illustration, image, animation)

### Alternating Sections
- Alternate between white (`bg-white`) and light gray (`bg-gray-50`)
- Creates visual separation without heavy dividers

### Dark Section (Accent)
- Use for CTA sections or to create contrast
- Dark background (`bg-gray-900` or `bg-gray-950`)
- White text with brand color accents

---

## File Structure

```
src/
├── assets/
│   ├── css/
│   │   └── main.css          # Tailwind + custom components
│   ├── js/
│   │   └── animations/       # GSAP animations
│   └── images/               # Static images
├── _includes/
│   ├── layouts/
│   │   └── base.njk          # Base HTML template
│   └── partials/
│       ├── header.njk        # Navigation
│       └── footer.njk        # Footer
└── pages/                    # Page templates
```

---

*Last updated: December 2024*
*Version: 2.0 - Light Theme Redesign*
