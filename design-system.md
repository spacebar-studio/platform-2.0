# Mosey Platform 2.0 — Design System

A comprehensive design system for the Mosey Platform 2.0 compliance dashboard. This document defines every visual token, component, animation, pattern, and guideline used across the interface.

---

## Table of Contents

**Foundations**
1. [Design Principles](#1-design-principles)
2. [Color Palette](#2-color-palette)
3. [Typography](#3-typography)
4. [Spacing Scale](#4-spacing-scale)
5. [Borders & Radius](#5-borders--radius)
6. [Shadows & Elevation](#6-shadows--elevation)
7. [Iconography](#7-iconography)

**Components**
8. [Component Library](#8-component-library)

**Motion**
9. [Motion & Animation](#9-motion--animation)

**Patterns**
10. [Layout System](#10-layout-system)
11. [Navigation](#11-navigation)
12. [Data Hierarchy](#12-data-hierarchy)
13. [Feedback & States](#13-feedback--states)

**Guidelines**
14. [Usage Rules](#14-usage-rules)
15. [Accessibility](#15-accessibility)

---

## 1. Design Principles

### Core Principles

| Principle | Description |
|---|---|
| **Command Center Over Task List** | The home surface is an active operational hub, not a passive to-do list. Users see everything — tasks, locations, automations, legislation — in a single adaptive surface. |
| **Context Always Visible** | Location setup status, active automations, new legislation, and employee resources are always one glance away in the persistent contextual sidebar. |
| **Filter to Focus** | Users cut through complexity by status, category, assignment, and state — every filter combination produces a meaningful, actionable view. |
| **Every Item Is a Doorway** | Every task, location, legislation item, and resource link navigates into its full product experience. The dashboard is a launchpad, not a destination. |
| **Adaptive to Role and Moment** | The dashboard serves the morning triage, the urgent escalation, and the weekly review equally well. Information density adapts to the operating mode. |

### Visual Design Philosophy

- **Light & Warm**: Warm cream backgrounds and white cards create a clean, approachable feel. Professional without being cold or clinical.
- **Clean Typography**: Outfit for all UI text provides excellent legibility at dashboard densities. JetBrains Mono for data creates scannable numeric columns.
- **Semantic Color**: Status colors are consistent and meaningful — teal for active, green for complete, amber for warning, red for overdue. Every color earns its use.

### Information Hierarchy

| Level | Role | Component | Spec |
|---|---|---|---|
| **L1: KPI Summary** | 2-second status scan | KPI cards in flex row | 22px / 600wt |
| **L2: Activity Feed** | Chronological context | Color-bordered cards | 13px / cards |
| **L3: Task List** | Filterable task detail | Task rows with metadata | 13px / rows |
| **L4: Sidebar Context** | Ambient awareness | Persistent modules | Panel / links |

---

## 2. Color Palette

### Backgrounds & Surfaces

| Token | Hex | Usage |
|---|---|---|
| `bg` | `#F8F8F6` | Page background |
| `wh` | `#FFFFFF` | Card backgrounds, surfaces |
| `s1` | `#F3F3F0` | Subtle shade, table headers |
| `s2` | `#EAEAE6` | Medium shade, bar backgrounds |
| `s3` | `#DDDDD8` | Strong shade, darker fills |

### Text Hierarchy

| Token | Hex | Usage |
|---|---|---|
| `t1` | `#1A1D1F` | Primary text — headings, labels, values |
| `t2` | `#6B6E70` | Secondary text — descriptions, body copy |
| `t3` | `#9B9EA0` | Tertiary text — timestamps, captions |

### Semantic Status Colors

Each semantic color has three variants: **Foreground** (the color itself), **Background** (6-8% opacity), and **Border** (18-20% opacity).

#### Teal (Active / In Progress)

| Variant | Value | Usage |
|---|---|---|
| Foreground | `#36B5A0` | Active states, "All" filter pill, in-progress indicators |
| Background | `rgba(54,181,160,.06)` | Active button backgrounds, chip fills |
| Border | `rgba(54,181,160,.18)` | Focus rings, accent borders |

#### Green (Success / Completed)

| Variant | Value | Usage |
|---|---|---|
| Foreground | `#4CAF7D` | Completed status, success indicators |
| Background | `rgba(76,175,125,.08)` | Success fill |
| Border | `rgba(76,175,125,.20)` | Success border |

#### Amber (Warning / Action Required)

| Variant | Value | Usage |
|---|---|---|
| Foreground | `#E6A34D` | Warning status, action required indicators |
| Background | `rgba(230,163,77,.08)` | Warning fill |
| Border | `rgba(230,163,77,.20)` | Warning border |

#### Red (Error / Overdue)

| Variant | Value | Usage |
|---|---|---|
| Foreground | `#C05050` | Error status, overdue indicators |
| Background | `rgba(192,80,80,.08)` | Error fill |
| Border | `rgba(192,80,80,.20)` | Error border |

#### Blue (New / Info)

| Variant | Value | Usage |
|---|---|---|
| Foreground | `#5B8BD4` | New items, informational indicators |
| Background | `rgba(91,139,212,.08)` | Info fill |
| Border | `rgba(91,139,212,.20)` | Info border |

#### Purple (Processing)

| Variant | Value | Usage |
|---|---|---|
| Foreground | `#7B6CC4` | Processing status |
| Background | `rgba(123,108,196,.08)` | Processing fill |
| Border | `rgba(123,108,196,.20)` | Processing border |

#### Rose (CTA / Brand)

| Variant | Value | Usage |
|---|---|---|
| Foreground | `#D4697A` | Primary CTA buttons, brand accent |
| Background | `rgba(212,105,122,.06)` | CTA hover states |
| Border | `rgba(212,105,122,.18)` | CTA borders |

### Border

| Token | Value | Usage |
|---|---|---|
| `bd` | `#E5E5E0` | Default border on cards, tables, dividers |
| `bL` | `#F0F0EC` | Light border variant |

### Color Usage Rules

- **Status Mapping**: Teal = Active/In Progress, Green = Completed, Amber = Warning/Action Required, Red = Overdue/Error, Blue = New, Purple = Processing.
- **Contrast**: Primary text (#1A1D1F) on white maintains WCAG AAA at 15.4:1. Use t2 for secondary, t3 only for captions.
- **Backgrounds**: Never use semantic foreground colors as backgrounds directly. Use the B (background) variant at 6-8% opacity.
- **Left Borders**: Activity cards use 3px left borders in status colors to create scannable visual lanes.

---

## 3. Typography

### Typefaces

| Font | Family | Usage |
|---|---|---|
| **Outfit** | `'Outfit', system-ui, sans-serif` | All UI text — headers, labels, body, buttons, navigation |
| **JetBrains Mono** | `'JetBrains Mono', monospace` | Dates, timestamps, IDs, counts, numeric data |

Outfit is loaded from Google Fonts with weights 300 (Light), 400 (Regular), 500 (Medium), 600 (Semibold), 700 (Bold). JetBrains Mono is loaded with weights 400 and 500.

### Type Scale

| Size | Weight | Usage |
|---|---|---|
| 28px | 600 | Page headers (letterSpacing: -0.5px) |
| 22px | 600 | KPI values, section titles (letterSpacing: -0.3px) |
| 20px | 600 | Screen/detail headers |
| 18px | 600 | Subsection headers |
| 16px | 600 | Body large, prominent labels |
| 14px | 500 | Task titles, card headers |
| 13px | 400 | Body default — descriptions, body copy |
| 12px | 400 | Captions, secondary labels, timestamps |
| 11px | 500 | Buttons, filter chips, small text |
| 10px | 600 | Badges, KPI labels, uppercase metadata |
| 9px | 400 | Chart labels, axis text (minimum) |

### Font Weights

| Weight | Name | Usage |
|---|---|---|
| 300 | Light | Hero text, decorative display |
| 400 | Regular | Body text, descriptions, inactive labels |
| 500 | Medium | Buttons, default labels, task titles |
| 600 | Semibold | Headers, KPI values, active labels, section titles |
| 700 | Bold | Page titles, emphasis, large metrics |

### Additional Properties

- **Letter spacing**: `-0.5px` on page headers, `-0.3px` on section titles, `0.06em` on uppercase labels, `0.3px` on badges.
- **Line heights**: `1` for KPI values, `1.3` for headers, `1.5` for body text, `1.6` for paragraphs.
- **Text transform**: `uppercase` on badges, KPI labels, section category headers.

---

## 4. Spacing Scale

### Gap Scale

| Value | Category | Usage |
|---|---|---|
| 4px | Tight | Badge gaps, icon spacing |
| 6px | Tight | Small element gaps, pill spacing |
| 8px | Default | Card internals, badge groups |
| 10px | Default | KPI grid, element gaps |
| 12px | Comfortable | Card grids, section gaps |
| 16px | Comfortable | Section padding, sidebar items |
| 20px | Spacious | Page content padding |
| 24px | Spacious | Section breaks |
| 32px | Generous | Section dividers |
| 48px | Generous | Page side padding |

### Padding Patterns

| Padding | Component |
|---|---|
| `2px 8px` | Badge |
| `3px 10px` | Small button |
| `5px 14px` | Tab/pill button |
| `6px 14px` | State filter pill |
| `7px 16px` | Button default |
| `10px 14px` | KPI card |
| `14px 16px` | Card default |
| `16px 20px` | Section content |
| `28px 48px` | Page content |
| `36px 40px` | Modal dialog |

---

## 5. Borders & Radius

### Border Radius Scale

| Radius | Usage |
|---|---|
| 2px | Scrollbar thumb, progress bars |
| 4px | Badges, small elements |
| 6px | Code blocks, filter chips |
| 8px | Buttons, KPI cards, small cards |
| 10px | Cards, activity cards, containers |
| 16px | Modals, large containers |
| 20px | Pill tab containers |
| 9999px | Full pill buttons, state filter pills |
| 50% | Circular avatars, status dots |

### Border Styles

| Style | Value | Usage |
|---|---|---|
| Default | `1px solid #E5E5E0` | Card borders, dividers, separators |
| Accent | `1px solid rgba(54,181,160,.18)` | Active cards, focus states |
| Status left | `3px solid {status-color}` | Activity card left borders |
| Active nav | `2px solid #36B5A0` | Active sidebar indicator |

---

## 6. Shadows & Elevation

| Level | Shadow | Usage |
|---|---|---|
| 0 — Flat | `none` | Default cards, inline elements |
| 1 — Raised | `0 2px 8px rgba(45,31,26,.06)` | Hover states, card interactions |
| 2 — Elevated | `0 8px 24px rgba(45,31,26,.10)` | Dropdowns, popovers |
| 3 — Overlay | `0 20px 60px rgba(45,31,26,.15)` | Modals, full overlays |

### Shadow Rules

- **Depth via Color**: Platform 2.0 communicates depth through surface color (bg → s1 → s2 → s3), not shadow.
- **Shadows for Hover**: Box-shadows appear on card hover states to provide interactive feedback.
- **No Default Shadows**: Cards never have box-shadows in their default state.

---

## 7. Iconography

Platform 2.0 uses a combination of emoji-based icons and simple unicode symbols.

### Navigation Icons

| Icon | Section | Description |
|---|---|---|
| ⊞ | Home Dashboard | Primary landing, task feed |
| ◎ | Locations | State management, setup |
| ◈ | Calendar | Timeline views |
| ⟁ | Tasks | Task management |
| ◧ | Mail / Mailroom | Communications |
| ⬡ | Team | People, assignments |
| ◉ | Search | Global search |
| ⚙ | Settings | Configuration |

### Status Indicators

| State | Color | Visual |
|---|---|---|
| New | Blue (#5B8BD4) | Filled circle |
| In Progress | Teal (#36B5A0) | Filled circle |
| Action Required | Amber (#E6A34D) | Warning triangle |
| Completed | Green (#4CAF7D) | Checkmark |
| Overdue | Red (#C05050) | Filled circle |
| Processing | Purple (#7B6CC4) | Filled circle |

---

## 8. Component Library

### State Filter Pills

Horizontal pill-based state selector that scopes the entire dashboard view.

**Spec:** `padding: 6px 14px`, `border-radius: 20px (9999 for pill)`, `font-size: 12px`, `font-family: Outfit`.

**States:**

| State | Background | Border | Color |
|---|---|---|---|
| Active (All) | `#36B5A0` | none | `#fff` |
| Active (State) | `#36B5A0` | none | `#fff`, with state icon |
| Inactive | `#fff` | `1px solid bd` | `t2` |
| Hover | `s1` | `1px solid bd` | `t2` |
| Overflow | `#fff` | `1px solid bd` | `t2`, "39 more ▾" |

---

### KPI Card

Key Performance Indicator for status summary row.

**Spec:** `padding: 14px 16px`, `border-radius: 10px`, `border: 1px solid bd`, `background: #fff`.

**Internal structure:**

| Element | Size | Weight | Color | Additional |
|---|---|---|---|---|
| Status icon | 32x32px | — | Status color at 8% bg | Border-radius: 8px |
| Value | 22px | 600 | `t1` | Line-height: 1 |
| Label | 12px | 400 | `t2` | Below value |

**Variants:** New (blue icon), In Progress (teal), Action Required (amber), Completed (green).

---

### Activity Card

Chronological feed card with status-colored left border.

**Spec:** `padding: 14px 16px`, `border-radius: 0 10px 10px 0`, `border: 1px solid bd`, `border-left: 3px solid {status-color}`.

**Status-to-border mapping:**

| Status | Border Color | Icon |
|---|---|---|
| Warning / Action Required | Amber (#E6A34D) | ⚠ |
| Success / Complete | Green (#4CAF7D) | ✓ |
| New / Info | Blue (#5B8BD4) | 📄 |
| Processing | Purple (#7B6CC4) | ⏳ |

**Internal structure:**
1. Header row: Status icon + Title (14px/500) + Category badge + Timestamp + Expand chevron
2. Expanded detail: Description (12px/t2) + Tag pill + Date (JetBrains Mono)

**Hover:** `box-shadow: 0 2px 8px rgba(45,31,26,.06)`.

---

### Task Row

Filterable task row with rich metadata.

**Spec:** `padding: 12px 14px`, `border-radius: 10px`, `border: 1px solid bd`, `background: #fff`.

**Internal structure:**
1. Status dot: 12px circle with 2px border in status color
2. Title: 13px / 500 / t1
3. Description: 12px / t3, single-line with ellipsis overflow
4. Due date: 11px, colored by urgency (red=overdue, amber=soon, t3=normal)
5. State label: 11px / t3
6. Assignee badge: 10px, teal background at 6%, pill shape

**Hover:** `background: s1`, `border-color: tealD`.

---

### Button

Primary and secondary action buttons with size and shape variants.

**Variants:**

| Variant | Background | Border | Text Color | Font Weight |
|---|---|---|---|---|
| Primary (Teal) | `#36B5A0` | none | `#fff` | 600 |
| Primary (Rose) | `#D4697A` | none | `#fff` | 600 |
| Secondary | `#fff` | `1px solid bd` | `t1` | 500 |
| Active | `tealB` | `1px solid tealD` | `teal` | 600 |

**Sizes:**

| Size | Padding | Font Size | Border Radius |
|---|---|---|---|
| Default | `7px 16px` | 13px | 8px |
| Small (sm) | `3px 10px` | 11px | 8px |
| Pill | `7px 16px` | 13px | 9999px |

**States:** Default, Hover (lighten bg), Active, Loading (opacity 0.6 + spinner), Disabled (opacity 0.4).

**Special:** Start button uses rose background with white count badge: `background: rgba(255,255,255,.3), padding: 1px 6px, border-radius: 4px`.

---

### Badge

Status and category indicator labels.

**Status badges:** `font-size: 10px`, `font-weight: 600`, `padding: 2px 8px`, `border-radius: 4px`, `text-transform: uppercase`, `letter-spacing: 0.3px`. Background uses status color at 8% opacity.

| Type | Color | Usage |
|---|---|---|
| success | `#4CAF7D` | Completed, healthy |
| active | `#36B5A0` | In progress, selected |
| warning | `#E6A34D` | Action required, attention |
| critical | `#C05050` | Overdue, failures |
| info | `#5B8BD4` | New, informational |
| processing | `#7B6CC4` | Processing states |
| neutral | `#9B9EA0` | Inactive, archived |

**Category badges:** `font-size: 10px`, `font-weight: 500`, `padding: 3px 10px`, `background: s1`, `border-radius: 4px`, `color: t2`. Includes category icon. Types: HR, Entity, Tax, Payroll, Legal, Insurance.

---

### Card

Primary container component.

**Base spec:** `background: #fff`, `border: 1px solid bd`, `border-radius: 10px`, `padding: 14px 16px`.

**Variants:**

| Variant | Properties |
|---|---|
| Default | White background, standard border |
| Glass | `background: rgba(255,255,255,.72)`, `backdrop-filter: blur(14px)` |
| Accent border | Custom `bc` prop with teal/status color |
| Status left-border | `border-left: 3px solid {color}` for activity cards |
| Header card | `padding: 0`, `overflow: hidden`, header div with bottom border |
| Animated | `className: "fu"` for fade-up entrance |

---

### Filter Toolbar

Multi-dimensional filter system for task feed.

**Structure:**
1. Filter dropdown button (secondary Btn)
2. Active filter chips: `padding: 3px 8px`, `background: tealB`, `border: 1px solid tealD`, `border-radius: 6px`, with dismiss ✕
3. Bulk edit toggle: 36x20px track, 16px thumb, `border-radius: 10px`
4. Start button: Rose primary Btn with count badge

---

### Sidebar Module

Persistent contextual sidebar section.

**Module header:** `font-size: 10px`, `font-weight: 600`, `text-transform: uppercase`, `letter-spacing: .06em`, `color: t3`.

**Module items:** `padding: 10px 12px`, `background: #fff`, `border: 1px solid bd`, `border-radius: 8px`, `gap: 4px`. Contains icon, title (13px/500/t1), optional subtitle (11px/t3), and chevron (›).

**Module types:** Complete Setup, Automations in Progress, Legislation, Employee Resources.

---

### Policy Banner

Persistent top-of-feed prompt card.

**Spec:** `padding: 14px 18px`, `border-radius: 10px`, `border: 1px solid bd`, `background: #fff`.

**Structure:** 32px icon container (teal bg at 6%) + Title (14px/600) + Description (12px/t2) + Chevron (›).

**Hover:** `box-shadow: 0 2px 8px rgba(45,31,26,.06)`.

---

### Form Input

**Spec:** `padding: 8px 12px`, `border-radius: 8px`, `border: 1px solid bd`, `font-size: 13px`, `font-family: Outfit`.

**States:**

| State | Border | Additional |
|---|---|---|
| Default | `bd` | — |
| Focus | `teal` | `box-shadow: 0 0 0 3px tealD` |
| Disabled | `bd` | `background: s1`, `color: t3`, `cursor: not-allowed` |

**Toggle:** 40x22px track, 18px thumb, `border-radius: 11px`. On: `background: teal`. Off: `background: s2`. Transition: `left .2s cubic-bezier(.4,0,.2,1)`.

---

## 9. Motion & Animation

### Entrance Animations

| Name | Keyframes | Duration | Usage |
|---|---|---|---|
| `fu` (Fade Up) | `opacity: 0, translateY(12px)` → `opacity: 1, translateY(0)` | 0.45s ease-out | Cards, KPIs, page sections |
| `fi` (Fade In) | `opacity: 0` → `opacity: 1` | 0.3s ease-out | Expanded content, details |
| `fadeScale` | `opacity: 0, scale(.96)` → `opacity: 1, scale(1)` | 0.4s ease-out | Modals, popovers |

### Continuous Animations

| Name | Effect | Duration | Usage |
|---|---|---|---|
| `gl` (Glow) | `box-shadow` pulse (rose, 6px→16px) | 2s ease-in-out infinite | Active indicators, CTA emphasis |
| `meshGrad` | Background-position cycle through 4 waypoints | 14s ease infinite | Animated page backgrounds |

### Hover Transitions

| Element | Property | Duration | Easing |
|---|---|---|---|
| Buttons | `all` | 0.15s | ease |
| Cards | `all` | 0.2s | ease |
| Table/task rows | `background` | 0.12s | ease |
| Toggle thumb | `left` | 0.2s | cubic-bezier(.4,0,.2,1) |
| Progress bars | `width` | 0.6s | ease |
| Expand chevrons | `transform` | 0.2s | ease |

### Staggered Entry

Activity cards and list items use sequential `animationDelay` for cascading entrance:
- Default: `animationDelay: i * 0.08s` (80ms between items)

---

## 10. Layout System

### App Shell Structure

```
┌──────┬─────────────────────────┬──────────────┐
│      │                         │              │
│ Nav  │   Main Content          │   Sidebar    │
│ 56px │   (flex: 1)             │   (280-320px)│
│      │                         │              │
│ Icon │   State Filter Bar      │  Setup       │
│ only │   Policy Banner         │  Automations │
│      │   KPI Row               │  Legislation │
│      │   Activity Feed         │  Resources   │
│      │   Task List             │              │
└──────┴─────────────────────────┴──────────────┘
```

### Content Widths

| Element | Width |
|---|---|
| Side Navigation | 56px, fixed, icon-only |
| Main Content | `flex: 1`, fills remaining space |
| Contextual Sidebar | 280-320px, fixed, right-aligned |
| Case Study Pages | `max-width: 900px`, centered with `margin: 0 auto` |
| Design System Sidebar | 220px, fixed left panel |
| Design System Content | `flex: 1`, `padding: 24px 32px` |

### Grid Patterns

| Pattern | CSS | Usage |
|---|---|---|
| KPI Row | `display: flex, gap: 10px` | Each KPI `flex: 1, min-width: 0` |
| Activity Feed | Vertical stack, `gap: 8px` | Sequential activity cards |
| Sidebar Modules | Vertical stack, `gap: 16px` | Module sections with items |
| Overview Grid | `grid-template-columns: 1fr 1fr` | Two-column content layouts |

---

## 11. Navigation

### Vertical Sidebar

56px icon-only navigation bar. Active item shows rose accent color. 8 navigation sections.

| Property | Value |
|---|---|
| Width | 56px |
| Background | `#fff` |
| Border | Right 1px `bd` |
| Icon size | 20px |
| Active color | Rose (`#D4697A`) |
| Inactive color | `t3` |
| Hover | Background lighten |

### State Filter Bar

Horizontal pill-based selector below the header. Scopes both task feed and sidebar.

| Property | Value |
|---|---|
| Position | Below header, above content |
| Layout | Horizontal flex, gap: 6px |
| Active pill | Filled teal, white text, 600 weight |
| Inactive pill | White bg, bd border, t2 color |
| Overflow | "39 more ▾" dropdown trigger |

### Breadcrumb via Back

Detail panels use a Back button. One level deep only.

---

## 12. Data Hierarchy

Platform 2.0 follows a four-level progressive disclosure pattern:

```
KPI Summary  →  Activity Feed  →  Task Triage  →  Sidebar Context
   (Scan)         (Review)          (Act)           (Monitor)
```

| Level | Component | Purpose |
|---|---|---|
| L1 — KPI Summary | Status count cards | 2-second system health scan |
| L2 — Activity Feed | Color-bordered cards | Chronological context |
| L3 — Task List | Filterable rows | Focused triage and action |
| L4 — Sidebar | Persistent modules | Ambient awareness |

---

## 13. Feedback & States

### Loading States

| Pattern | Implementation | Usage |
|---|---|---|
| Spinner | 24px circle with border animation | Inline button loading |
| Skeleton | Pulsing background bars (s2, alternating opacity) | Content placeholders |
| Progress Bar | Animated width transition, 0.6s ease | Multi-step processes |
| Button Loading | Text change to "Loading..." + disabled state | Action feedback |

### Empty States

Centered layout with:
- Large faded icon (28px, 30% opacity)
- Title (13px, 600wt, t1)
- Description (11px, t3)
- Action button (Btn sm)
- Container: dashed border, centered text

### Alert Severity Mapping

| Severity | Badge Type | Left Border | Action |
|---|---|---|---|
| Overdue | critical | Red | Immediate attention |
| Action Required | warning | Amber | Review and respond |
| New | info | Blue | Acknowledge |
| Completed | success | Green | No action needed |
| Processing | processing | Purple | Monitor |

---

## 14. Usage Rules

### Color

**Do:**
- Use semantic colors consistently: teal=active, green=complete, amber=warning, red=overdue
- Use opacity variants at 6-8% for tinted backgrounds
- Pair every color-coded element with a text label

**Don't:**
- Use semantic foreground colors as background fills directly
- Mix severity meanings (amber for success, teal for errors)
- Introduce colors outside the defined palette

### Typography

**Do:**
- Use Outfit for all UI text
- Use JetBrains Mono for dates, IDs, timestamps, and numeric data
- Use the type scale consistently — don't invent new sizes

**Don't:**
- Go below 9px font size for any text
- Use font-weight 700 on body text — reserve bold for page titles
- Mix fonts within a single label

### Components

**Do:**
- Limit to one primary (teal/rose) button per visual group
- Use 3px left borders on activity cards for status color lanes
- Place 3-5 KPIs per row at the top of the dashboard

**Don't:**
- Nest cards more than one level deep
- Use badges for interactive elements — they're display-only
- Skip the anim prop on cards that appear on page load

### Motion

**Do:**
- Use fu (fade-up) for cards and sections entering the viewport
- Keep transition durations between 0.12s and 0.6s
- Use ease-out for entrances, ease for state changes

**Don't:**
- Apply continuous animations to more than 2 elements at once
- Animate elements that are already visible — entrances only
- Use animation delays longer than 0.5s for staggered lists

### Layout

**Do:**
- Use fixed widths for navigation (56px) and sidebar (280-320px)
- Let the main content area flex to fill remaining space
- Use gap for spacing between siblings, margin for section separation

**Don't:**
- Use percentage widths for fixed panels
- Set overflow:auto on the root shell — only inner panels scroll
- Create layouts wider than the viewport

---

## 15. Accessibility

### Color Contrast Ratios

| Foreground | Background | Ratio | Level |
|---|---|---|---|
| t1 (#1A1D1F) | White (#FFF) | 15.4:1 | AAA |
| t2 (#6B6E70) | White (#FFF) | 5.1:1 | AA |
| Teal (#36B5A0) | White (#FFF) | 3.2:1 | AA Large |
| Rose (#D4697A) | White (#FFF) | 3.8:1 | AA Large |
| Red (#C05050) | White (#FFF) | 4.6:1 | AA |
| t3 (#9B9EA0) | White (#FFF) | 2.8:1 | — (captions only) |

### Principles

1. **Color Is Not the Only Signal** — Every status uses text labels (badges), icons, or descriptive text alongside color.
2. **Minimum Target Sizing** — All interactive elements meet 32px minimum touch target.
3. **Keyboard Navigation** — Native HTML button elements with visible focus states.
4. **Font Size Minimums** — 9px minimum (chart labels only). 10px for badges. 13px for body text.
5. **Motion Sensitivity** — Animations use ease-out, stay under 0.45s for entrances. Infinite animations are subtle.

---

## Token Reference

```
// Colors
DS.bg   = "#F8F8F6"    DS.wh   = "#FFFFFF"    DS.s1   = "#F3F3F0"
DS.s2   = "#EAEAE6"    DS.s3   = "#DDDDD8"    DS.bd   = "#E5E5E0"
DS.t1   = "#1A1D1F"    DS.t2   = "#6B6E70"    DS.t3   = "#9B9EA0"
DS.teal = "#36B5A0"    DS.green= "#4CAF7D"    DS.amber= "#E6A34D"
DS.red  = "#C05050"    DS.blue = "#5B8BD4"    DS.purple="#7B6CC4"
DS.rose = "#D4697A"

// Fonts
FT = "'Outfit', system-ui, sans-serif"    // All UI text
MN = "'JetBrains Mono', monospace"        // Dates, IDs, numeric

// Animation Classes
.fu  = fade-up (0.45s)    .fi  = fade-in (0.3s)    .fs  = fadeScale (0.4s)
.gl  = glow (2s infinite)  meshGrad = background animation (14s infinite)
```

---

*Mosey Platform 2.0 Design System — April 2026*
