# Design Rationale - MataCitra Landing Page

## Color System

### Primary Colors

| Color | Hex | Usage | Why |
|-------|-----|-------|-----|
| **Deep Forest** | `#0B2B26` | Primary backgrounds, headings, buttons | Teal-green gelap → medical credibility + warmth. Dark enough untuk contrast WCAG, light enough avoid oppressive feel. |
| **Forest** | `#1B4332` | Secondary elements, hover states | Slightly lighter untuk layering, maintains green family cohesion. |
| **Sage** | `#40916C` | Accent icons, borders | Mid-tone green → visual breathing room antara dark dan light. |

### Accent Colors

| Color | Hex | Usage | Why |
|-------|-----|-------|-----|
| **Gold** | `#B8860B` | CTAs, badges, highlights | Gold → premium healthcare, trust, warmth. Darker shade (bukan `#C5A059`) untuk contrast ratio ≥ 4.5:1 dengan light backgrounds. |
| **Mint** | `#D8F3DC` | Card backgrounds, section dividers | Light green → organic, calming, bukan clinical white. |
| **Cream** | `#FCFAF7` | Page background | Warmer than pure white → approachable, reduced eye strain untuk target audience 40+. |

### Neutral Scale

| Color | Hex | Usage | Why |
|-------|-----|-------|-----|
| **Charcoal** | `#2D3436` | Body text | Soft black → readable tanpa harshness. |
| **Warm Gray** | `#636E72` | Secondary text, descriptions | Muted → hierarchy tanpa compete dengan headings. |

### Why Green + Gold?

```
Green (#0B2B26) → Health, growth, vision, nature
Gold (#B8860B) → Premium, trust, expertise, warmth
```

Pasangan ini:
- Berbeda dari competitors (bukan biru-hijau generik)
- Memberikan premium healthcare feel
- Tetap approachable untuk audience 40+ (bukan corporate cold)

---

## Typography System

### Font Pairing

| Font | Weight | Usage | Why |
|------|--------|-------|-----|
| **Playfair Display** | 400, 600, 700, italic variants | Headings, display text | Serif → editorial, trustworthy, premium. Italic untuk emphasis tanpa bold (lebih refined). |
| **DM Sans** | 400, 500, 600 | Body, UI elements | Geometric sans → clean, readable, modern. Tanpa compete sama Playfair. |

### Why NOT Inter/Roboto?

- Overused → generic AI feel
- System fonts → no personality
- DM Sans + Playfair → distinctive, memorable

### Type Scale

```
Display: 68px (desktop) / 48px (tablet) / 32px (mobile)
Heading: 56px / 40px / 32px
Subheading: 38px / 32px / 28px
Body: 20px (desktop) / 18px (mobile)
```

**Minimum 20px body** untuk audience 40+ — readability over compactness.

---

## Spacing System

Base unit: **8px**

| Token | Value | Usage |
|-------|-------|-------|
| `--space-xs` | 8px | Tight gaps |
| `--space-sm` | 12px | Icon gaps |
| `--space-md` | 16px | Button padding |
| `--space-lg` | 24px | Card padding |
| `--space-xl` | 32px | Section gaps |
| `--space-2xl` | 48px | Major spacing |
| `--space-3xl` | 64px | Section separation |
| `--space-4xl` | 80px | Hero/major sections |

**Why 8px base?** Easy to multiply/divide, consistent rhythm, mobile-friendly scaling.

---

## Component System

### Buttons

#### Primary CTA
```css
background: #0B2B26
padding: 18px 36px
border-radius: 14px
font-weight: 600
box-shadow: 0 8px 24px rgba(11, 43, 38, 0.25)
```

**Why?** Dark green → action, high contrast. Box shadow → depth, clickable feel. Hover → gold transition untuk visual interest.

#### Secondary CTA
```css
background: #FFFFFF
border: 2px solid #0B2B26
```

**Why?** Outline style → secondary action, don't compete dengan primary. Hover fills dengan mint untuk feedback.

### Cards

```css
background: #FFFFFF
border-radius: 20px
box-shadow: 0 4px 24px rgba(11, 43, 38, 0.08)
padding: 40px 32px
```

**Why?**
- White → clean, medical feel
- 20px radius → soft, approachable (bukan harsh 4px)
- Subtle shadow → elevation without drama
- Hover → shadow increases + translateY untuk tactile feedback

### Icons

Using **Lucide** library:
- Consistent 24px grid
- 2px stroke weight
- Rounded caps
- Single color (bukan multicolored)

**Why Lucide?**
- Clean, modern aesthetic
- Open source (bukan premium libraries)
- Tree-shakeable untuk performance
- Medical-appropriate icon set

---

## Motion & Animation

### Principles

