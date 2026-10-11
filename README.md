# Tinder AI Frontend — Course Version

A React interface for browsing generated profiles, creating matches, and chatting through a companion backend.

## Features

- Browse profiles and accept or skip them.
- View matches and open conversations.
- Send chat messages and refresh conversation history.

## Requirements

- Node.js `^18.0.0 || >=20.0.0` and npm.
- A running backend exposing profiles, matches, conversations, and images.

## Run locally

```sh
git clone https://github.com/PravatKumaraMishra/Tinder_Ai_Frontend.git
cd Tinder_Ai_Frontend
npm ci
```

This version hardcodes `http://localhost:8080` for API calls and profile images in `src/App.jsx`. Run a compatible backend at that address and allow the frontend origin in its CORS settings. The newer [TinderAiFrontend](https://github.com/PravatKumaraMishra/TinderAiFrontend) separates API helpers and uses an environment variable.

Browse a profile, accept it, switch to matches, and send a message.

```sh
npm run dev
```

Open the local URL printed by Vite (normally `http://localhost:5173`).

## Available commands

| Command | Script |
| --- | --- |
| `npm run dev` | `vite` |
| `npm run build` | `vite build` |
| `npm run lint` | `eslint . --ext js,jsx --report-unused-disable-directives --max-warnings 0` |
| `npm run preview` | `vite preview` |

`npm run preview` serves the output of `npm run build`; it does not build the project itself.

## Project structure

- `src/App.jsx`: screens, state, and API requests.
- `src/main.jsx`: React entry point.
- `tailwind.config.js`: styling configuration.

## Notes

The UI needs the backend to return profiles and conversations. Check backend availability, its image route, and CORS if the screen remains on Loading. Backend AI configuration is documented in its repository. This is a learning application. Original course reference: https://javabrains.io/products/digital_downloads/tinder-ai
