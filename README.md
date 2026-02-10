# Reacticx Skills for AI Coding Agents

A comprehensive Claude Code / OpenCode skill for the **Reacticx** React Native component library. This skill provides AI coding agents with complete reference documentation for 90+ production-ready animated components.

## What is Reacticx?

[Reacticx](https://www.reacticx.com) is a headless, animation-focused component library for React Native featuring 60+ production-ready components with smooth 60fps animations built on React Native Reanimated and Skia.

## What is this repo?

This repository contains an **AI agent skill file** that can be used with:

- **Claude Code** (Anthropic's CLI)
- **OpenCode** or any AI coding tool that supports markdown skill files

When loaded, the skill gives your AI assistant full knowledge of:

- All Reacticx components (90+)
- Props/API reference for each component
- Installation commands and dependencies
- Usage examples and patterns
- Best practices

## Installation

### For Claude Code

**Option 1: Clone into your project**
```bash
# In your React Native project root
mkdir -p .claude/skills
curl -o .claude/skills/reacticx.md https://raw.githubusercontent.com/honeyhead/reacticx_skills/main/skills/reacticx.md
```

**Option 2: Clone the full repo**
```bash
git clone https://github.com/honeyhead/reacticx_skills.git
cp reacticx_skills/skills/reacticx.md /path/to/your-project/.claude/skills/
```

**Option 3: Use the `.claude/skills` directory directly**
```bash
# Clone this repo, then symlink or copy the .claude directory
cp -r reacticx_skills/.claude/skills/reacticx.md ~/.claude/skills/
```

### For OpenCode

Copy the skill file to your OpenCode skills directory:
```bash
cp skills/reacticx.md /path/to/opencode/skills/
```

### Manual Setup

Simply copy `skills/reacticx.md` into whatever directory your AI coding tool reads skill files from.

## Component Coverage

| Category | Count | Examples |
|----------|-------|---------|
| **Shaders** | 8 | Aurora, Mesh Gradient, Skia Ripple |
| **Texts** | 6 | Animated Text, Gooey Text, Fade Text |
| **Micro Interactions** | 9 | Gooey Switch, Elastic Slider, Hamburger |
| **Components** | 67+ | Accordion, Toast, Picker, Carousel variants |
| **Total** | **90+** | |

## Skill Structure

```
reacticx_skills/
├── README.md                          # This file
├── .claude/
│   └── skills/
│       └── reacticx.md               # For Claude Code (project-level)
└── skills/
    └── reacticx.md                    # Universal skill file
```

## Usage Example

Once the skill is installed, your AI agent can:

```
You: "Add a gooey switch toggle to my settings screen"
Agent: [Uses skill knowledge to provide correct import, props, and usage]
```

```
You: "Create a carousel with parallax effect for my image gallery"
Agent: [Knows ParallaxCarousel component, its props, dependencies, and setup]
```

## Updating

The skill was generated from the official Reacticx documentation at https://www.reacticx.com/docs. To update:

1. Pull the latest version of this repo
2. Copy the updated skill file to your project

## Contributing

If you find missing components or incorrect props, please open an issue or PR.

## Credits

- **Reacticx Library**: Created by [@rit3zh](https://github.com/rit3zh)
- **Skill Generation**: Automated with Claude Code Agent Teams
- **Documentation Source**: https://www.reacticx.com/docs

## License

This skill file is a documentation reference derived from the Reacticx open-source project. The Reacticx library itself is maintained by its original author.
