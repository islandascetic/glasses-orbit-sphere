# Glasses Orbit Sphere

A 600x600 Meta Ray-Ban Display Web App prototype that renders a Three.js sphere-like object and creates a room-anchored illusion from browser sensor input.

## What it does

- Fixed 600x600 viewport for MRBD Web Apps.
- Uses Three.js for a polished glowing sphere/orbit object.
- On start, anchors the sphere at the current glasses orientation.
- Uses `DeviceOrientationEvent` to estimate where that anchor should appear on screen.
  - Look away from the anchor and the sphere moves off screen.
  - Look back toward the anchor and it re-enters the display.
- Uses `DeviceMotionEvent` as a rough near/far signal when available.
- Supports keyboard-only testing:
  - Enter: start sensors / re-anchor sphere in front of you
  - Up/Down: simulate walking closer/farther
  - Left/Right: simulate looking/rotating relative to the anchor

## Important limitation

This is a spatial illusion, not true room-scale positioning.

Web Apps can access orientation and motion sensors, but they do not expose reliable absolute indoor position tracking. The distance behavior in this prototype is approximate/manual. For true room-relative position and robust walking closer/farther, a native DAT/ARKit-style helper or another tracking bridge would likely be needed.
