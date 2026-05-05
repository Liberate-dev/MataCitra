# Design System Inspired by Cureganic

## 1. Visual Theme & Atmosphere

Cureganic's design system embodies a warm, approachable, and trustworthy aesthetic centered on natural wellness and community connection. The visual language combines organic, calming greens with deep navy tones, creating a sense of both professional credibility and accessible health advocacy. The system prioritizes clarity and openness, using generous whitespace and soft transitions to invite users into a conversation about alternative health solutions. Rounded corners and gentle shadows create a human-centered, non-clinical feel that contrasts with traditional medical aesthetics, positioning natural healing as empowering rather than fringe. The overall mood is optimistic, inclusive, and community-driven.

**Key Characteristics**

- Organic green palette with deep navy accents for trust and authority
- Warm, accessible color combinations that avoid clinical coldness
- Generous whitespace and breathing room throughout layouts
- Rounded, soft-cornered components with subtle elevation
- Typography-driven design with strong hierarchy and clear messaging
- Illustrative, inclusive imagery featuring diverse human figures
- Emphasis on community testimony and shared experiences

## 2. Color Palette & Roles

### Primary
- **Primary Brand Green** (`#28954E`): Main call-to-action buttons, primary interactive elements, and key brand moments; represents growth and natural healing
- **Deep Navy Blue** (`#0A2440`): Primary text, headings, and authoritative content; conveys trust and expertise in health information
- **Dark Slate** (`#425466`): Secondary text, supporting information, and UI elements; provides visual hierarchy without harshness

### Accent Colors
- **Soft Sage Green** (`#9ABB9B`): Lighter accent for hover states, secondary buttons, and supporting UI elements
- **Muted Teal-Green** (`#E5F3EB`): Light backgrounds for featured content sections and card highlights
- **Powder Blue** (`#0166FF`): Link highlights and interactive feedback elements

### Interactive
- **Pressed Navy** (`#3C485A`): Hover and active states for navigation and buttons; darker than default for visual feedback
- **Cool Gray** (`#6C7A90`): Disabled states and secondary interactive elements
- **Neutral Gray** (`#888990`): Tertiary interactive elements and subtle dividers

### Neutral Scale
- **Pure White** (`#FFFFFF`): Primary background, card surfaces, and content containers
- **Off-White** (`#F8F7F3`): Subtle background variation for visual separation
- **Light Neutral** (`#F6F9FC`): Secondary background layers and low-contrast surfaces
- **Pure Black** (`#000000`): Primary text and strong UI elements
- **Dark Gray** (`#2A2A2A`): Secondary and tertiary text
- **Light Gray** (`#CCCCCC`): Borders and subtle dividers

### Surface & Borders
- **Default Border** (`#CCCCCC`): Light borders on inputs and cards
- **Shadow Overlay** (`#2A2A2A` at 10% opacity): Subtle depth for dropdowns and elevation

### Semantic / Status
- **Error Red** (`#DC3232`): Error states, validation failures, and critical alerts
- **Danger Red** (`#E9463A`): Secondary error indication and destructive actions

## 3. Typography Rules

### Font Family

**Primary: Avenir**
- Font stack: `Avenir, 'Avenir Next', 'Helvetica Neue', sans-serif`
- Used for headings, display text, and strong visual hierarchy
- Weights: 900 (Black), 700 (Bold), 400 (Book)

