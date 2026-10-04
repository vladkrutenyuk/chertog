# Chertog

> Чертоги пышные построю
> Из бирюзы и янтаря.
>
> — М. Ю. Лермонтов, «Демон»

*I will build lavish halls of turquoise and amber.*

**Chertog** (Russian *чертог* — a palace, a hall; as in *чертоги разума*, the "mind palace") is a minimal graphical shell built around spatial memory.

It is not a distro and not a kernel. Chertog runs on top of a bare, terminal-only Ubuntu install and becomes the only thing you see on screen: Ubuntu underneath, Chertog on top.

> ⚠️ Early concept stage. Nothing works yet.

## The idea

No windows. No panels. No menus. The whole screen is split into three zones:

```
┌──────────┬───────────────────────────────────┐
│          │                                   │
│   File   │                                   │
│   tree   │              Canvas               │
│          │                                   │
│          │                                   │
│          ├───────────────────────────────────┤
│          │  bash   [tab 1] [tab 2]           │
└──────────┴───────────────────────────────────┘
```

- **File tree** on the left, full height — where your files *are*.
- **Terminal** at the bottom — a classic bash terminal with tabs, nothing more.
- **Canvas** everywhere else — where your files *live in your head*.

### The canvas

An infinite zoomable space where you place any file wherever you want, and remember things by *where* they are rather than by their path — like a memory palace.

- **Any file can live on the canvas**, as long as a handler for its format exists.
- **Level of detail.** Each format defines how it looks from far away, up close, and at which point it becomes interactive. An image starts as a color spot and ends as an editable picture; a text file starts as a label and ends as an editor.
- **Rooms.** Group things by placing them together. A room looks like a single object from afar — zoom in, and its contents appear. Rooms nest infinitely.
- **Commands anywhere.** Click on empty space, type a command, run it — the output appears right there and stays on the canvas. No calculator app needed.
- **Your files stay untouched.** The canvas layout is stored separately as plain text and only references paths.

### Configured with text

The system is managed the way bare Ubuntu always is — through its standard config files and the terminal. Chertog itself follows the same rule: layout, colors, keybindings and canvas behavior live in plain config files in one known place. No settings apps.

### AI-native potential

Since the entire system is text — configs, canvas layouts, and documentation (`README.md`, guides, `AGENTS.md`) — an AI agent running inside it can understand how everything works from the start, and change it the same way a human would: by editing files.

## Status

Concept and design. Planned stack: Rust, a GPU renderer, and an embedded terminal core.
