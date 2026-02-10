<p align="center">
  <h1 align="center">Reacticx Skills</h1>
  <p align="center">AI Agent Skill for Reacticx React Native Component Library</p>
</p>

<p align="center">
  <a href="#english">English</a> | <a href="#한국어">한국어</a> | <a href="#日本語">日本語</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/components-90%2B-blue" alt="90+ Components" />
  <img src="https://img.shields.io/badge/score-8.2%2F10-green" alt="Score 8.2/10" />
  <img src="https://img.shields.io/badge/agents-Claude%20%7C%20Codex%20%7C%20OpenCode-purple" alt="Multi-Agent" />
</p>

---

## English

### What is this?

An AI agent skill that gives your coding assistant complete knowledge of the [Reacticx](https://www.reacticx.com) React Native component library — 90+ production-ready animated components with 60fps animations.

### Quick Start

```bash
# Install with npx skills (Recommended)
npx skills add https://github.com/honeyhead/reacticx_skills --skill reacticx
```

Then add to your project root for automatic triggering:

```markdown
<!-- CLAUDE.md or .agents/instructions.md -->
This project uses the Reacticx library for UI components.
Always check Reacticx components first when building UI.
```

### Manual Installation

```bash
# Claude Code
cp -r reacticx/ your-project/.claude/skills/reacticx/

# OpenCode / Codex / Other agents
cp -r reacticx/ your-project/.agents/skills/reacticx/
```

### Skill Architecture

```
reacticx/
├── SKILL.md (199 lines)              # Always loaded: setup, CLI, component index
└── references/ (10 files)            # Loaded on-demand per category
    ├── shaders.md                    # Aurora, Mesh Gradient, Skia Ripple...
    ├── texts.md                      # Animated Text, Gooey Text, Fade Text...
    ├── micro-interactions.md         # Gooey Switch, Elastic Slider...
    ├── components-carousels.md       # Parallax, Tilt, Cinematic...
    ├── components-navigation.md      # Bottom Sheet, Dialog, Tabs...
    ├── components-inputs.md          # Button, Picker, Switch...
    ├── display-loaders.md            # Circle Loader, Spinner Arc...
    ├── display-progress.md           # Progress, Shimmer, Rolling Counter...
    ├── display-content.md            # Avatar, Badge, Toast, QR Code...
    └── display-effects.md            # Glow, Ripple, Pagination...
```

### Component Coverage

| Category | Count | Highlights |
|----------|-------|-----------|
| Shaders | 8 | Aurora, Mesh Gradient, Skia Ripple, Siri Orb |
| Texts | 6 | Animated Text, Gooey Text, Staggered Text |
| Micro Interactions | 9 | Gooey Switch, Elastic Slider, Hamburger |
| Carousels | 13 | Parallax, Tilt, Cinematic, Vertical Flow |
| Navigation | 13 | Bottom Sheet, Dynamic Island, Dialog, Tabs |
| Inputs | 13 | Button, Picker, OTP Input, Switch, Theme Switch |
| Loaders | 6 | Circle Loader, Spinner Arc, Pulsing Dots |
| Progress | 5 | Circular Progress, Shimmer, Rolling Counter |
| Content | 10 | Avatar, Badge, Toast, Empty State, QR Code |
| Effects | 7 | Glow, Ripple, Stack Cards, Infinite Menu |
| **Total** | **90+** | |

### Design Principles

Built following [Anthropic's skill-creator guidelines](https://github.com/anthropics/skills):

- **Progressive Disclosure** — SKILL.md (199 lines) always loaded; references loaded only when needed
- **Concise** — Props tables + selective code examples for compound/hook patterns only
- **Context Efficient** — ~16K tokens total; display split into 4 files saves ~82% context per query

### Credits

- **Reacticx Library**: [@rit3zh](https://github.com/rit3zh) — https://www.reacticx.com
- **Skill Generation**: Claude Code Agent Teams (40+ agents across 6 phases)

---

## 한국어

### 이게 뭔가요?

AI 코딩 에이전트에게 [Reacticx](https://www.reacticx.com) React Native 컴포넌트 라이브러리의 완전한 지식을 부여하는 스킬입니다. 60fps 애니메이션을 지원하는 90개 이상의 프로덕션 레디 컴포넌트를 커버합니다.

### 빠른 시작

```bash
# npx skills로 설치 (권장)
npx skills add https://github.com/honeyhead/reacticx_skills --skill reacticx
```

자동 트리거를 위해 프로젝트 루트에 추가:

```markdown
<!-- CLAUDE.md 또는 .agents/instructions.md -->
이 프로젝트는 UI 컴포넌트로 Reacticx 라이브러리를 사용한다.
새로운 UI 컴포넌트가 필요할 때 항상 Reacticx를 우선 확인할 것.
```

### 수동 설치

```bash
# Claude Code
cp -r reacticx/ your-project/.claude/skills/reacticx/

# OpenCode / Codex / 기타 에이전트
cp -r reacticx/ your-project/.agents/skills/reacticx/
```

### 컴포넌트 커버리지

| 카테고리 | 개수 | 주요 컴포넌트 |
|---------|------|-------------|
| 셰이더 | 8 | Aurora, Mesh Gradient, Skia Ripple, Siri Orb |
| 텍스트 | 6 | Animated Text, Gooey Text, Staggered Text |
| 마이크로 인터랙션 | 9 | Gooey Switch, Elastic Slider, Hamburger |
| 캐러셀 | 13 | Parallax, Tilt, Cinematic, Vertical Flow |
| 네비게이션 | 13 | Bottom Sheet, Dynamic Island, Dialog, Tabs |
| 입력/컨트롤 | 13 | Button, Picker, OTP Input, Switch |
| 로더 | 6 | Circle Loader, Spinner Arc, Pulsing Dots |
| 프로그레스 | 5 | Circular Progress, Shimmer, Rolling Counter |
| 콘텐츠 | 10 | Avatar, Badge, Toast, Empty State, QR Code |
| 이펙트 | 7 | Glow, Ripple, Stack Cards, Infinite Menu |
| **합계** | **90+** | |

### 설계 원칙

[Anthropic skill-creator 가이드라인](https://github.com/anthropics/skills) 준수:

- **Progressive Disclosure** — SKILL.md(199줄)만 항상 로드, 레퍼런스는 필요시에만
- **간결함** — Props 테이블 + compound/hook 패턴에만 선별적 코드 예제
- **컨텍스트 효율** — 총 ~16K 토큰; display 4분할로 쿼리당 ~82% 컨텍스트 절감

---

## 日本語

### これは何ですか？

AIコーディングエージェントに[Reacticx](https://www.reacticx.com) React Nativeコンポーネントライブラリの完全な知識を付与するスキルです。60fpsアニメーション対応の90以上のプロダクションレディコンポーネントをカバーします。

### クイックスタート

```bash
# npx skillsでインストール（推奨）
npx skills add https://github.com/honeyhead/reacticx_skills --skill reacticx
```

自動トリガーのためにプロジェクトルートに追加：

```markdown
<!-- CLAUDE.md または .agents/instructions.md -->
このプロジェクトはUIコンポーネントにReacticxライブラリを使用する。
新しいUIコンポーネントが必要な場合、常にReacticxを優先的に確認すること。
```

### 手動インストール

```bash
# Claude Code
cp -r reacticx/ your-project/.claude/skills/reacticx/

# OpenCode / Codex / その他のエージェント
cp -r reacticx/ your-project/.agents/skills/reacticx/
```

### コンポーネントカバレッジ

| カテゴリ | 数 | 主要コンポーネント |
|---------|-----|-----------------|
| シェーダー | 8 | Aurora, Mesh Gradient, Skia Ripple, Siri Orb |
| テキスト | 6 | Animated Text, Gooey Text, Staggered Text |
| マイクロインタラクション | 9 | Gooey Switch, Elastic Slider, Hamburger |
| カルーセル | 13 | Parallax, Tilt, Cinematic, Vertical Flow |
| ナビゲーション | 13 | Bottom Sheet, Dynamic Island, Dialog, Tabs |
| 入力/コントロール | 13 | Button, Picker, OTP Input, Switch |
| ローダー | 6 | Circle Loader, Spinner Arc, Pulsing Dots |
| プログレス | 5 | Circular Progress, Shimmer, Rolling Counter |
| コンテンツ | 10 | Avatar, Badge, Toast, Empty State, QR Code |
| エフェクト | 7 | Glow, Ripple, Stack Cards, Infinite Menu |
| **合計** | **90+** | |

### 設計原則

[Anthropic skill-creatorガイドライン](https://github.com/anthropics/skills)準拠：

- **Progressive Disclosure** — SKILL.md（199行）のみ常時ロード、リファレンスは必要時のみ
- **簡潔さ** — Propsテーブル + compound/hookパターンのみ選択的コード例
- **コンテキスト効率** — 合計約16Kトークン; display 4分割でクエリ当たり約82%コンテキスト削減

---

<p align="center">
  <sub>Generated with Claude Code Agent Teams | Reacticx by <a href="https://github.com/rit3zh">@rit3zh</a></sub>
</p>
