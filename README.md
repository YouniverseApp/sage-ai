# Sage AI Companion — local starter

## Requirements
- Node.js 22 or newer recommended
- An OpenAI API key with API access and billing configured

## Setup
1. Extract this folder to your computer.
2. Open a terminal in this folder.
3. Run: `npm install`
4. Copy `.env.example` to `.env`.
   - macOS/Linux: `cp .env.example .env`
   - Windows PowerShell: `Copy-Item .env.example .env`
5. Open `.env` in a text editor and replace `replace_with_your_key` with your API key.
   Never send the key to anyone, commit it to Git, or put it in files inside `public/`.
6. Start the app: `npm start`
7. Open http://localhost:3000 in your browser.

## Troubleshooting
- `Sage's AI is not configured yet`: ensure `.env` is in the project root, the key is set, then stop/restart the server.
- Authentication error: verify the key is valid and belongs to a project with API access.
- Usage/rate limit: check API billing and limits in the OpenAI Platform.
- Model error: set `OPENAI_MODEL` in `.env` to a model available to your API project.

## Security notes
- `.env` is excluded by `.gitignore`; keep it private.
- API calls are made by `server.js`, never directly from browser JavaScript.
- This is a local prototype, not ready for public launch. Before deployment, add user authentication, stronger rate limiting, CSRF/origin protections appropriate to your setup, privacy and retention controls, and a persistent/shared rate-limit store.
- Chat history lives only in the browser tab and is sent to the server when you send a message. It is not stored in a database by this starter, but API provider data handling still applies.
- If you believe the key was exposed, revoke it and create a new one.


## Sage personality profile
The server now includes Sage's expanded personality instructions: a warm, poetic, non-dogmatic spiritual companion drawing on Advaita Vedanta, Zen Buddhism, Stoicism, Sufism, and depth psychology. It also recognises the phrases "Roll 'em, Sage", "Synthesis, Sage", and "Candle of Return" as reflective modes.

To change Sage's personality later, edit the `systemInstructions` text near the top of `server.js`. Do not put your API key in that file; keep it in `.env`.