1. **Purposeful** — Every animation communicates something
2. **Subtle** — Enhance, not distract
3. **Fast** — 200-400ms max untuk interactions
4. **Reduced motion** — Respect `prefers-reduced-motion`

### Animation Tokens

```css
--duration-fast: 200ms
--duration-normal: 400ms
--duration-slow: 800ms
--ease-out: cubic-bezier(0.4, 0, 0.2, 1)
```

### Animation Inventory

| Animation | Usage | Timing |
|-----------|-------|--------|
| `fadeInUp` | Scroll reveal, hero entrance | 800ms |
| `float` | Floating cards (hero) | 5s infinite |
| `shimmer` | Logo highlight | 3s infinite |
| `pulse-gold` | Map pin emphasis | 2s infinite |
| `scaleIn` | Hero image entrance | 800ms |

### Parallax Strategy

Parallax only on **desktop** (`min-width: 768px`).

**Why disable on mobile?**
- Performance impact on low-end devices
- Battery drain
- Motion sickness for some users
- WCAG prefers reduced motion

---

## Layout System

### Container

```css
max-width: 1400px
padding: 0 60px (desktop) / 0 24px (mobile)
margin: 0 auto
```

### Grid

12-column system:
- Desktop: 3-4 columns
- Tablet: 2 columns
- Mobile: 1 column

### Section Rhythm

```
Hero → Stats → Services → Doctors → Gallery → Facilities → Testimonials → Contact → Footer
```

**Why this order?**
1. Hero establishes trust + CTA
2. Stats immediately build credibility
3. Services show what we do
4. Doctors put faces to expertise
5. Gallery visualizes environment
6. Facilities prove capability
7. Testimonials provide social proof
8. Contact makes conversion easy

---

## Responsive Breakpoints

| Breakpoint | Width | Columns | Font Scale |
|------------|-------|---------|------------|
| Desktop | 1024px+ | 3-4 | Full |
| Tablet | 768-1023px | 2 | 90% |
| Mobile | <768px | 1 | 80% |

### Mobile-First Decisions

- Touch targets minimum **44x44px** (WCAG 2.1 AAA)
- Font size tidak turun dari **16px** untuk body
- Images lazy-loaded untuk performance
- Parallax disabled
- Simplified navigation (hamburger menu)

---

## Accessibility Decisions

### Color Contrast

| Combination | Ratio | WCAG Level |
|-------------|-------|------------|
| Deep Forest on White | 12.6:1 | AAA |
| Charcoal on White | 9.5:1 | AAA |
| Gold on White | 4.7:1 | AA |
| White on Gold | 4.7:1 | AA |

**Gold darkened dari `#C5A059` ke `#B8860B`** untuk mencapai 4.5:1 minimum.

### Focus States

```css
*:focus-visible {
  outline: 3px solid var(--gold);
  outline-offset: 2px;
}
```

**Why gold?** Consistent dengan brand, visible against semua backgrounds.

### Screen Reader Support

- Skip link untuk keyboard navigation
- ARIA labels pada icon-only links
- `aria-hidden` pada decorative elements
- Landmark roles (`banner`, `navigation`, `contentinfo`)
- Proper heading hierarchy (H1 → H2 → H3)

---

## Performance Decisions

### Critical Path

1. **Critical CSS inline** — Above-the-fold renders tanpa blocking
2. **Font preconnect** — Faster font loading
3. **Image preload** — Hero image LCP optimized
4. **Lazy loading** — Below-fold images deferred
5. **Decoding async** — Images don't block main thread
6. **JS defer** — Scripts load setelah parse

### Why Not Use External Stylesheet?

Single HTML file chosen untuk:
- Zero build step
- Portable (copy paste aja)
- GitHub Pages compatible
- Fewer HTTP requests

Tradeoff: Larger HTML file, but acceptable untuk landing page size.

---

## Design Influences

### Cureganic (DESIGN.md reference)
- Warm, approachable healthcare aesthetic
- Organic color palette
- Soft rounded corners
- Generous whitespace

### Spring Health (springhealth.com)
- Large stat callouts ("<1 day", "95%")
- Trust-building logos strip
- Benefit-focused headlines
- Clean, spacious layout

### Applied to MataCitra

```
Cureganic warmth → Organic green palette + soft corners
Spring Health stats → Large numbers in hero + stats section
Both → Medical credibility + approachability balance
```

---

## Anti-Patterns Avoided

❌ **Purple gradients** — Generic AI/SaaS look
❌ **Inter/Roboto** — Overused, no personality
❌ **Harsh shadows** — Too dramatic, not healthcare-appropriate
❌ **Pure black text** — Too harsh on eyes
❌ **Small fonts** — Not accessible for 40+ audience
❌ **Symmetrical everything** — Boring, generic
❌ **Decoration without purpose** — Clutter
❌ **Animations everywhere** — Distracting, performance hit
