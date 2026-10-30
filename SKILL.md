---
name: ibk-design-system
description: Use when designing or building any page, section or component for the IBK Products website. Builds only from this design system (Clay base).
---

# IBK Products design system

The look: warm, friendly, generous, handmade (Clay base).
Source of truth: `assets/tokens.css` (values) and `assets/components.css` (components). The storybook (`storybook.html`) shows every token and component.
Home page design: `prototypes/home.html`.

## Hard rules
1. Use tokens only. Never write a colour, font, size, radius, shadow or duration directly in a page. If a value is missing, propose adding a token first.
2. Use existing components before inventing new ones. If a page needs something new, say so, propose it as a component, and add it to `components.css` and the storybook once agreed.
3. One `display` or `h1` per page. Sections use `h2`, items inside sections use `h3`.
4. One primary button per view. Button labels start with a verb.
5. One inverse section per page, used for the closing call to action.
6. Every page works on a phone at 390px wide, with no horizontal scroll and touch targets of at least 44px.
7. Text contrast at least 4.5:1. Errors are shown in words, not colour alone.
8. Motion is subtle: elements rise and fade in once with `data-reveal`. Respect reduced motion.
9. No fake testimonials, reviews or numbers. Placeholders stay visibly marked until replaced with real ones.
10. Design decisions are made in Claude chat and recorded in the design system or a prototype. When building (Claude Code), never decide design: if something isn't defined, stop and ask with two or three options.
11. A split hero (`hero--split`) has one `h1`, one lead, one primary button, and a panel with at most three row cards. Each row card names one benefit in a title and one sentence.
12. Never choose a payment, analytics or dashboard tool without asking first.

## Components (class names)
- Layout: `container`, `section`, `section--surface`, `section--inverse`, `section--tight`, `section-head`, `grid grid--2|grid--3`, `split`, `stack`
- Type: `display`, `h1`, `h2`, `h3`, `lead`, `body`, `small`, `eyebrow`, `measure`
- Actions: `btn btn--primary`, `btn btn--secondary`, `btn-row`, `link`
- Blocks: `nav`, `hero`, `hero--split` (with `hero__main`, `hero__panel`), `page-hero`, `card`, `card--row`, `card__icon`, `steps` / `step`, `price` / `price--featured`, `badge`, `list`, `quote`, `faq`, `cta`, `footer`
- Forms: `form`, `form__row`, `field`, `label`, `input`, `field__error`

## Page patterns
- Home: split hero (benefits in the panel), what we do (4 cards for the business types, `grid--2`), how it works (3 steps), proof (quote), closing CTA (inverse)
- Pricing: page hero, plans (3 price cards, one featured), FAQ, closing CTA
- About: page hero, beliefs (split), closing CTA
- Contact: page hero, form + what happens next (split)

## Before you deliver
- [ ] Only tokens and existing components used
- [ ] Phone, tablet and desktop checked; no horizontal scroll
- [ ] One h1, one primary button per view, one inverse section
- [ ] Contrast and form errors checked
- [ ] Placeholders replaced or clearly marked

## Keeping this skill current
When a decision changes the system (a new token, a new component, a new rule), update this file in the same change. Claude chat should suggest it: "This should go into the design skill."