**Secondary: Sen**
- Font stack: `Sen, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`
- Used for body text, labels, links, and UI content
- Weights: 700 (Bold), 400 (Regular)

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Display / H1 | Avenir | 68px | 900 | 71px | 0px | Hero headlines, page titles |
| Heading / H2 | Avenir | 60px | 900 | 64px | 0px | Section headings, major content blocks |
| Subheading / H4 | Avenir | 32px | 900 | 71px | 0px | Subsection titles, card headlines |
| Body / Paragraph | Sen | 22px | 400 | 32px | 0px | Main content text, descriptions |
| Label / Subtitle | Sen | 24px | 400 | 48px | 0px | Form labels, metadata, supporting text |
| Link | Sen | 16px | 400 | 24px | 0px | Inline links, navigation text |
| Button / CTA | Sen | 24px | 700 | 34px | 0px | Action text in buttons and CTAs |
| Caption | Avenir | 14px | 400 | 20px | 0px | Small supporting text, footnotes |
| Code / Monospace | `'Courier New', monospace` | 14px | 400 | 20px | 0px | Code blocks, technical content |

### Principles

- **Contrast-driven hierarchy**: Use Avenir for visual dominance (headings) and Sen for readability (body)
- **Generous line height**: Minimum 1.4x font size ensures comfortable reading and accessible spacing
- **Weight emphasis over size**: Rely on font weight changes (400 to 700 to 900) to create visual hierarchy without excessive size jumps
- **Semantic sizing**: Display text (68px+) reserved for page-level content; body text (22px) ensures legibility on all devices
- **Label clarity**: Slightly larger label text (24px) distinguishes form inputs and metadata from body content

## 4. Component Stylings

### Buttons

**Primary Button (Sign Up / Main CTA)**
- `background-color: #28954E`
- `color: #FFFFFF`
- `font-family: Sen, sans-serif`
- `font-size: 24px`
- `font-weight: 700`
- `padding: 16px 24px`
- `border-radius: 10px`
- `border: none`
- `height: 68px`
- `width: auto` (min 224px)
- `line-height: 34px`
- `box-shadow: none`
- **Hover state**: `background-color: #1F7A3E`, cursor pointer
- **Active state**: `background-color: #165F31`
- **Disabled state**: `background-color: #6C7A90`, `color: #CCCCCC`

**Secondary Button (Invite / Tertiary CTA)**
- `background-color: #E9463A`
- `color: #FFFFFF`
- `font-family: Sen, sans-serif`
- `font-size: 24px`
- `font-weight: 700`
- `padding: 16px 24px`
- `border-radius: 10px`
- `border: none`
- `height: 68px`
- `width: auto` (min 224px)
- `line-height: 34px`
- `box-shadow: none`
- **Hover state**: `background-color: #D62F25`, cursor pointer
- **Active state**: `background-color: #C1291C`

**Ghost Button (Link-style)**
- `background-color: transparent`
- `color: #9ABB9B`
- `font-family: Sen, sans-serif`
- `font-size: 24px`
- `font-weight: 700`
- `padding: 0px`
- `border-radius: 0px`
- `border: none`
- `height: 58px`
- `line-height: 34px`
- `box-shadow: none`
- **Hover state**: `color: #28954E`, text-decoration underline
- **Active state**: `color: #0A2440`

**Icon Button**
- `background-color: rgba(154, 187, 155, 0.2)`
- `color: #9ABB9B`
- `border-radius: 10px`
- `border: none`
- `height: 50px`
- `width: 51px`
- `font-size: 26px`
- `line-height: 39px`
- **Hover state**: `background-color: rgba(154, 187, 155, 0.4)`, `color: #28954E`

### Cards & Containers

**Content Card**
- `background-color: #FFFFFF`
- `border: 1px solid #CCCCCC`
- `border-radius: 10px`
- `padding: 32px 24px`
- `box-shadow: rgba(42, 42, 42, 0.08) 0px 2px 8px`
- **Hover state**: `box-shadow: rgba(42, 42, 42, 0.12) 0px 4px 12px`

**Featured Section Card**
- `background-color: #E5F3EB`
- `border: 1px solid #9ABB9B`
- `border-radius: 10px`
- `padding: 32px 24px`
- `box-shadow: none`
- `color: #0A2440`

**Hero Container**
- `background-color: #F8F7F3`
- `padding: 60px 40px`
- `border-radius: 0px`
- `max-width: 1200px`
- `margin: 0 auto`

