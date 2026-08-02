---
name: Style guide generator
slug: style-guide-generator
description: Turn a website, screenshots, or existing brand materials into a clear, organized design style guide document that your design and development team can use as the single source of truth.
---

# Style guide generator

Produce a comprehensive style guide / design system document from
whatever inputs are provided: a website URL, screenshots or images, or
existing brand documentation. Fill gaps with clarifying questions or clearly
marked placeholders rather than inventing brand facts.

## Gathering information

- If given a URL, fetch and analyze the page for design elements.
- If given screenshots or images, analyze them visually for the same elements.
- If given existing documentation, extract and reorganize it into the structure below.
- If information is missing, ask clarifying questions (mission statement, brand colors, accessibility requirements) rather than guessing at brand-specific facts.

Elements to extract: colors (primary, secondary, accent, text, background,
success/warning/error), typography (fonts, weights, sizes, line heights),
logo usage rules, icon style, imagery style, UI component patterns, layout
and spacing system, accessibility requirements.

## Standard structure

Organize the output into these sections:

**1.0 Introduction** — version number, date, purpose, audience.

**1.1 Mission & vision** — company mission/vision/positioning, if provided.

**1.2 Design principles** — 4-6 core principles guiding design decisions (e.g. "Clarity above all," "Consistency builds trust").

**2.0 Brand identity**
- *2.1 Logo usage* — primary logo, clear space, minimum size, incorrect-usage examples, color variations.
- *2.2 Color palette* — table of role / color name / HEX / RGB, covering primary, secondary, accent, text, background, and system colors (success/warning/error), with accessibility contrast notes.
- *2.3 Typography* — heading and body specs (family, weight, size, line height) in a table, plus fallback fonts.
- *2.4 Iconography* — style (outlined/filled/line weight), grid system, size variants.
- *2.5 Imagery* — photography/illustration style, treatment rules, do's and don'ts.

**3.0 Content style guide**
- *3.1 Voice and tone* — consistent voice attributes, and how tone shifts by context.
- *3.2 Grammar and mechanics* — punctuation, capitalization, active/passive preference, number and date formatting.

**4.0 UI components** — for each component (buttons, forms, cards, modals, navigation, tables, alerts, tooltips, badges, progress indicators): state variants, size variants, usage guidance, accessibility notes.

**5.0 Layout & grid** — grid system (columns, gutters), responsive breakpoints, spacing scale, container widths, margin/padding conventions.

**6.0 Accessibility** — WCAG compliance level (2.1 AA is the standard default), color contrast requirements, alt text guidelines, keyboard navigation, screen reader considerations, focus indicators.

**7.0 Resources** — links to design files, icon/illustration libraries, font files, code repository (use placeholders if unavailable).

**8.0 Changelog** — version history with dates and a summary of changes per version.

## Extraction by source type

**From a URL**: fetch the page and analyze color values, font families/sizes/weights, spacing patterns, component structures, visual hierarchy, button/form styling, and navigation patterns.

**From screenshots**: identify the color palette, typography hierarchy, spacing/layout patterns, and UI component variants visually.

**From existing documentation**: extract mission/vision, existing brand guidelines, color specs, typography standards, and any documented component library.

## Table formats to use

Color palette:
```
| Role | Color Name | HEX | RGB |
```

Typography:
```
| Element | Font Family | Weight | Size (px) | Line Height |
```

Button states:
```
| State | Appearance | Usage |
```

## Handling incomplete information

- Make reasonable inferences from what's provided (extract colors from screenshots, infer typography from a live site).
- Use clear placeholders for unknowns: "[Insert company mission statement]," "[Link to design files]," and default to "Version 1.0" with the current date.
- Ask clarifying questions when brand facts are genuinely unknown (mission statement, brand colors if none are visible, accessibility requirements beyond the WCAG default).

## Quality checklist before delivering

- [ ] Every section is either complete or clearly marked as a placeholder
- [ ] Color palette includes both HEX and RGB values
- [ ] Typography specs include family, weight, size, and line height
- [ ] Tables are properly formatted
- [ ] Accessibility requirements are documented
- [ ] Version number and date are included
- [ ] Resources section is present (even if placeholder links)
- [ ] Changelog starts at version 1.0
