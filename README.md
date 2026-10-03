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

## Install and share

The web app manifest and PNG icons provide install metadata for supported browsers, including Apple home-screen support. The Open Graph preview graphic is `og.png` (1200 × 630), referenced at `https://hum-runner.netlify.app/og.png`; social crawlers need the image at that publicly reachable URL.

## Analytics (optional)

Cloudflare Web Analytics is wired in as an opt-in page-view beacon and is disabled until configured. In Cloudflare, open **Web Analytics → Add a site**, add the deployed hostname, and copy the token from the manual snippet. Set `CLOUDFLARE_ANALYTICS_TOKEN` near the end of `index.html` to that token, then deploy. Cloudflare's beacon measures site visits and does not access or send microphone audio; it does not report gameplay events or scores.

## Production checklist

- Deploy over HTTPS and confirm microphone permission and touch fallback on real phones.
- Verify the social preview from the live URL after setting the absolute `og:image` address.
- Confirm the manifest and icon load at the deployed paths and test Add to Home Screen on target devices.
- Enable analytics only after configuring the Cloudflare-issued token for the deployed hostname.
- Test the live game in Chrome, Safari on iPhone, Firefox, and Samsung Internet, including mic denial, silence/noise, and tab switching.

## Browser notes

Use a modern browser with microphone permissions and Web Audio support. If microphone access is denied or unavailable, choose **Play without mic** from the prompt.
