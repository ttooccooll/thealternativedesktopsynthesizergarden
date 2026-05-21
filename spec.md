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
| 2 | Window Candy | windowcandy.thealternativedesktopsynthesizer.garden | A love letter to an era when the desktop was a frontier. Nostalgia rendered as sound, dial-up tones turned to drones. Is it practical? That's for me to know and for you to know too, unless you don't want to. idk | Canned Nostalgia |
| 3 | Labyrinth | labyrinth.thealternativedesktopsynthesizer.garden | An instrument that tends itself. Knobs turn without your touch, parameters drift like wind through olive branches. Surrender control. Try playing some notes and hitting the wild button frantically for a different, less pleasant approach. | Autonomous Synth |

- Each card has a full-width screenshot with triple-layered flamboyant border (inner gold gradient, dark outer frame, outermost gold gradient)
- Screenshots at 55% opacity by default, fully opaque on hover
- Hover effects: lift (-8px), gold border glow, radial gradient overlay, gold top-line reveal, heading color change, paragraph text shifts to gold-light with 2px lift
- Background gradient transitioning from sky-light to transparent

### 4. Vision
- Centered layout
- Bridge text: "These are not static tools. They are living instruments, meant to evolve with you. It is indeed go time, broski. Grab a light beer and do your thang miss twang."
- Vine divider SVG with lavender and jasmine flowers, leaves, and curving stems
- Quote: "We do not build synthesizers to recreate the past. We grow synthesizers to recreate the present."
  - Gold decorative lines on left/right that expand on hover
- Supporting text: "Each instrument in this garden is free to use, free to modify, and free to inspire. The desktop is our soil. Water is our liquid. Sound is what blooms."

### 5. Call to Action
- Flux image at top with slow hover scale (1.5s)
- "Step inside and see what has taken root." text (gold, italic Cormorant Garamond)
- Gold ornament divider
- Button row: "Explore the Garden" link → small recraft image → "Don't Explore the Garden" button
- "Explore the Garden" links to `#instruments` and triggers a plink sound
- Terracotta-to-gold gradient background on buttons
- Hover effects: ripple expansion, gradient shift to gold/terracotta, box-shadow glow, slight lift

### 6. Footer
- Background image: `b_A_beautiful_garden_a.jpeg` with mask gradient and 0.15 opacity
- Gold gradient overlay from bottom
- Gold ornament line
- Copyright: "The Alternative Desktop Synthesizer Garden - 2026"
- Footer text lightens to gold on hover

## Visual Design