### Inputs & Forms

**Standard Text Input**
- `background-color: #FFFFFF`
- `color: #000000`
- `font-family: Sen, sans-serif`
- `font-size: 22px`
- `font-weight: 400`
- `padding: 0px 0px 0px 25px`
- `border-radius: 10px`
- `border: 1px solid transparent`
- `height: 68px`
- `width: 400px`
- `line-height: 32px`
- `box-shadow: none`
- **Focus state**: `border: 2px solid #28954E`, `outline: none`
- **Placeholder**: `color: #6C7A90`, `opacity: 0.8`

**Form Field Input (with shadow)**
- `background-color: #FFFFFF`
- `color: #6C7A90`
- `font-family: Avenir, sans-serif`
- `font-size: 18px`
- `font-weight: 300`
- `padding: 20px`
- `border-radius: 10px`
- `border: none`
- `height: 68px`
- `width: 370px`
- `line-height: 30px`
- `box-shadow: rgba(35, 32, 79, 0.02) 4px 3px 9px 1px`
- **Focus state**: `box-shadow: rgba(35, 32, 79, 0.08) 4px 3px 12px 2px`, `color: #0A2440`
- **Error state**: `border: 2px solid #DC3232`, `box-shadow: rgba(220, 50, 50, 0.1) 0px 0px 8px`

**Label**
- `color: #0A2440`
- `font-family: Sen, sans-serif`
- `font-size: 24px`
- `font-weight: 400`
- `line-height: 48px`
- `padding: 0px 0px 12px 0px`
- `display: block`

### Navigation

**Navigation Link**
- `background-color: transparent`
- `color: #0A2440`
- `font-family: Sen, sans-serif`
- `font-size: 16px`
- `font-weight: 400`
- `padding: 8px 16px`
- `border-radius: 0px`
- `border: none`
- `line-height: 24px`
- `text-decoration: none`
- **Hover state**: `color: #28954E`, `border-bottom: 2px solid #28954E`
- **Active state**: `color: #28954E`, `border-bottom: 3px solid #28954E`

**Social Icon Link**
- `background-color: rgba(154, 187, 155, 0.15)`
- `color: #9ABB9B`
- `border-radius: 50%`
- `height: 50px`
- `width: 50px`
- `display: flex`
- `align-items: center`
- `justify-content: center`
- `font-size: 24px`
- `text-decoration: none`
- **Hover state**: `background-color: rgba(40, 149, 78, 0.2)`, `color: #28954E`

## 5. Layout Principles

### Spacing System

Base unit: `4px`

Spacing scale with contexts:
- `4px`: Tight spacing between inline elements
- `8px`: Minimal margin between related items
- `12px`: Small gaps within components
- `16px`: Standard padding for buttons and small containers
- `20px`: Medium padding for form inputs and card interiors
- `24px`: Common padding for components and sections
- `32px`: Large spacing between content blocks
- `36px`: Section separation
- `40px`: Container padding and major layout margins
- `52px`: Large component padding
- `56px`: Spacing between major sections
- `60px`: Hero section and large container padding

**Usage Context:**
- Form inputs and buttons: `16px`–`24px` padding
- Card interiors: `24px`–`32px` padding
- Section margins: `32px`–`60px`
- Text line spacing: `32px` (via line-height)

### Grid & Container

- **Max container width**: `1200px`
- **Column strategy**: 12-column responsive grid
- **Section patterns**: Full-width backgrounds with centered max-width containers
- **Gutter width**: `24px` between columns
- **Edge margins**: `40px` on desktop (scales down on mobile)
- **Hero sections**: Full-width with `60px` vertical padding

### Whitespace Philosophy

