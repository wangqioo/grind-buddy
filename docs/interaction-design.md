# Interaction Design

## The Core Primitive: Eye Contact

K230 detects face orientation in real time — the device knows whether the user is looking at it.

This is the single most important technical decision in the project. It enables:
- Zero-friction interaction (no buttons, no wake word needed in normal use)
- Natural social protocol: eye contact precedes deeper attention
- Triggering expensive recognition only when it matters
- A felt distinction between "you're nearby" and "you're looking at me"

When the user looks at the device, it immediately turns to meet their gaze. This moment is the heartbeat of the entire product.

## Intent Detection

The same physical action carries different meaning depending on context. The LLM layer resolves ambiguity using accumulated user state.

Example — head tilt left:
- Doing neck stretches → mirror the motion together
- Deep in thought → tilt the other way, resonating curiosity
- Fatigue posture → soft, caring response
- Habitual idle movement → ignore

Local layer sees: "head offset 15 degrees." LLM layer understands: why.

## Voice Interaction

Microphone is always on (low power). Voice is only processed as directed input when eye contact is established. Otherwise treated as ambient audio — tone and energy feed into emotional state sensing without content processing.

Two activation modes:
1. Look at it → speak → it listens (zero friction, main mode)
2. Call its name → it responds (without eye contact, for explicit summons)

## Emotion State Machine

The device has its own emotional baseline that drifts independently over time. User inputs (eye contact, presence, ambient audio) are influences, not direct triggers.

This makes it feel like an independent life rather than a mirror.

## Sound Design

All sounds are non-verbal. Timbre and rhythm carry meaning:
- Short rising tone = happy
- Low drawn-out tone = sulking
- Volume: as quiet as possible. Aim for "did I imagine that?"

Sound categories:
- Arrival / departure tones
- Idle state murmurs
- Response sounds (to eye contact, to user actions)

## Motion Design

The gimbal's three axes enable rich expression:
- Pan + tilt + roll combinations create body language
- Easing curves matter more than the motion itself
- Small random micro-jitter in idle state = alive, not mechanical
- Screen expression and gimbal motion must be choreographed together

## Learning & Evolution

User attention is the implicit feedback signal. Motions that cause the user to look longer or lean closer are reinforced. Over months, each device develops idiosyncratic tendencies unique to its user relationship.