### Color Palette
- **Sky**: sky-black (#0d031a), sky-dark (#240b36), sky-deep (#1a0a2e), sky-mid (#3d1c56), sky-warm (#8b3a4f), sky-gold (#d4856a), sky-light (#eaa845)
- **Earth tones**: stone (#c4a882), stone dark (#8b7355), terracotta (#c67b5c), terracotta dark (#a05a3c)
- **Florals**: lavender light (#c4b5d0)
- **Accents**: gold (#d4a853), gold light (#f0d48a), cream (#f5efe6)
- **Text**: light (#f0e6d6), muted (#c4b5a0)

### Animations
- **Twinkle** - star opacity oscillation (0.2 to variable max, 2-6s duration)
- **Float** - firefly movement with CSS custom properties for dx/dy (6-14s duration)
- **Ornament glow** - brightness pulsing on decorative gold lines (4s cycle)
- **Bob** - scroll indicator vertical oscillation (2s cycle, 8px displacement)
- **Fade-in** - elements appear on scroll via IntersectionObserver (threshold: 0.1)
- **Card hover** - lift, glow, and color transitions with cubic-bezier easing
- **Text hover** - paragraphs and titles lighten on hover
- **Vine divider hover** - opacity increase and slight scale
- **CTA button hover** - ripple expansion, gradient shift, box-shadow glow
- **Image hover** - slow 1.5s scale and filter transitions

### Responsive Breakpoints
- 1200px - reduced gaps (3rem/2rem), garden illustration height 500px, philosophy text light
- 900px - single-column philosophy, garden illustration moves above text (order: -1), single-column instruments (max-width 400px), hero image height 50%
- 600px - reduced padding (4rem/1.5rem), hero padding 1.5rem, hero subtitle 1rem, scroll indicator bottom 2rem, philosophy padding-top 6rem, garden illustration 350px, instrument card padding reduced, CTA padding 5rem/1.5rem, CTA illustration 250px, button 0.8rem/2rem at 1rem font, footer padding 5rem/1rem/2rem
- 400px - hero h1 2rem, section title 1.6rem, garden illustration 280px, reduced chaos shake (no rotation, smaller translations)

## Audio Features

### Ambient Hum
- Triggered on first user interaction (Enter button or any click)
- **14-voice Cmaj9#11 chord** spread across 4+ octaves:
  - C1 sub (32.70 Hz, sine) × 3 detuned voices
  - C2 (65.41 Hz, triangle)
  - E3 (164.81 Hz, sawtooth)
  - B3 (246.94 Hz, sawtooth)
  - F#4 (369.99 Hz, sawtooth)
  - A4 (440.00 Hz, sawtooth)
  - D5 (587.33 Hz, triangle)
  - G5 (783.99 Hz, sine)
  - C#6 (1108.73 Hz, sine)
  - E6 (1321.00 Hz, sine)
  - G#6 (1663.00 Hz, sine)
  - B7 (1975.53 Hz, sine)
- **Staggered entry** — each note fades in 1.2s after the previous, with 5-9 second individual ramps (~18 second total bloom)
- **Pitch glide** — all voices modulated by a 0.03Hz LFO (±6.2 semitones, ~33s cycle)
- **Per-voice LFOs** — volume modulation (0.015-0.055Hz) and detune modulation (0.01-0.04Hz)
- **4 filter sweeps** at different speeds:
  - Lowpass at 1200Hz (0.008-0.02Hz)
  - Bandpass at 700Hz (0.004-0.012Hz)
  - Highpass at 100Hz (0.02-0.04Hz)
  - Bandpass at 400Hz (0.015-0.025Hz)
- **Stereo panning** on higher notes (A4+) with independent LFOs
- **Tape saturation** via tanh waveshaper
- **Chorus** with modulated delay and breathing mix
- **7-second convolution reverb** with synthetic impulse response
- **Delay** with feedback loop feeding into reverb

### Plink Sound
- Triggered on "Enter" button and "Explore the Garden" link
- **4 notes** (C#6, E6, G#6, B7) staggered 40ms apart with 1.5s decay
- **Echo delay** — 300ms left, 380ms right with lowpass filter, panning LFO, and 0.5 feedback
- **8-second convolution reverb** for cosmic space

### "Don't Explore the Garden" Chaos
- **Screen shake** — 20 iterations of violent translation + rotation (reduced on mobile)
- **Color flash** — rapid hue rotation, saturation spikes, and inversion on the sky gradient
- **Horrible noise** — 3-second stereo buffer with:
  - 10 detuned oscillators with LFO frequency modulation
  - 3 FM synthesis voices with aggressive carrier modulation
  - 3 ring modulation pairs
  - 3 noise layers
  - Click trains, siren sweeps, drill sounds
  - 5 sub-bass oscillators (18-35 Hz)
  - 3 rumble layers (32-50 Hz)
  - Low growl with FM modulation
  - Heavy waveshaper distortion (k=200)
  - Dynamics compressor

## Key Design Decisions

- **Single file** - HTML, CSS, and JS all in one file for portability and zero build step
- **External images** - uses JPEG/PNG files for visual richness (hero, illustrations, instrument screenshots, CTA section)
- **No frameworks** - vanilla HTML/CSS/JS only
- **Garden metaphor** - consistent visual language throughout (plants, vines, earth tones, gold accents)
- **Desktop-native philosophy** - instruments are designed for the personal computer, not emulations of hardware
- **Conversational tone** - text mixes poetic imagery with casual, self-deprecating humor and asides
- **Subdomain architecture** - each instrument lives on its own subdomain of thealternativedesktopsynthesizer.garden
- **Audio-first experience** - ambient hum, plink sounds, and chaos audio are core to the experience
