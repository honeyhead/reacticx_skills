# Reacticx Skills for AI Coding Agents

AI agent skill for the **Reacticx** React Native component library (90+ production-ready animated components).

## Installation

### Using `npx skills` (Recommended)
```bash
npx skills add https://github.com/honeyhead/reacticx_skills --skill reacticx
```

### Manual Installation
```bash
# Claude Code
cp -r reacticx/ /path/to/your-project/.claude/skills/reacticx/

# OpenCode / Codex / other agents
cp -r reacticx/ /path/to/your-project/.agents/skills/reacticx/
```

## Skill Structure

```
reacticx_skills/
├── README.md
├── reacticx/                          # Canonical skill source
│   ├── SKILL.md                       # Main skill (178 lines)
│   └── references/                    # Loaded on-demand by category
│       ├── shaders.md                 # 8 shader components
│       ├── texts.md                   # 6 text animation components
│       ├── micro-interactions.md      # 9 micro interaction components
│       ├── components-carousels.md    # 13 carousel components
│       ├── components-navigation.md   # 13 navigation/layout components
│       ├── components-inputs.md       # 13 input/control components
│       └── components-display.md      # 28 display/feedback components
```

Installed via `npx skills add`, the tool auto-places it in the correct agent directory (`.claude/skills/`, `.agents/skills/`, etc.).
```

## Component Coverage

| Category | Count | Examples |
|----------|-------|---------|
| **Shaders** | 8 | Aurora, Mesh Gradient, Skia Ripple |
| **Texts** | 6 | Animated Text, Gooey Text, Fade Text |
| **Micro Interactions** | 9 | Gooey Switch, Elastic Slider, Hamburger |
| **Carousels** | 13 | Parallax, Tilt, Cinematic, Vertical Flow |
| **Navigation** | 13 | Bottom Sheet, Dynamic Island, Tabs |
| **Inputs** | 13 | Button, Picker, OTP, Switch, Search Bar |
| **Display** | 28 | Toast, Avatar, Shimmer, Progress, Glow |
| **Total** | **90+** | |

## Progressive Disclosure

The skill uses progressive context loading per the Anthropic skill-creator guidelines:
1. **SKILL.md** (178 lines) - Always loaded: setup, CLI, component index
2. **references/** - Loaded on-demand when agent needs specific component details

## Credits

- **Reacticx Library**: [@rit3zh](https://github.com/rit3zh)
- **Docs Source**: https://www.reacticx.com/docs
- **Skill Generation**: Claude Code Agent Teams (Orchestrator + 5 Workers + Reviewer)