Cureganic emphasizes generous whitespace to communicate openness, calm, and accessibility. The design avoids visual clutter by spacing components far apart (32px–60px margins between sections) and using soft background colors rather than borders. This breathing room signals that health information is clear and non-urgent, inviting thoughtful engagement rather than rushed decisions. Whitespace separates related content blocks and gives users mental space to absorb messaging.

### Border Radius Scale

- `0px`: Full-width hero sections, page backgrounds
- `6px`: Modal and overlay borders
- `9px`: Image and media element corners
- `10px`: Input fields, buttons, cards, and standard UI components

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat | No shadow, `box-shadow: none` | Ghost buttons, links, text elements |
| Subtle | `rgba(42, 42, 42, 0.08) 0px 2px 8px` | Standard cards and containers |
| Medium | `rgba(42, 42, 42, 0.12) 0px 4px 12px` | Hovered cards, elevated sections |
| Enhanced | `rgba(35, 32, 79, 0.02) 4px 3px 9px 1px` | Form inputs with built-in depth |
| Focus | `rgba(35, 32, 79, 0.08) 4px 3px 12px 2px` | Focused input fields |
| Dropdown | `rgba(42, 42, 42, 0.1) 0px 0px 20px 10px` | Dropdown menus and floating panels |

**Shadow Philosophy**

Cureganic uses subtle, soft shadows to create layering without visual drama. Shadows are applied sparingly and typically at smaller scales (2–4px blur radius) to maintain the calm, approachable aesthetic. The drop shadow palette uses very low opacity (2–12%) of dark colors rather than pure black, preventing harsh visual hierarchy. Elevation increases only for interactive moments (hover states) or functional layers (inputs with depth). This restrained approach keeps the focus on content and messaging rather than visual effects.

## 7. Do's and Don'ts

### Do

