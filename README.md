# Glasses Orbit Sphere

A 600x600 Meta Ray-Ban Display Web App prototype that renders a Three.js sphere-like object and changes the view using browser sensor input.

## What it does

- Fixed 600x600 viewport for MRBD Web Apps.
- Uses Three.js for a polished glowing sphere/orbit object.
- Uses `DeviceOrientationEvent` for yaw/pitch/roll when available.
- Uses `DeviceMotionEvent` as a rough near/far signal when available.
- Supports keyboard-only testing:
  - Enter: request/start sensors
  - Up/Down: adjust test distance
  - Left/Right: rotate test angle

## Important limitation

Web Apps can access orientation and motion sensors, but they do not expose reliable absolute indoor position tracking. The distance behavior in this prototype is an approximation/test control, not true spatial localization.

For true world-relative position, a native DAT/ARKit-style helper or another tracking bridge would likely be needed.
