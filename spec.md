# Spec: The Alternative Desktop Synthesizer Garden

## Overview

A single-page, self-contained HTML landing page for a project that creates desktop-native synthesizer instruments. The page uses a Mediterranean garden metaphor to present a collection of experimental musical instruments built for personal computers. The tone is casual, slightly self-deprecating, and conversational — mixing poetic garden imagery with offhand asides ("kind of nifty, at best", "Pizza rolls are often times present", "It is indeed go time, broski").

## Project Structure

```
thealternativedesktopsynthesizergarden/
  index.html          # Single-file application (HTML + CSS + JS)
  a_A_beautiful_garden_a.jpeg   # Hero image and CTA section image
  b_A_beautiful_garden_a.jpeg   # Philosophy section illustration and footer image
  flux-2-pro_a_A_beautiful_garden_a.jpeg   # CTA section image
  recraft-v4_b_A_beautiful_garden_a.png    # CTA section small image between buttons
  qwerty screenshot.png   # QWERTY Tempered instrument card screenshot
  windows screenshot.png  # Window Candy instrument card screenshot
  labyrinth screenshot.png # Labyrinth instrument card screenshot
  spec.md             # This file
  README.md           # Project readme
```

## Technical Stack

- **HTML5** - Single document, no external dependencies (except Google Fonts)
- **CSS** - Embedded styles with CSS custom properties, animations, gradients, and responsive breakpoints
- **JavaScript** - Vanilla JS for procedural element generation, IntersectionObserver animations, and Web Audio API synthesis
- **SVG** - Inline SVG for the vine divider in the Vision section
- **Images** - JPEG/PNG files for hero, illustrations, instrument screenshots, and CTA section
- **Fonts** - Cormorant Garamond and EB Garamond via Google Fonts

## Page Sections

### 1. Hero
- Full-viewport landing section (`min-height: 100vh`)
- Title structure:
  - "The Alternative Desktop" (small, uppercase, muted)
  - "Synthesizer" (main word)
  - "Garden" (italic, gold-light color)
- Subtitle: "We make synths that are kind of nifty, at best. They don't work well on mobile. Some work with midi. Get off your dang phone."
- Background: sky gradient from deep purple (#1a0a2e) through mid purple (#3d1c56), warm burgundy (#8b3a4f), gold (#d4856a), light gold (#eaa845), back through gold/warm to sky-dark and sky-black at the bottom
- Procedurally generated stars (80) with randomized positions, sizes, durations, and opacities
- Procedurally generated fireflies (20) with randomized paths and timing
- Hero image: `a_A_beautiful_garden_a.jpeg` with mask gradient and 0.8 opacity
- Two gold ornament lines (above and below title) with pulsing glow animation
- Scroll indicator at bottom:
  - "Enter" button that smooth-scrolls to the philosophy section and triggers the ambient hum
  - Three gold arrows in a row below the button
  - Entire indicator has a bobbing animation

### 2. Philosophy ("A Garden Grows")
- Two-column layout: philosophy text + garden illustration
- Garden illustration: `b_A_beautiful_garden_a.jpeg` with radial mask and drop-shadow, scales on hover (1.5s transition)
- Drop cap on first paragraph (gold, 4rem Cormorant Garamond)
- Text content:
  - Paragraph 1: "Every great synthesizer begins as a seed, I think. It is a quiet idea planted in the soil of curiosity, watered by late nights and the hum of a computer fan. Pizza rolls are often times present. Here, we tend to those seeds with care."
  - Paragraph 2: "This garden is a collection of desktop instruments, each one native to the machine it lives on. They are not emulations of hardware past. They are something new, sort of. They are tools grown from the unique character of the personal computer itself."
  - Paragraph 3: "We build for the future of music. For the producer at 2 AM. For the producer at 3 AM. For the producer at 3:30 AM. For the sound designer who hears something no one else has. For anyone who believes the desktop is not a limitation, it is a landscape. Put plants in it."
- Fade-in on scroll via IntersectionObserver
- Text paragraphs lighten on hover
- Background gradient transitions from sky-black to sky-light

### 3. Instruments ("What Grows Here")
- Three instrument cards in a grid, each linking to its subdomain:

| Card | Name | Subdomain | Description | Tag |
|------|------|-----------|-------------|-----|
| 1 | QWERTY Tempered | qwertytempered.thealternativedesktopsynthesizer.garden | An equal-tempered instrument born from the keys beneath your fingers. The keyboard becomes a keyboard. May we frighten you? | Experimental Tuning |
| 2 | Window Candy | windowcandy.thealternativedesktopsynthesizer.garden | A love letter to an era when the desktop was a frontier. Nostalgia rendered as sound, dial-up tones turned to drones. Is it practical? That's for me t