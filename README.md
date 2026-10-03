# Hum Runner

A small browser game where you guide a ball through gaps by humming. Higher pitches move the ball up, lower pitches move it down, and silence lets it sink. The game also includes touch controls for playing without a microphone.

## Run locally

Microphone access requires a secure context. For local development, serve this folder from `localhost` (or deploy it over HTTPS), then open the page in a browser. Opening `index.html` directly from the filesystem may prevent microphone access.

No build step or dependencies are required.

## How to play

1. Choose **Start and allow mic** and grant microphone access.
2. Follow the prompts to hum your lowest and highest comfortable notes for calibration.
3. Hum higher to climb, lower to descend, and stop humming to sink. Pass through the gaps without hitting a wall.
4. If you prefer not to use a microphone, choose **Play without mic** and drag or touch to guide the ball.

The game includes a mute toggle, a microphone level indicator, pause/resume controls, and automatically pauses when the tab loses focus. Your best score is stored in the browser.

## Browser notes

Use a modern browser with microphone permissions and Web Audio support. If microphone access is denied or unavailable, choose **Play without mic** from the prompt.