- **Use Avenir for headings** to create visual dominance and draw attention to key messages
- **Leverage the green primary color** for all primary CTAs to create consistent action signaling
- **Maintain 32px minimum line height** for body text to ensure readability and accessibility
- **Apply 24px–32px padding** to cards and containers for breathing room
- **Use the full `#E5F3EB` background** for featured or call-out sections to signal importance gently
- **Employ soft box shadows** (8px blur, 2–8% opacity) for subtle depth on hover states
- **Center content in max-width 1200px containers** with 40px edge margins on desktop
- **Use the navy-to-slate color progression** (#0A2440 → #425466) for text hierarchy
- **Round corners at 10px** for input fields, buttons, and cards for consistency
- **Test links and interactive elements** with the secondary color (#9ABB9B) for light backgrounds

### Don't

- **Avoid pure black (#000000) text on dark navy backgrounds** — use mid-tone grays (#425466) instead
- **Don't use the error red (#DC3232) for non-critical messages** — reserve it for validation failures and warnings
- **Avoid applying shadows larger than 12px blur** — keep them subtle to maintain the calm aesthetic
- **Don't shrink text below 16px** for body content; maintain minimum 22px for main paragraphs
- **Avoid nesting more than two levels of cards** — simplify visual hierarchy to prevent confusion
- **Don't use more than three different shades of gray** in a single view
- **Avoid corner radius below 6px** — this design uses 0px or 9px–10px for consistency
- **Don't fill wide sections with solid accent colors** — use the light background variants (#E5F3EB) instead
- **Avoid animating shadows** — instead, change color or opacity on state changes
- **Don't use the secondary red (#E9463A) for neutral buttons** — reserve it for secondary CTAs and invitations only

## 8. Responsive Behavior

### Breakpoints

| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | 320px–479px | Single column, 16px edge margins, 48px section spacing, 14px–18px body text |
| Tablet | 480px–767px | 1–2 columns, 24px edge margins, 40px section spacing, 18px–20px body text |
| Desktop | 768px–1199px | 2–3 columns, 32px edge margins, 48px section spacing, 22px body text |
| Large Desktop | 1200px+ | 3+ columns, 40px edge margins, 60px section spacing, 22px body text, max-width 1200px containers |

### Touch Targets

- **Minimum touch target size**: `44px × 44px` (7mm × 7mm per WCAG 2.1 Level AAA)
- **Button height**: `68px` on mobile, `58px–68px` on desktop
- **Link padding**: `8px 16px` minimum for keyboard and touch navigation
- **Icon buttons**: `50px × 50px` minimum
- **Form inputs**: `68px` height to accommodate touch interaction comfortably

### Collapsing Strategy

- **Navigation**: Stack vertically in hamburger menu below 768px; horizontal layout on desktop
- **Grid layouts**: Switch from 3 columns (desktop) → 2 columns (tablet) → 1 column (mobile)
- **Hero sections**: Reduce padding from `60px` (desktop) → `36px` (tablet) → `24px` (mobile)
- **Typography**: Scale headings down 10–15% on mobile; maintain body text at minimum 16px
- **Button width**: Change from fixed 224px to `100%` on mobile with 16px margins
- **Containers**: Adjust from 1200px max-width to 100% with edge padding on mobile
- **Card layouts**: Stack cards vertically on mobile; maintain grid on tablet and above
- **Form fields**: Full width on mobile (100% – 32px margin); auto width on desktop (370px)

## 9. Agent Prompt Guide

### Quick Color Reference

- **Primary CTA**: Primary Brand Green (`#28954E`)
- **Secondary CTA**: Error Red (`#E9463A`)
- **Background**: Pure White (`#FFFFFF`)
- **Subtle Background**: Off-White (`#F8F7F3`)
- **Featured Background**: Soft Sage (`#E5F3EB`)
- **Heading Text**: Deep Navy Blue (`#0A2440`)
- **Body Text**: Pure Black (`#000000`) or Dark Slate (`#425466`)
- **Supporting Text**: Cool Gray (`#6C7A90`)
- **Borders**: Light Gray (`#CCCCCC`)
- **Hover/Active States**: Pressed Navy (`#3C485A`)
- **Disabled States**: Cool Gray (`#6C7A90`)
- **Error States**: Error Red (`#DC3232`)
- **Accent Highlights**: Muted Teal (`#9ABB9B`)
- **Icon Buttons**: Soft Sage Green (`#9ABB9B`)

### Iteration Guide

1. **Use Avenir Black (900px weight) for all H1, H2, H4 headings** to establish visual hierarchy and authority; pair with 32px–68px sizing
2. **Apply 24px line-height minimum and Sen font for body text** to ensure readability; maintain 22px font size for standard paragraphs
3. **Set primary button `background-color` to `#28954E` with 24px padding** and `10px border-radius`; include `:hover` state at `#1F7A3E`
4. **Wrap all input fields in containers with `10px border-radius` and white backgrounds**; add subtle shadow `rgba(35, 32, 79, 0.02) 4px 3px 9px 1px`
5. **Create cards with `24px–32px padding`, `1px #CCCCCC borders`, and `10px border-radius`**; apply soft shadows only on hover
6. **Use 40px–60px margins between major sections**; add `32px padding` to card interiors
7. **Apply `#0A2440` (Deep Navy) to all primary heading text** and `#425466` (Dark Slate) to secondary text for consistent hierarchy
8. **Include focus states on all interactive elements**: inputs show `2px #28954E border`, buttons show `#1F7A3E` background
9. **Center max-width containers at 1200px with 40px horizontal margins on desktop**; collapse to 100% width with 16px margins on mobile
10. **Responsive typography scale**: H1 drops from 68px (desktop) → 48px (tablet) → 32px (mobile); maintain body text 22px (desktop) → 18px (tablet) → 16px (mobile)
11. **Always test link colors on light backgrounds**: use `#0A2440` for dark links, `#9ABB9B` for light backgrounds; change to `#28954E` on hover
12. **Leverage the secondary red (`#E9463A`) for invite/secondary buttons only**; reserve `#DC3232` for error states and validation messages