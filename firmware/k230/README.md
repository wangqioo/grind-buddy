# K230 Firmware

Responsibilities:
- Camera input & face orientation detection (is user looking at device?)
- Local vision model inference (expression, fatigue, gaze duration)
- Emotion state machine
- Screen expression output (eyes, contextual icons)
- High-level intent commands to ESP32-S3 (e.g. `emotion=curious`)
- LLM communication over WiFi (async, non-real-time)
