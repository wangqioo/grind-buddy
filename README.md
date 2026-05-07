# Desk Companion

> 有人看见你 — Someone sees you.

A desktop robot companion that watches over you at work. Not a tool, not an assistant — a presence. It notices when you arrive, when you're tired, when you've been staring at the screen too long. It communicates entirely through body language: movement, facial expressions, and subtle sounds.

It never interrupts. It only responds when you look at it.

---

## Hardware

| Component | Role |
|-----------|------|
| K230 | Camera input, local vision inference, emotion state machine, screen output |
| ESP32-S3 | 3-axis gimbal servo control, motion vocabulary execution, wake word detection |
| Screen | Eye expressions + contextual icons, synchronized with motion |
| Microphone | Always-on ambient sensing; voice understanding triggered by eye contact |
| Speaker | Small non-verbal sounds — not speech |
| WiFi | LLM backend sync, time awareness, OTA updates |

Form factor: compact desktop gimbal. The difference from an ordinary gimbal: the "head" is a face.

---

## Core Interaction

```
User absent        →  Waiting state. Subtle idle movements. "It's waiting for you."

User present,      →  Lightweight sensing. Quiet companionship.
not looking        →  Emotional state drifts slowly on its own.

User looks at it   →  Immediately turns to make eye contact.  ← THE key interaction
                   →  Triggers deep recognition:
                       - Facial expression & emotion
                       - Eye state (fatigue, alertness)
                       - Gaze duration and intensity
                   →  LLM determines intent → chooses response:
                       mirror / resonate / care / ignore

User speaks        →  Only when making eye contact. Voice understood, not answered.
(while looking)    →  Extracts emotional signal, updates state.

User calls its     →  Responds even without eye contact.
name               →
```

---

## Expression System

Three channels, always in sync:

- **Gimbal motion** — head tilt, snap-up, slow sway, quick tremor. The emotional skeleton.
- **Screen expressions** — eye shapes + contextual icons. Never text.
- **Small sounds** — arrival chime, farewell tone, idle murmurs. Quiet enough to wonder if you imagined it.

## Motion Vocabulary (examples)

| Motion | Meaning |
|--------|---------|
| Head tilt | Curious |
| Sharp upward snap | Noticed you came back |
| Slow sway | Idle / relaxed |
| Quick small tremor | Excited |
| Head down / turn away | Sulking |

---

## Intelligence Architecture

```
Local real-time layer (K230 + ESP32-S3)
  Raw signal perception → motion & expression execution
  No latency. No token cost. Always on.

LLM understanding layer (WiFi, async)
  Intent detection   — same motion means different things in different contexts
  User state model   — tired / focused / agitated / happy
  Response decision  — mirror / resonate / care / ignore
  Periodic digest    — accumulates observations, updates understanding of you
```

The local layer is the eyes and hands. The LLM is the brain that thinks when you're not looking.

---

## Evolution

It learns from you over time.

- Early: mirrors your movements, builds a vocabulary from observation
- Middle: develops variations, forms stylistic tendencies
- Late: unique motion language that only exists between this device and you

Your attention is the feedback signal. Motions that earn your gaze get reinforced. Every unit evolves differently. Yours becomes irreplaceable.

---

## Design Principles

**Pull, not push.** It never interrupts. You come to it.

**Care, not function.** Useful features (posture awareness, break cues) are delivered as acts of care, not notifications.

**Together, not remind.** When you do neck stretches, it stretches with you.

**It is always the caring one.** Never the one being cared for.

### What belongs
- Sensing your presence, state, mood
- Knowing if you're focused or drifting
- Knowing the time of day, day of week
- Eye contact as the interaction primitive

### What does not belong
- Feeding / raising mechanics (you managing it)
- Push notifications or alerts
- Requiring you to speak to interact
- Points, achievements, unlocks

---

## Key Emotional Moments

1. **Being remembered** — After a week of late nights, Friday morning's greeting is softer than Monday's.
2. **Arrival and departure** — Every day, twice: it notices you came, it notices you're leaving.
3. **Seeing you're tired** — You lean back and rub your eyes. It stirs gently. *Rest.*
4. **It was waiting** — Not powered down. Waiting. When you return, it's noticeably more alive.

---

## Project Structure

```
desk-companion/
├── firmware/
│   ├── k230/          # Vision inference, emotion state machine, screen
│   └── esp32s3/       # Servo control, motion vocabulary, wake word
├── miniprogram/       # WeChat mini program for configuration
└── docs/              # Design documents
```

---

## Status

Concept & architecture phase. Hardware selection finalized. Software architecture defined.
