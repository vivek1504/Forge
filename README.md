<div align="center">

<img src="https://res.cloudinary.com/dj7gqjguy/image/upload/v1779355997/forge-demo_xp6s5r.gif" alt="Forge Demo" width="100%" />

# Forge

**A full IDE in your browser. No install. No server. Just code.**

[**→ Try it live**](https://forge.vivekjadhav.xyz) · [Report a bug](https://github.com/vivek1504/forge/issues) · [Request a feature](https://github.com/vivek1504/forge/issues)

[![Stars](https://img.shields.io/github/stars/vivek1504/forge?style=flat&color=yellow)](https://github.com/yourusername/forge/stargazers)
![Forge](https://img.shields.io/badge/Forge-v1.2.0-blue)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite)

</div>

---

> If Forge is useful to you, a ⭐ helps others find it — thank you!

---

## What is this?

Forge runs a real Node.js environment directly in your browser tab using [WebContainers](https://webcontainers.io/). Pick a framework, start coding, and see a live preview — all without touching your terminal or installing anything.

No Docker. No cloud VM. No backend. It's all client-side.

## Try it

**[forge.vivekjadhav.xyz](https://forge.vivekjadhav.xyz)**

## Features

- **Zero setup** — open the URL and you're coding in seconds
- **Real runtime** — actual Node.js in the browser, not a sandbox simulator
- **Live preview** — HMR-powered preview updates as you type
- **Monaco editor** — the same editor that powers VS Code
- **Integrated terminal** — full xterm.js terminal, not a fake console
- **File explorer** — create, rename, delete files like a real IDE
- **Download as zip** — export your project and keep working locally
- **Runs 100% client-side** — no server, no data sent anywhere

## Supported frameworks

| Framework | Status |
|-----------|--------|
| React + Vite | ✅ |
| Vue + Vite | ✅ |
| Svelte + Vite | ✅ |
| Node.js | ✅ |
| Next.js | 🔜 Coming soon |
| Remix | 🔜 Coming soon |

## How it works

WebContainers is a browser-based runtime from StackBlitz that boots a real Node.js environment using WebAssembly. Forge wraps this with a Monaco editor, an xterm.js terminal, and a live preview iframe to give you a complete IDE experience — entirely in a browser tab.

The hard parts: getting SharedArrayBuffer headers right, managing WebContainer lifecycle, syncing the file system with the editor, and keeping the terminal responsive. The repo shows how all of that fits together.

## Run it locally

```bash
git clone https://github.com/yourusername/forge.git
cd forge
npm install
npm run dev
```

Open `http://localhost:5173`. Note: WebContainers requires `Cross-Origin-Isolation` headers — the dev server handles this automatically.

## Tech stack

| Layer | Library |
|-------|---------|
| Framework | React 19 + TypeScript |
| Editor | Monaco Editor |
| Terminal | xterm.js |
| Runtime | WebContainers API |
| Build | Vite 7 |
| Styling | TailwindCSS 4 |
| State | Jotai |
| Routing | React Router v7 |
| Animations | Framer Motion |

## Project structure

```
src/
├── components/
│   ├── CodeEditor.tsx       # Monaco editor wrapper
│   ├── Terminal.tsx         # xterm.js terminal
│   ├── Sidebar.tsx          # File explorer
│   ├── PreviewFrame.tsx     # Live preview iframe
│   ├── IdeHeader.tsx
│   └── IdeFooter.tsx
├── lib/
│   ├── webContainerRuntime.ts   # WebContainer setup & lifecycle
│   ├── webContainerManager.ts   # Instance management
│   ├── projectFiles.ts          # Framework templates
│   ├── atoms.ts                 # Jotai state
│   └── utils.ts
└── pages/
    ├── LandingPage.tsx
    └── IDEpage.tsx
```

## Contributing

PRs are welcome. If you're adding a new framework template, the relevant file is `src/lib/projectFiles.ts`.

## License

MIT
