# Forge

A real in-browser IDE powered by WebContainers. Code, build, and run projects directly in your browser with zero setup.

<p align="center">
  <img
    src="https://res.cloudinary.com/dj7gqjguy/image/upload/v1779355997/forge-demo_xp6s5r.gif"
    alt="Forge Demo"
    width="100%"
  />
</p>

![Forge](https://img.shields.io/badge/Forge-v1.2.0-blue)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite)

## Features

- **Instant Start** - Pick a framework and start coding immediately. No configuration needed.
- **Multiple Frameworks** - Support for React, Vue, Svelte, and Node.js projects
- **Monaco Editor** - VS Code-like editing experience with syntax highlighting
- **Integrated Terminal** - Full terminal with xterm.js integration
- **Live Preview** - See your changes in real-time with HMR support
- **File Explorer** - Navigate and manage project files with ease
- **Download Projects** - Export your project as a zip file
- **Runs Entirely in Browser** - Powered by WebContainers, no server required

## Tech Stack

- **Frontend**: React 19, TypeScript, TailwindCSS 4
- **Editor**: Monaco Editor
- **Terminal**: xterm.js
- **Runtime**: WebContainers API
- **Build**: Vite 7
- **Animations**: Framer Motion
- **State Management**: Jotai
- **Routing**: React Router v7

## Getting Started

### Prerequisites

- Node.js 18+ 
- npm or pnpm

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/forge.git
cd forge

# Install dependencies
npm install

# Start development server
npm run dev
```

The app will be available at `http://localhost:5173`

### Build for Production

```bash
npm run build
npm run preview
```

## Project Structure

```
src/
├── components/              # React components
│   ├── ui/                  # Reusable UI components
│   ├── CodeEditor.tsx       # Monaco editor wrapper
│   ├── Terminal.tsx         # xterm.js terminal
│   ├── Sidebar.tsx          # File explorer sidebar
│   ├── IdeHeader.tsx        # IDE top navigation
│   ├── IdeFooter.tsx        # IDE status bar
│   ├── PreviewFrame.tsx     # Live preview iframe
│   ├── HeroSection.tsx      # Landing hero section
│   ├── FeaturesSection.tsx  # Landing features section
│   └── FrameworkSection.tsx # Framework picker
├── lib/                     # Core libraries
│   ├── webContainerRuntime.ts  # WebContainer setup & commands
│   ├── webContainerManager.ts  # WebContainer instance management
│   ├── projectFiles.ts         # Framework templates
│   ├── terminalSingleton.ts    # Terminal instance
│   ├── atoms.ts                # Jotai state atoms
│   ├── store.ts                # Global store
│   ├── types.ts                # TypeScript types
│   └── utils.ts                # Utility functions
├── pages/                   # Page components
│   ├── LandingPage.tsx
│   └── IDEpage.tsx
└── main.tsx                 # App entry point
```

## Supported Frameworks

| Framework | Status | Description |
|-----------|--------|-------------|
| React | ✅ Available | Build interactive UIs with Vite |
| Vue | ✅ Available | Progressive framework with Vite |
| Svelte | ✅ Available | Cybernetically enhanced apps |
| Node.js | ✅ Available | Server-side JavaScript |
| Next.js | 🔜 Coming Soon | Full-stack React framework |
| Remix | 🔜 Coming Soon | Full stack web framework |

## Configuration

The IDE uses sensible defaults, but you can customize:

- **Terminal scrollback**: Configured in `terminalSingleton.ts`
- **Editor theme**: Monaco editor settings in `CodeEditor.tsx`
- **Project templates**: Add new frameworks in `projectFiles.ts`

## License

MIT License - feel free to use this project for personal or commercial purposes.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

Built with ❤️ using WebContainers
