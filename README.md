<div align="center">

<p align="center">
  <a href="https://github.com/user-attachments/assets/3fdeb5ad-e832-4bbf-a879-bb22c35d0ea0">
    <img src="./src/assets/demo.webp" width="900" alt="Forge Demo">
  </a>
</p>

# Forge

**A full IDE in your browser. No install. No server. Just code.**

[**→ Try it live**](https://forge.vivekjadhav.xyz) · [Report a bug](https://github.com/vivek1504/forge/issues) · [Request a feature](https://github.com/vivek1504/forge/issues)

[![Stars](https://img.shields.io/github/stars/vivek1504/forge?style=flat&color=yellow)](https://github.com/vivek1504/forge/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/vivek1504/forge/blob/main/LICENSE)
![Forge](https://img.shields.io/badge/Forge-v1.2.0-blue)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite)

</div>

---

> If Forge is useful to you, a ⭐ helps others find it — thank you!

---

## What is this?

Forge runs a **real Node.js environment directly in your browser tab** using [WebContainers](https://webcontainers.io/). Pick a framework, start coding, and see a live preview — all without touching your terminal or installing anything.

No Docker. No cloud VM. No backend. It's all client-side.

**Why Forge over StackBlitz or CodeSandbox?** Forge is fully open-source, self-hostable, and has zero vendor lock-in. It's also a clean, minimal reference implementation — no accounts, no paywalls, no telemetry. Just the code, fully readable and forkable.

## Try it

**[forge.vivekjadhav.xyz](https://forge.vivekjadhav.xyz)**

---

## Features

- **Zero setup** — open the URL and you're coding in seconds
- **Real runtime** — actual Node.js in the browser, not a sandbox simulator
- **Live preview** — HMR-powered preview updates as you type
- **Monaco editor** — the same editor that powers VS Code
- **Integrated terminal** — full xterm.js terminal, not a fake console
- **File explorer** — create, rename, and delete files like a real IDE
- **Download as zip** — export your project and keep working locally
- **100% client-side** — no server, no accounts, no data sent anywhere

---

## Supported frameworks

| Framework | Status |
|-----------|--------|
| React + Vite | ✅ |
| Vue + Vite | ✅ |
| Svelte + Vite | ✅ |
| Node.js | ✅ |
| Next.js | 🔜 Coming soon |
| Remix | 🔜 Coming soon |

---

## Run it locally

```bash
git clone https://github.com/vivek1504/forge.git
cd forge
npm install
npm run dev
```

Open `http://localhost:5173`.

> **Note:** WebContainers require `Cross-Origin-Isolation` headers (`COOP` + `COEP`). The dev server sets these automatically via the Vite config.

---

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

---

## Project structure

```
src/
├── components/
│   ├── CodeEditor.tsx        # Monaco editor wrapper
│   ├── Terminal.tsx          # xterm.js terminal
│   ├── Sidebar.tsx           # File explorer
│   ├── PreviewFrame.tsx      # Live preview iframe
│   ├── IdeHeader.tsx
│   └── IdeFooter.tsx
├── lib/
│   ├── webContainerRuntime.ts    # WebContainer setup & lifecycle
│   ├── webContainerManager.ts    # Instance management
│   ├── projectFiles.ts           # Framework templates
│   ├── atoms.ts                  # Jotai state
│   └── utils.ts
└── pages/
    ├── LandingPage.tsx
    └── IDEpage.tsx
```

---

## Contributing

PRs are welcome — especially for new framework templates and bug fixes.

- **New framework template?** → `src/lib/projectFiles.ts` is where templates live
- **Testing:** Run `npm run dev` and verify HMR, terminal, and file explorer work end-to-end in Chrome (WebContainers have best support there)

If you're unsure whether something is worth building, open an issue first and let's talk.

---

## License

MIT — do whatever you want with it.
