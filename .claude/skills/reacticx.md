# Reacticx - React Native Component Library Reference

Use this skill when developing React Native apps with the Reacticx library. Reacticx provides 60+ production-ready animated components with smooth 60fps animations built on React Native Reanimated and Skia.

**Official docs:** https://www.reacticx.com/docs
**GitHub:** https://github.com/rit3zh/reacticx
**Package:** `reacticx` (CLI tool)

---

## Quick Setup

### 1. Install Required Utilities
```bash
npm install react-native-reanimated react-native-gesture-handler react-native-svg expo-haptics expo-blur expo-symbols @expo/vector-icons @shopify/react-native-skia
```

### 2. Initialize Config (optional, for CLI usage)
```bash
npx reacticx init
```
Creates `component.config.json`:
```json
{ "outDir": "src/shared/ui" }
```

### 3. Add Components
```bash
npx reacticx add <component-name>
npx reacticx add <component> --dir <path>
npx reacticx add <component> --overwrite
npx reacticx list
npx reacticx list -c <category>
```

---

## Component Categories & Quick Reference

### Shaders (GPU-accelerated visual effects)
| Component | Install Name | Description |
|-----------|-------------|-------------|
| Aurora | `aurora` | Skia-based animated aurora light waves |
| Chroma Ring | `chroma-ring` | Animated chromatic ring shader effect |
| Energy Orb | `energy-orb` | Glowing energy orb shader animation |
| Siri Orb | `siri-orb` | Siri-inspired orb animation with Skia |
| Mesh Gradient | `mesh-gradient` | Animated mesh gradient background |
| Grainy Gradient | `grainy-gradient` | Gradient with grain texture overlay |
| Skia Ripple | `skia-ripple` | Tap-driven Skia ripple effect |
| Wave Scrawler | `wave-scrawler` | Shader-based image wave transition |

### Texts (Animated typography)
| Component | Install Name | Description |
|-----------|-------------|-------------|
| Animated Text | `animated-text` | Per-character staggered animation with blur |
| Dynamic Text | `dynamic-text` | Cycles through text items with transitions |
| Fade Text | `fade-text` | Word-by-word fade-in with blur |
| Gooey Text | `gooey-text` | Morphing text with gooey blur (Skia) |
| Curved Marquee | `curved-marquee` | Text scrolling along curved SVG path |
| Staggered Text | `staggered-text` | Per-character Skia stagger animation |

### Micro Interactions
| Component | Install Name | Description |
|-----------|-------------|-------------|
| Animated Scroll Progress | `animated-scroll-progress` | Scroll tracker with floating action button |
| Animated Theme Toggle | `animated-theme-toggle` | SVG morphing sun/moon toggle |
| Animated Countdown | `countdown` | Per-character staggered countdown timer |
| Elastic Slider | `elastic-slider` | Elastic drag slider with spring physics |
| Flexi Button | `flexi-button` | Icon-to-text expanding button |
| Gooey Switch | `gooey-switch` | Skia blob toggle switch |
| Hamburger | `hamburger` | Morphing hamburger-to-X icon |
| Spin Button | `spin-button` | Loading state button with spinner |
| Stacked Chips | `stacked-chips` | Sideways-expanding chip menu |

### Components (UI building blocks)
| Component | Install Name | Description |
|-----------|-------------|-------------|
| Accordion | `accordion` | Expandable sections with haptic feedback |
| Animated Chip Group | `animated-chip` | Chip selector with expand animation |
| Animated Header ScrollView | `animated-header-scrollview` | iOS-style collapsing scroll header |
| Animated Input Bar | `animated-input-bar` | Rotating staggered placeholder input |
| Animated Masked Text | `animated-masked-text` | Shimmer wave masked text effect |
| Avatar | `avatar` | Flexible avatar with fallback initials |
| Avatar Group | `avatar-group` | Overlapping interactive avatar group |
| Badge | `badge` | Status/notification badge |
| Blur Carousel | `blur-carousel` | Horizontal blur-and-scale carousel |
| Button | `button` | Customizable press-animated button |
| Bottom Sheet | `bottom-sheet` | Draggable bottom sheet |
| Bottom Sheet Stack | `bottom-sheet-stack` | Stacked bottom sheets |
| CheckBox | `check-box` | Animated checkbox |
| Cinematic Carousel | `cinematic-carousel` | Cinematic-style carousel |
| Circle Loader | `circle-loader` | Circular loading animation |
| Circular Carousel | `circular-carousel` | Circular layout carousel |
| Circular List | `circular-list` | Circular scrolling list |
| Circular Loader | `circular-loader` | Circular loading indicator |
| Curved Bottom Tabs | `curved-bottom-tabs` | Curved tab bar navigation |
| Dialog | `dialog` | Animated dialog/modal |
| Disclosure Group | `disclosure-group` | Expandable disclosure sections |
| Dropdown | `dropdown` | Animated dropdown menu |
| Dynamic Island | `dynamic-island` | iOS Dynamic Island component |
| Empty State | `empty-state` | Composable empty state screen |
| Flip Card | `flip-card` | 3D flip card with blur |
| Glow | `glow` | Animated glow outline wrapper |
| Infinite Menu | `infinite-menu` | 3D radial menu with Skia |
| Lanyard | `lanyard` | Unstable lanyard component |
| Marquee | `marquee` | Auto-scrolling text marquee |
| Material Carousel | `material-carousel` | Material-inspired carousel |
| Matched Geometry | `matched-geometry` | Tap-to-expand layout transition |
| Morphing Tab Bar | `morphing-tabbar` | Fluid morphing tab navigation |
| Orbitdot Loader | `orbiting-dots` | Orbiting dots loading indicator |
| OTP Input | `otp-input` | Animated OTP input fields |
| Pagination | `pagination` | Draggable pagination dots |
| Parallax Carousel | `parallax-carousel` | Depth-based parallax carousel |
| Picker | `picker` | iOS-style 3D picker |
| Progress | `progress` | Animated progress bar |
| Circular Progress | `circular-progress` | Circular progress ring |
| Pulsing Loader | `pulsing-dots` | Pulsing dots loading indicator |
| QR Code | `qr-code` | Tap-to-expand QR code viewer |
| Radial Intro | `radial-intro` | Orbiting images animation |
| Ripple | `ripple` | Touchable ripple wrapper |
| Rolling Counter | `rolling-counter` | Spring-animated digit counter |
| Rotate Carousel | `rotate-carousel` | 3D rotating carousel |
| Rotating Square | `rotating-square` | Animated rotating square |
| Ruler | `ruler` | Interactive ruler control |
| Scale Carousel | `scale-carousel` | Scale-based carousel |
| Scrollable Search | `scrollable-search` | Search with scroll animation |
| Search Bar | `search-bar` | Animated search bar |
| Segmented Control | `segmented-control` | iOS-style segmented control |
| Seekbar | `seekbar` | Animated seek/progress bar |
| Shimmer | `shimmer` | Shimmer loading placeholder |
| Shimmer Wave Text | `shimmer-wave` | Shimmer wave text effect |
| Spinner Arc | `spinner-arc` | Arc-style loading spinner |
| Split View | `split-view` | Split view layout |
| Stack Aware Tabs | `stack-aware-tabs` | Stack-aware tab navigation |
| Stack Cards | `stack-cards` | Stacked card layout |
| Stepper | `stepper` | Animated stepper control |
| Switch | `switch` | Spring-animated toggle switch |
| Tabs | `tabs` | Animated tab component |
| Theme Switch | `theme-switch` | Skia-powered theme transition |
| Tilt Carousel | `tilt-carousel` | 3D tilt effect carousel |
| Title | `title` | Flexible heading component |
| Toast | `toast` | Global toast notification system |
| Vertical Flow Carousel | `vertical-flow-carousel` | Vertical snapping carousel |
| Vertical Page Carousel | `vertical-page-carousel` | Vertically paged carousel |

---

## Component Details

### Aurora
**Category:** Shaders | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
```bash
npx reacticx add aurora
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `width` | `number?` | Screen width | Component width |
| `height` | `number?` | 25% screen | Component height |
| `auroraColors` | `string[]?` | DEFAULT_AURORA_COLORS | Aurora color array |
| `skyColors` | `[string, string]?` | DEFAULT_SKY_COLORS | Sky gradient [top, bottom] |
| `speed` | `number?` | `0.5` | Animation speed |
| `intensity` | `number?` | `1` | Light wave intensity |
| `waveDirection` | `[number, number]?` | `[9, -9]` | Wave direction vectors |
```tsx
import Aurora from "@/components/molecules/aurora";
<View style={{ flex: 1 }}><Aurora /></View>
```

---

### Chroma Ring
**Category:** Shaders | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
```bash
npx reacticx add chroma-ring
```
Animated chromatic ring shader effect with customizable colors and animation speed.

---

### Energy Orb
**Category:** Shaders | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
```bash
npx reacticx add energy-orb
```
Glowing energy orb with shader-based rendering and customizable glow parameters.

---

### Siri Orb
**Category:** Shaders | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
```bash
npx reacticx add siri-orb
```
Siri-inspired orb animation using Skia shaders with fluid motion effects.

---

### Mesh Gradient
**Category:** Shaders | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
```bash
npx reacticx add mesh-gradient
```
Animated mesh gradient background with customizable control points and colors.

---

### Grainy Gradient
**Category:** Shaders | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
```bash
npx reacticx add grainy-gradient
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `width` | `number?` | Screen width | Canvas width |
| `height` | `number?` | Screen height | Canvas height |
| `colors` | `string[]?` | `["#5b0bb5","#7c3aed","#fb923c","#db2777"]` | Gradient colors (up to 5) |
| `speed` | `number?` | `2.9` | Animation speed |
| `animated` | `boolean?` | `true` | Enable animation |
| `intensity` | `number?` | `0.112` | Grain intensity |
| `size` | `number?` | `1.9` | Grain particle size |
| `amplitude` | `number?` | `0.1` | Wave amplitude |
| `brightness` | `number?` | `0` | Brightness adjustment |
```tsx
import { GrainyGradient } from "@/components/organisms/grainy-gradient";
<View style={{ flex: 1 }}><GrainyGradient /></View>
```

---

### Skia Ripple
**Category:** Shaders | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`, `react-native-gesture-handler`
```bash
npx reacticx add skia-ripple
```
Exports: `SkiaRippleEffect`, `RippleImage`, `RippleRect`

**Shared Props:**
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `width` | `number` | Required | Container width |
| `height` | `number` | Required | Container height |
| `amplitude` | `number` | `12` | Wave intensity |
| `frequency` | `number` | `15` | Wave density |
| `decay` | `number` | `8` | Dampening effect |
| `speed` | `number` | `1200` | Animation duration ms |
| `borderRadius` | `number` | `0` | Corner radius |

**RippleImage** adds: `source` (string, image URL), `fit` ("cover"|"contain"|"fill"|"none"|"scaleDown")
**RippleRect** adds: `color` (string), `children` (ReactNode)

```tsx
import { RippleImage } from "@/components/organisms/skia-ripple";
<GestureHandlerRootView>
  <RippleImage width={350} height={420} borderRadius={28} source="https://..." />
</GestureHandlerRootView>
```

---

### Wave Scrawler
**Category:** Shaders | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`, `react-native-worklets`
```bash
npx reacticx add wave-scrawler
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `source` | `array` | Required | Image URI array |
| `index` | `number` | Required | Active image index |
| `duration` | `number` | `1000` | Transition duration ms |
| `amplitude` | `number` | `0.108` | Wave height |
| `colorSeparation` | `number` | `0.095` | RGB separation effect |
| `onTransitionEnd` | `function` | Optional | Transition callback |

---

### Animated Text
**Category:** Texts | **Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add animated-text
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `text` | `string` | Required | Text to animate |
| `style` | `any` | undefined | Text styling |
| `animationConfig` | `object` | defaults | Spring config, characterDelay (15), maxBlurIntensity (12) |
| `enterFrom` | `object` | defaults | Entry state: opacity, translateY, scale, rotate |
| `enterTo` | `object` | defaults | Entry end state |
| `exitFrom` | `object` | defaults | Exit start state |
| `exitTo` | `object` | defaults | Exit end state |
```tsx
import AnimatedText from "@/components/organisms/animated-text";
<AnimatedText
  text="Hello World"
  animationConfig={{ spring: { damping: 15, stiffness: 210, mass: 1 }, characterDelay: 15 }}
  enterFrom={{ opacity: 0, translateY: 55, scale: 0.2 }}
  style={{ color: "#fff", fontSize: 40 }}
/>
```

---

### Dynamic Text
**Category:** Texts | **Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add dynamic-text
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `items` | `DynamicTextItem[]` | Required | Text items to cycle through |
| `loop` | `boolean` | `false` | Enable looping |
| `loopCount` | `number` | `-1` | Loop count (-1 = infinite) |
| `animationPreset` | `"fade"|"zoom"|"custom"` | `"fade"` | Animation style |
| `animationDirection` | `"up"|"down"` | `"up"` | Direction |
| `timing` | `object` | DEFAULT_TIMING | Duration and interval |
| `text` | `object` | DEFAULT_TEXT | Font config |
| `paused` | `boolean` | `false` | Pause animation |
| `onIndexChange` | `function` | undefined | Index change callback |
```tsx
import { DynamicText } from "@/components/molecules/dynamic-text";
<DynamicText items={[{ text: "Hello" }, { text: "World" }]} loop dot={{ size: 5 }} />
```

---

### Fade Text
**Category:** Texts | **Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add fade-text
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `inputs` | `array` | Required | Text content array |
| `wordDelay` | `number` | `300` | Delay between words ms |
| `duration` | `number` | `800` | Animation duration |
| `fontSize` | `number` | `32` | Text size |
| `color` | `string` | `"#ffffff"` | Text color |
| `blurIntensity` | `[number,number,number]` | defaults | Blur levels |
```tsx
import { FadeText } from "@/components/organisms/fade-text";
<FadeText inputs={["Hello World!", "Reacticx rocks!"]} duration={3500} wordDelay={300} />
```

---

### Gooey Text
**Category:** Texts | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
```bash
npx reacticx add gooey-text
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `texts` | `string[]` | Required | Text strings to morph between |
| `morphTime` | `number` | `1` | Morph duration (seconds) |
| `cooldownTime` | `number` | `0.25` | Pause between morphs |
| `fontSize` | `number` | `48` | Text size |
| `color` | `string` | `"black"` | Text color |
| `fontSource` | `number|string` | `null` | Custom font file |
| `width` | `number` | `300` | Container width |
| `height` | `number` | `100` | Container height |
```tsx
import GooeyText from "@/components/molecules/gooey-text";
<GooeyText texts={["REACTICX", "IS", "AWESOME!"]} color="white" fontSize={50} />
```

---

### Curved Marquee
**Category:** Texts | **Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add curved-marquee
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `text` | `string` | `"⟣ REACTICX ⟢"` | Text content |
| `speed` | `number` | `500` | Scroll speed |
| `curve` | `number` | `-500` | Curve intensity |
| `direction` | `"right"|"left"` | `"left"` | Scroll direction |
| `textColor` | `string` | `"#ffffff"` | Text color |
| `fontSize` | `number` | `100` | Font size |
| `copies` | `number` | `50` | Text repetitions |
```tsx
import { CurvedMarquee } from "@/components/organisms/curved-marquee";
<CurvedMarquee text="Hello World" speed={500} curve={-500} />
```

---

### Staggered Text
**Category:** Texts | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
```bash
npx reacticx add staggered-text
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `texts` | `string[]` | Required | Text strings to cycle |
| `activeIndex` | `number` | `0` | Current text index |
| `fontSize` | `number` | `24` | Character size |
| `color` | `string` | `"#ffffff"` | Text color |
| `staggerFrom` | `"leading"|"trailing"|"random"|"edges"|"center"` | `"leading"` | Stagger direction |
| `letterSpacing` | `number` | `1` | Character spacing |
```tsx
import { StaggeredText } from "@/components/organisms/staggered-text";
<StaggeredText texts={["Hello", "World"]} activeIndex={0} fontSize={35} color="#fff" />
```

---

### Animated Scroll Progress
**Category:** Micro Interactions | **Deps:** `react-native-reanimated`, `react-native-worklets`
```bash
npx reacticx add animated-scroll-progress
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Scrollable content |
| `renderInitialContent` | `function` | Required | Initial FAB renderer |
| `renderEndContent` | `function` | Required | End-state FAB renderer |
| `endReachedThreshold` | `number` | `100` | Progress % for end state |
| `fabWidth` | `number` | Required | FAB width |
| `fabHeight` | `number` | `50` | FAB height |
| `fabBottomOffset` | `number` | `30` | Distance from bottom |
| `fabBackgroundColor` | `string` | Required | Initial bg color |
| `fabEndBackgroundColor` | `string` | Required | End bg color |
| `fabBorderRadius` | `number` | `100` | Corner radius |

---

### Animated Theme Toggle
**Category:** Micro Interactions | **Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add animated-theme-toggle
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `isDark` | `boolean` | Required | Current theme state |
| `onToggle` | `function` | Required | Toggle callback |
| `size` | `number` | `100` | Icon size |
| `color` | `string` | `"#000"` | Icon color |
| `strokeWidth` | `number` | `1.5` | SVG stroke width |
| `moonScale` | `number` | `0.65` | Moon scale factor |
```tsx
import { AnimatedThemeToggle } from "@/components/micro-interactions/animated-theme-toggle";
<AnimatedThemeToggle isDark={isDark} onToggle={() => setIsDark(!isDark)} size={98} />
```

---

### Animated Countdown
**Category:** Micro Interactions | **Deps:** `react-native-reanimated`
```bash
npx reacticx add countdown
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `targetDate` | `Date` | Required | Countdown target |
| `size` | `"xlarge"|"large"|"medium"|"small"` | `"medium"` | Size preset |
| `customization.numberColor` | `string` | `"#ffffff"` | Number color |
| `customization.labelColor` | `string` | `"#666666"` | Label color |
| `customization.showLabels` | `boolean` | `true` | Show time labels |
| `customization.showDays` | `boolean` | `true` | Show days |
| `customization.onFinish` | `function` | undefined | Completion callback |
```tsx
import { CountdownTimer } from "@/components/micro-interactions/countdown";
<CountdownTimer targetDate={new Date("2026-12-31")} customization={{ numberColor: "#fff" }} />
```

---

### Elastic Slider
**Category:** Micro Interactions | **Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`
```bash
npx reacticx add elastic-slider
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `defaultValue` | `number` | `50` | Initial value |
| `startingValue` | `number` | `0` | Min value |
| `maxValue` | `number` | `100` | Max value |
| `isStepped` | `boolean` | `false` | Step mode |
| `onValueChange` | `function` | undefined | Value callback |
| `trackColor` | `string` | `"#9CA3AF"` | Track color |
| `fillColor` | `string` | `"#6B7280"` | Fill color |
| `renderLeadingAccessory` | `function` | undefined | Leading icon |
| `renderTrailingAccessory` | `function` | undefined | Trailing icon |

---

### Flexi Button
**Category:** Micro Interactions | **Deps:** `react-native-reanimated`, `expo-blur`, `@expo/vector-icons`
```bash
npx reacticx add flexi-button
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `onPress` | `function` | undefined | Press callback |
| `collapsedWidth` | `number` | `40` | Collapsed width |
| `expandedWidth` | `number` | `120` | Expanded width |
| `text` | `string` | `"Clear All"` | Expanded text |
| `icon` | `string|function` | `"notifications"` | Icon name or renderer |
| `backgroundColor` | `string` | `"rgba(255,255,255,0.1)"` | Background color |

---

### Gooey Switch
**Category:** Micro Interactions | **Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `@shopify/react-native-skia`, `react-native-worklets`, `@expo/vector-icons`, `expo-symbols`
```bash
npx reacticx add gooey-switch
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `active` | `boolean?` | -- | Controlled state |
| `onToggle` | `function?` | -- | Toggle callback |
| `size` | `number?` | DEFAULT_SIZE | Component size |
| `activeColor` | `string?` | DEFAULT_ON_COLOR | On color |
| `inactiveColor` | `string?` | DEFAULT_OFF_COLOR | Off color |
| `trackColor` | `string?` | DEFAULT_BLOB_COLOR | Blob color |
| `gooey` | `number?` | `35` | Gooey intensity |
| `isDisabled` | `boolean?` | `false` | Disable toggle |
```tsx
import GooeySwitch from '@/components/micro-interactions/gooey-switch';
<GooeySwitch activeColor="#8093ff" size={200} trackColor="#1a1a1a" gooey={35} />
```

---

### Hamburger
**Category:** Micro Interactions | **Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add hamburger
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `progress` | `SharedValue<number>` | Required | 0=hamburger, 1=X |
| `size` | `number` | `54` | Icon size |
| `color` | `string` | `"black"` | Line color |
| `strokeWidth` | `number` | `size*0.04` | Line thickness |
| `onPress` | `function` | -- | Press callback |
```tsx
import Hamburger from "@/components/micro-interactions/hamburger";
const progress = useSharedValue(0);
<Hamburger progress={progress} color="#fff" size={90}
  onPress={() => { progress.value = withTiming(progress.value === 1 ? 0 : 1); }} />
```

---

### Spin Button
**Category:** Micro Interactions | **Deps:** `react-native-reanimated`
```bash
npx reacticx add spin-button
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `idleText` | `string` | `"Save"` | Idle state text |
| `activeText` | `string` | `"Saving"` | Loading text |
| `colors` | `object` | defaults | Color config for states |
| `onPress` | `function` | -- | Press callback |
| `disabled` | `boolean` | `false` | Disable button |
| `controlled` | `boolean` | `false` | Controlled mode |
| `isActive` | `boolean` | -- | Active state (controlled) |

---

### Stacked Chips
**Category:** Micro Interactions | **Deps:** `react-native-reanimated`, `expo-haptics`, `expo-blur`
```bash
npx reacticx add stacked-chips
```
Compound component: `StackedChips`, `StackedChips.Trigger`, `StackedChips.Content`
```tsx
<StackedChips>
  <StackedChips.Trigger><Text>Create</Text></StackedChips.Trigger>
  <StackedChips.Content><Text>Document</Text></StackedChips.Content>
</StackedChips>
```

---

### Accordion
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-haptics`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add accordion
```
Compound: `Accordion`, `Accordion.Item`, `Accordion.Trigger`, `Accordion.Content`

| Prop (Accordion) | Type | Default | Description |
|------|------|---------|-------------|
| `type` | `"single"|"multiple"` | `"single"` | Expansion mode |
| `theme` | `AccordionTheme` | light | Theme config |
| `spacing` | `number` | `0` | Gap between items |

| Prop (Accordion.Item) | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `string` | Required | Unique ID |
| `pop` | `boolean` | `false` | Scale animation |
| `icon` | `"cross"|"chevron"` | `"chevron"` | Icon style |
```tsx
<Accordion type="single" spacing={8}>
  <Accordion.Item value="1" icon="chevron">
    <Accordion.Trigger><Text>Question</Text></Accordion.Trigger>
    <Accordion.Content><Text>Answer</Text></Accordion.Content>
  </Accordion.Item>
</Accordion>
```

---

### Animated Chip Group
**Category:** Components | **Deps:** `react-native-reanimated`
```bash
npx reacticx add animated-chip
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `chips` | `ChipItem[]` | Required | Chip items |
| `selectedIndex` | `number` | Optional | Selected index |
| `onChange` | `function` | Optional | Selection callback |

ChipItem: `{ label, icon, activeColor, labelColor, inActiveBackgroundColor }`

---

### Animated Header ScrollView
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-linear-gradient`, `@react-native-masked-view/masked-view`, `expo-blur`, `react-native-safe-area-context`, `react-native-easing-gradient`
```bash
npx reacticx add animated-header-scrollview
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `largeTitle` | `string` | Required | Large heading text |
| `subtitle` | `string` | Optional | Secondary text |
| `children` | `ReactNode` | Required | Scroll content |
| `rightComponent` | `ReactNode` | Optional | Header right element |
| `largeHeaderTitleStyle` | `any` | `{fontSize:40}` | Large title style |
```tsx
<AnimatedHeaderScrollView largeTitle="Today" subtitle="Wednesday, Jan 22">
  <Text>Content here</Text>
</AnimatedHeaderScrollView>
```

---

### Animated Input Bar
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add animated-input-bar
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `placeholders` | `string[]` | Required | Placeholder texts to cycle |
| `animationInterval` | `number` | `3000` | Cycle interval ms |
| `value` | `string` | Optional | Input value |
| `onChangeText` | `function` | Optional | Text change callback |
| `characterDelayIncrement` | `number` | `30` | Character stagger ms |

---

### Animated Masked Text
**Category:** Components | **Deps:** `expo-linear-gradient`, `@react-native-masked-view/masked-view`
```bash
npx reacticx add animated-masked-text
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `string` | Required | Text content |
| `speed` | `number` | `1` | Animation speed |
| `colors` | `array` | shimmer gradient | Gradient colors |
| `baseTextColor` | `string` | `"#000000"` | Base text color |
```tsx
<AnimatedMaskedText style={{ fontSize: 84, fontWeight: "100" }} baseTextColor="#2a2a2a">
  Reacticx
</AnimatedMaskedText>
```

---

### Avatar
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-worklets`
```bash
npx reacticx add avatar
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `image` | `{ uri: string, name?: string }` | Required | Image source |
| `size` | `number` | `40` | Avatar size |
| `showBorder` | `boolean` | `true` | Show border |
| `loading` | `boolean` | `false` | Shimmer loading |
| `showOnlineIndicator` | `boolean` | `false` | Status dot |
| `showText` | `boolean` | `false` | Show name text |
| `textPosition` | `"bottom"|"right"|"top"` | `"bottom"` | Name position |
```tsx
<Avatar image={{ uri: "https://...", name: "John" }} size={48} showOnlineIndicator />
```

---

### Avatar Group
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`, `expo-haptics`
```bash
npx reacticx add avatar-group
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `avatars` | `AvatarItem[]` | Required | `{ id, uri?, name? }` array |
| `size` | `number` | `40` | Avatar diameter |
| `max` | `number` | `5` | Max visible |
| `overlap` | `number` | `10` | Overlap distance |
| `onPress` | `function` | Optional | Press callback (receives id) |

---

### Badge
**Category:** Components | **Deps:** none (core RN only)
```bash
npx reacticx add badge
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `label` | `string` | Required | Badge text |
| `variant` | `"pending"|"notifications"|"error"|"warning"|"success"|"default"` | `"default"` | Style variant |
| `size` | `"lg"|"md"|"sm"` | `"md"` | Size |
| `icon` | `ReactNode` | -- | Optional icon |

---

### Blur Carousel
**Category:** Components | **Deps:** `react-native-reanimated`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add blur-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Carousel items |
| `renderItem` | `function` | Required | Item renderer |
| `spacing` | `number` | `20` | Item spacing |
| `itemWidth` | `number` | `SCREEN_WIDTH * 0.75` | Item width |

---

### Button
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-worklets`, `expo-linear-gradient`
```bash
npx reacticx add button
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Content |
| `isLoading` | `boolean` | false | Loading state |
| `onPress` | `function` | -- | Press handler |
| `width` | `number` | `200` | Width |
| `height` | `number` | `48` | Height |
| `backgroundColor` | `string` | `"#fff"` | Bg color |
| `gradientColors` | `array` | -- | Gradient colors |
| `withPressAnimation` | `boolean` | `true` | Scale on press |
| `animationDuration` | `number` | `250` | Animation ms |
| `disabled` | `boolean` | false | Disabled state |
| `showLoadingIndicator` | `boolean` | false | Show spinner |

---

### Bottom Sheet
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`
```bash
npx reacticx add bottom-sheet
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Sheet content |
| `snapPoints` | `array` | Required | Snap position values |
| `enableBackdrop` | `boolean` | `true` | Show overlay |
| `backdropOpacity` | `number` | `0.5` | Backdrop transparency |
| `dismissOnBackdropPress` | `boolean` | `true` | Close on backdrop tap |
| `dismissOnSwipeDown` | `boolean` | `true` | Close on swipe down |
| `onClose` | `function` | -- | Close callback |
| `showHandle` | `boolean` | `true` | Show drag handle |
| `backgroundColor` | `string` | `"#FFFFFF"` | Sheet bg color |
| `borderRadius` | `number` | `24` | Corner radius |
| `enableDynamicSizing` | `boolean` | `false` | Dynamic height |

**Methods (ref):** `snapToIndex(i)`, `expand()`, `collapse()`, `close()`, `getCurrentIndex()`
```tsx
const sheetRef = useRef<BottomSheetMethods>(null);
<BottomSheet ref={sheetRef} snapPoints={["50%","90%"]} backgroundColor="#1c1c1e" borderRadius={28}>
  <View style={{ padding: 20 }}><Text>Content</Text></View>
</BottomSheet>
```

---

### Bottom Sheet Stack
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-gesture-handler`
```bash
npx reacticx add bottom-sheet-stack
```
Wrap app with `<BottomSheetStackProvider>`. Use hooks:
- `useBottomSheet()` returns `{ present(component), dismiss() }`
- `useBottomSheetStack()` returns `{ pushSheet(config), popSheet(id?), popToRoot(), getStackDepth() }`
```tsx
const { present } = useBottomSheet();
present(<BottomSheet snapPoints={['50%']}><Text>Content</Text></BottomSheet>);
```

---

### CheckBox
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add check-box
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `checked` | `boolean` | `false` | Checkbox state |
| `checkmarkColor` | `string` | -- | Checkmark color |
| `stroke` | `number` | `1.5` | Stroke width |
| `size` | `number` | -- | Checkbox size |
```tsx
<CheckBox checked={checked} checkmarkColor="#fff" stroke={5.5} size={60} />
```

---

### Cinematic Carousel
**Category:** Components | **Deps:** `react-native-reanimated`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add cinematic-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Carousel items |
| `renderItem` | `function` | Required | Item renderer |
| `spacing` | `number` | `20` | Item spacing |
| `itemWidth` | `number` | `SCREEN_WIDTH*0.75` | Item width |

3D perspective transforms with dynamic blur and scale/opacity effects.

---

### Circle Loader
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add circle-loader
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `dotColor` | `string` | `"#007AFF"` | Dot color |
| `dotRadius` | `number` | `6` | Dot radius |
| `dotSpacing` | `number` | `20` | Dot spacing |
| `duration` | `number` | `950` | Animation ms |
```tsx
<CircleLoadingIndicator dotColor="#fff" duration={500} dotSpacing={8} />
```

---

### Circular Carousel
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-blur`, `react-native-worklets`
```bash
npx reacticx add circular-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Carousel items |
| `renderItem` | `function` | Required | Item renderer |
| `spacing` | `number` | `20` | Item spacing |
| `itemWidth` | `number` | `SCREEN_WIDTH*0.75` | Item width |
| `onIndexChange` | `function` | Optional | Index callback |

Cards rotate, scale, and blur in circular style.

---

### Circular List
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-worklets`, `expo-blur`, `expo-haptics`
```bash
npx reacticx add circular-list
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `string[]` | Required | Image URI array |
| `scaleEnabled` | `boolean` | `false` | Enable scale animation |
```tsx
<CircularList data={["https://...","https://..."]} scaleEnabled={true} />
```

---

### Circular Loader
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add circular-loader
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `size` | `number` | `40` | Loader diameter |
| `strokeWidth` | `number` | `4` | Stroke width |
| `activeColor` | `string` | `"#000000"` | Arc color |
| `duration` | `number` | `1000` | Animation ms |
| `enableBlur` | `boolean` | `false` | Motion blur |
| `gradientLength` | `number` | `20` | Gradient fade % |
```tsx
<CircularLoader activeColor="#fff" gradientLength={50} enableBlur />
```

---

### Curved Bottom Tabs
**Category:** Components | **Deps:** `react-native-reanimated`, `@react-navigation/bottom-tabs`, `react-native-svg`
```bash
npx reacticx add curved-bottom-tabs
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `tabs` | `Tab[]` | Required | `{ id, title, icon, badge? }` array |
| `currentIndex` | `number` | Required | Active tab |
| `onPress` | `function` | Required | Tab select callback |
| `gradient` | `[string,string]` | `["#121212","#1A1A1A"]` | Background gradient |
| `activeColor` | `string` | `"#ffffff"` | Active icon color |
| `inactiveColor` | `string` | `"#cccccc"` | Inactive icon color |
| `hideWhenKeyboardShown` | `boolean` | `false` | Auto-hide on keyboard |

Integrates with Expo Router's `Tabs` navigator. Requires `GestureHandlerRootView`.

---

### Dialog
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-blur`, `react-native-worklets`
```bash
npx reacticx add dialog
```
Compound: `Dialog`, `Dialog.Trigger`, `Dialog.Backdrop`, `Dialog.Content`, `Dialog.Close`

| Prop (Backdrop) | Type | Default | Description |
|------|------|---------|-------------|
| `blurAmount` | `number` | `20` | Blur intensity |
| `backgroundColor` | `string` | `"rgba(0,0,0,0.5)"` | Overlay color |

Open: 550ms, Close: 650ms. Tapping outside dismisses.
```tsx
<Dialog>
  <Dialog.Trigger><Pressable><Text>Open</Text></Pressable></Dialog.Trigger>
  <Dialog.Backdrop blurAmount={25} />
  <Dialog.Content>
    <Text>Modal Content</Text>
    <Dialog.Close asChild><Pressable><Text>Close</Text></Pressable></Dialog.Close>
  </Dialog.Content>
</Dialog>
```

---

### Dropdown
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`, `expo-haptics`
```bash
npx reacticx add dropdown
```
Compound: `Dropdown`, `Dropdown.Trigger`, `Dropdown.Content`, `Dropdown.Item`

| Prop (Content) | Type | Default | Description |
|------|------|---------|-------------|
| `position` | `"auto"|"top"|"bottom"|"left"|"right"` | `"auto"` | Menu position |
```tsx
<Dropdown>
  <Dropdown.Trigger><Text>Menu</Text></Dropdown.Trigger>
  <Dropdown.Content>
    <Dropdown.Item onPress={() => {}}><Text>Edit</Text></Dropdown.Item>
    <Dropdown.Item onPress={() => {}}><Text>Delete</Text></Dropdown.Item>
  </Dropdown.Content>
</Dropdown>
```

---

### Disclosure Group
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add disclosure-group
```
Compound: `DisclosureGroup`, `DisclosureGroup.Trigger`, `DisclosureGroup.Items`, `DisclosureGroup.Item`

| Prop (Trigger) | Type | Default | Description |
|------|------|---------|-------------|
| `showChevron` | `boolean` | `true` | Show chevron |
| `chevronColor` | `string` | `"#ffffff"` | Chevron color |

| Prop (Items) | Type | Default | Description |
|------|------|---------|-------------|
| `maxHeight` | `number` | `400` | Max scrollable height |
| `scrollable` | `boolean` | `true` | Enable scroll |
| `useBlur` | `boolean` | `false` | Blur overlay |
```tsx
<DisclosureGroup>
  <DisclosureGroup.Trigger><Text>Options</Text></DisclosureGroup.Trigger>
  <DisclosureGroup.Items>
    <DisclosureGroup.Item onPress={() => {}}><Text>Edit</Text></DisclosureGroup.Item>
  </DisclosureGroup.Items>
</DisclosureGroup>
```

---

### Dropdown
**Category:** Components
```bash
npx reacticx add dropdown
```
Animated dropdown menu with customizable options.

---

### Dynamic Island
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-blur`, `expo-haptics`
```bash
npx reacticx add dynamic-island
```
Compound: `DynamicIsland.Provider`, `DynamicIsland.Trigger`, `DynamicIsland.Content`

| Prop (Provider) | Type | Default | Description |
|------|------|---------|-------------|
| `config` | `object` | -- | collapsedWidth/Height, expandedWidth/Height |
| `haptics` | `boolean` | `true` | Haptic feedback |
| `onExpand` | `function` | -- | Expand callback |
| `onCollapse` | `function` | -- | Collapse callback |

Hook: `useDynamicIsland()` returns `{ isExpanded, expand, collapse, toggle }`
```tsx
<DynamicIsland.Provider>
  <DynamicIsland.Trigger><Text>Tap</Text></DynamicIsland.Trigger>
  <DynamicIsland.Content><Text>Expanded!</Text></DynamicIsland.Content>
</DynamicIsland.Provider>
```

---

### Empty State
**Category:** Components
```bash
npx reacticx add empty-state
```
Compound: `Empty`, `EmptyHeader`, `EmptyMedia`, `EmptyTitle`, `EmptyDescription`, `EmptyContent`, `EmptyButton`
```tsx
<Empty>
  <EmptyHeader>
    <EmptyMedia variant="icon"><Icon /></EmptyMedia>
    <EmptyTitle>No Messages</EmptyTitle>
    <EmptyDescription>Start a conversation</EmptyDescription>
  </EmptyHeader>
  <EmptyContent>
    <EmptyButton onPress={() => {}}>New Message</EmptyButton>
  </EmptyContent>
</Empty>
```

---

### Flip Card
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-haptics`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add flip-card
```
Compound: `FlipCard`, `FlipCard.Front`, `FlipCard.Back`, `FlipCard.Trigger`

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `width` | `number` | `340` | Card width |
| `height` | `number` | `480` | Card height |
| `borderRadius` | `number` | `24` | Corner radius |
| `animationDuration` | `number` | `600` | Flip duration ms |
| `enableHaptics` | `boolean` | `true` | Haptic feedback |
| `scaleOnPress` | `boolean` | `true` | Scale on press |

---

### Glow
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add glow
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Content to wrap |
| `size` | `number` | `4` | Border thickness |
| `color` | `string` | `"#8b5cf6"` | Primary glow color |
| `secondaryColor` | `string` | `"#ec4899"` | Secondary color |
| `duration` | `number` | `3000` | Animation cycle ms |
| `style` | `"pulse"|"wave"|"breathe"|"snap"|"spinner"|"linear"|"withoutEasing"` | `"pulse"` | Animation style |
| `intensity` | `number` | `1` | Opacity multiplier |
| `enabled` | `boolean` | `true` | Toggle glow |
```tsx
<Glow size={2} style="pulse" color="#8b5cf6" secondaryColor="#ec4899">
  <View style={{ width: 280, height: 56, backgroundColor: "#151515", borderRadius: 28 }}>
    <Text>Glowing Button</Text>
  </View>
</Glow>
```

---

### Infinite Menu
**Category:** Components | **Deps:** `@shopify/react-native-skia`, `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`
```bash
npx reacticx add infinite-menu
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `items` | `{ image: string }[]` | Required | Menu items |
| `scale` | `number` | `1` | Sphere scale |
| `backgroundColor` | `string` | `"#000000"` | Background color |

---

### Lanyard
**Category:** Components
```bash
npx reacticx add lanyard
```
Unstable lanyard component (experimental).

---

### Marquee
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-gesture-handler`
```bash
npx reacticx add marquee
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Content to scroll |
| `speed` | `number` | `50` | Scroll speed |
| `spacing` | `number` | `0` | Content gap |
| `pauseOnPress` | `boolean` | `false` | Pause on touch |
| `direction` | `"ltr"|"rtl"` | `"ltr"` | Scroll direction |
```tsx
<Marquee speed={50} spacing={20}><Text>Reacticx</Text></Marquee>
```

---

### Material Carousel
**Category:** Components | **Deps:** `react-native-reanimated`
```bash
npx reacticx add material-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `string[]` | Required | Image URI array |
| `renderItem` | `function` | Optional | Custom renderer |

---

### Matched Geometry
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `expo-blur`, `react-native-worklets`
```bash
npx reacticx add matched-geometry
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `id` | `string` | Required | Unique transition ID |
| `children` | `ReactNode` | Required | Content |
| `onPress` | `function` | Optional | Press callback |

Requires `GestureHandlerRootView` wrapper. Drag ~300px triggers dismissal.

---

### Morphing Tab Bar
**Category:** Components | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`, `expo-haptics`
```bash
npx reacticx add morphing-tabbar
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `items` | `{ keyPath: string, name: string }[]` | DEFAULT | Tab items |
| `onTabChange` | `function` | Optional | Tab change callback |
| `initialActiveIndex` | `number` | `0` | Starting tab |
| `animationDuration` | `number` | `300` | Morph duration |
| `borderRadius` | `number` | `12` | Container radius |
| `enableGlass` | `boolean` | `false` | Glassmorphism effect |
```tsx
<MorphicTabBar
  items={[{ keyPath: '/home', name: 'Home' }, { keyPath: '/search', name: 'Search' }]}
  onTabChange={(keyPath, index) => console.log(keyPath)}
/>
```

---

### Orbitdot Loader
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add orbiting-dots
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `dotColor` | `string` | `"#fff"` | Dot color |
| `dotRadius` | `number` | `4` | Dot radius |
| `centerRadius` | `number` | `5` | Center circle radius |
| `size` | `number` | `40` | Component size |
| `duration` | `number` | `900` | Animation duration |
| `numDots` | `number` | `4` | Number of dots |

---

### OTP Input
**Category:** Components | **Deps:** `react-native-reanimated`
```bash
npx reacticx add otp-input
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `otpCount` | `number` | `6` | Number of fields (4-6) |
| `error` | `boolean` | `false` | Error state (shake) |
| `errorMessage` | `string` | `"Invalid OTP..."` | Error text |
| `onInputChange` | `function` | -- | Input callback |
| `onInputFinished` | `function` | -- | Completion callback |
| `inputWidth` | `number` | `60` | Field width |
| `inputHeight` | `number` | `60` | Field height |
| `animationVariant` | `string` | `"fadeSlideDown"` | Entry animation |
```tsx
<OtpInput otpCount={4} error={error} onInputFinished={(code) => verify(code)} />
```

---

### Pagination
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-worklets`, `expo-haptics`, `react-native-gesture-handler`
```bash
npx reacticx add pagination
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `activeIndex` | `number` | Required | Current page |
| `totalItems` | `number` | Required | Total pages |
| `activeColor` | `string` | `"#c4c4c4"` | Active dot color |
| `inactiveColor` | `string` | `"#363636"` | Inactive color |
| `dotSize` | `number` | `10` | Dot diameter |
| `onIndexChange` | `function` | Optional | Index callback |

---

### Parallax Carousel
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-haptics`, `react-native-worklets`
```bash
npx reacticx add parallax-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Items with `image.uri` |
| `renderItem` | `function` | Required | Item renderer |
| `parallaxIntensity` | `number` | `0.7` | Parallax effect |
| `itemWidth` | `number` | screen width | Item width |
| `pagingEnabled` | `boolean` | `true` | Snap paging |

---

### Picker
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-worklets`, `expo-blur`, `react-native-gesture-handler`, `expo-linear-gradient`, `expo-haptics`
```bash
npx reacticx add picker
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `items` | `array` | Required | Selectable items |
| `onItemChange` | `function` | Optional | Selection callback |
| `initialIndex` | `number` | `0` | Starting index |
| `itemHeight` | `number` | `44` | Item height |
| `fontSize` | `number` | `20` | Text size |
| `hapticFeedback` | `boolean` | `true` | Enable haptics |
```tsx
<Picker items={["Day","Afternoon","Evening","Night"]} onItemChange={(item) => setSelected(item)} />
```

---

### Progress
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-linear-gradient`
```bash
npx reacticx add progress
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `progress` | `number` | `0` | Value 0-1 |
| `height` | `number` | `10` | Bar height |
| `progressColor` | `string` | `"#2089dc"` | Fill color |
| `trackColor` | `string` | `"#e0e0e0"` | Track color |
| `showPercentage` | `boolean` | `false` | Show % text |
| `indeterminate` | `boolean` | `false` | Loading mode |
| `useGradient` | `boolean` | `false` | Gradient fill |
| `pulsate` | `boolean` | `false` | Pulse animation |

---

### Circular Progress
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add circular-progress
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `progress` | `SharedValue<number>` | Required | Progress 0-100 |
| `size` | `number` | `50` | Component size |
| `strokeWidth` | `number` | `3` | Ring thickness |
| `progressCircleColor` | `string` | `"white"` | Progress color |
| `renderIcon` | `function` | Optional | Center icon |

---

### Pulsing Loader
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add pulsing-dots
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `dotCount` | `number` | `3` | Number of dots |
| `radius` | `number` | `6` | Dot radius |
| `spacing` | `number` | `25` | Dot spacing |
| `duration` | `number` | `800` | Animation ms |
| `color` | `string` | `"#00C896"` | Dot color |

---

### QR Code
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-blur`, `@expo/vector-icons`, `react-native-qrcode-styled`
```bash
npx reacticx add qr-code
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `QRCodevalue` | `string` | default URL | QR data |
| `springConfig` | `object` | defaults | Spring physics |
| `backgroundColorFocused` | `string` | defaults | Expanded bg color |

---

### Radial Intro
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add radial-intro
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `orbitItems` | `{ id, src }[]` | Required | Orbit images |
| `stageSize` | `number` | `320` | Container size |
| `imageSize` | `number` | `60` | Image size |
| `spinDuration` | `number` | `30` | Spin duration (sec) |
| `expanded` | `boolean` | `false` | Expanded state |
| `onCenterPress` | `function` | Optional | Center press callback |

---

### Ripple
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `expo-blur`, `react-native-worklets`
```bash
npx reacticx add ripple
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Content to wrap |
| `onPress` | `function` | undefined | Press callback |
| `rippleConfig.color` | `string` | `"rgba(255,255,255,0.2)"` | Ripple color |
| `rippleConfig.duration` | `number` | `600` | Duration ms |
| `rippleConfig.blur.enabled` | `boolean` | `false` | Enable blur |
| `centered` | `boolean` | `false` | Center ripple |
| `disabled` | `boolean` | `false` | Disable |

---

### Rolling Counter
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-blur`, `react-native-worklets`
```bash
npx reacticx add rolling-counter
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `SharedValue|number` | Required | Display value |
| `height` | `number` | `60` | Digit height |
| `width` | `number` | `40` | Digit width |
| `fontSize` | `number` | `48` | Font size |
| `color` | `string` | `"#000"` | Text color |
| `springConfig` | `object` | defaults | Spring config |

---

### Rotate Carousel
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-haptics`, `react-native-worklets`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add rotate-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Carousel data |
| `renderItem` | `function` | Required | Item renderer |
| `rotatePercentage` | `number` | `90` | 3D rotation angle |
| `spacing` | `number` | `20` | Item spacing |

---

### Rotating Square
**Category:** Components
```bash
npx reacticx add rotating-square
```
Animated rotating square loading indicator.

---

### Ruler
**Category:** Components
```bash
npx reacticx add ruler
```
Interactive ruler control with haptic feedback.

---

### Scale Carousel
**Category:** Components
```bash
npx reacticx add scale-carousel
```
Scale-based horizontal carousel with size transitions.

---

### Scrollable Search
**Category:** Components
```bash
npx reacticx add scrollable-search
```
Search component with scroll-aware animations.

---

### Search Bar
**Category:** Components
```bash
npx reacticx add search-bar
```
Animated search bar with expand/collapse transitions.

---

### Segmented Control
**Category:** Components
```bash
npx reacticx add segmented-control
```
iOS-style animated segmented control.

---

### Seekbar
**Category:** Components
```bash
npx reacticx add seekbar
```
Animated seek/progress bar with drag interaction.

---

### Shimmer
**Category:** Components
```bash
npx reacticx add shimmer
```
Shimmer loading placeholder effect.

---

### Shimmer Wave Text
**Category:** Components
```bash
npx reacticx add shimmer-wave
```
Shimmer wave animation flowing across text.

---

### Spinner Arc
**Category:** Components
```bash
npx reacticx add spinner-arc
```
Arc-style loading spinner with rotation animation.

---

### Split View
**Category:** Components
```bash
npx reacticx add split-view
```
Resizable split view layout with drag separator.

---

### Stack Aware Tabs
**Category:** Components
```bash
npx reacticx add stack-aware-tabs
```
Tab navigation aware of navigation stack state.

---

### Stack Cards
**Category:** Components
```bash
npx reacticx add stack-cards
```
Stacked card layout with swipe gestures.

---

### Stepper
**Category:** Components
```bash
npx reacticx add stepper
```
Animated stepper/quantity control.

---

### Switch
**Category:** Components | **Deps:** `react-native-reanimated`
```bash
npx reacticx add switch
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `boolean` | Required | Toggle state |
| `onValueChange` | `function` | Required | Change callback |
| `width` | `number` | `56` | Track width |
| `height` | `number` | `32` | Track height |
| `onColor` | `string` | `"#4CD964"` | Active color |
| `offColor` | `string` | `"#E9E9EA"` | Inactive color |
| `thumbColor` | `string` | `"#FFFFFF"` | Thumb color |
| `thumbOnIcon` | `ReactNode` | -- | On icon |
| `thumbOffIcon` | `ReactNode` | -- | Off icon |
| `iconAnimationType` | `"fade"|"scale"|"rotate"|"bounce"` | `"fade"` | Icon transition |

---

### Tabs
**Category:** Components
```bash
npx reacticx add tabs
```
Animated tab component with customizable transitions.

---

### Theme Switch
**Category:** Components | **Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
```bash
npx reacticx add theme-switch
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `theme` | `ThemeMode` | Required | Current theme |
| `onThemeChange` | `function` | Required | Theme callback |
| `animationType` | `AnimationType` | `Circular` | Transition type |
| `duration` | `number` | `500` | Animation ms |
| `children` | `ReactNode` | Required | App content |

Skia-powered theme transitions. Supports Circular, Fade, Slide, and other animation types.

---

### Tilt Carousel
**Category:** Components | **Deps:** `react-native-reanimated`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add tilt-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Carousel items |
| `renderItem` | `function` | Required | Item renderer |
| `itemWidth` | `number` | `250` | Item width |
| `itemHeight` | `number` | `400` | Item height |
| `rotationAngle` | `number` | `20` | Tilt degrees |
| `translateYValue` | `number` | `60` | Vertical lift |
| `transformOrigin` | `"top"|"center"|"bottom"` | `"bottom"` | Rotation origin |
| `useBlur` | `boolean` | `false` | Blur non-center items |

---

### Title
**Category:** Components | **Deps:** `react-native-reanimated`
```bash
npx reacticx add title
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `string` | Required | Text content |
| `level` | `"h1"-"h6"` | Optional | Heading level |
| `weight` | `FontWeight` | `"normal"` | Font weight |
| `color` | `string` | theme | Text color |
| `align` | `"left"|"center"|"right"` | `"left"` | Alignment |
| `animated` | `boolean` | `false` | Fade-in animation |
| `loading` | `boolean` | `false` | Skeleton loader |

Presets: `Title.H1` through `Title.H6`
```tsx
<Title.H1 color="#fff" weight="bold" animated>Welcome</Title.H1>
```

---

### Toast
**Category:** Components | **Deps:** `react-native-reanimated`, `react-native-worklets`, `react-native-safe-area-context`
```bash
npx reacticx add toast
```
Global API: Wrap app with `<ToastProviderWithViewport>`, use `useToast()` hook.

| Method | Description |
|--------|-------------|
| `toast.show(content, options)` | Show toast, returns ID |
| `toast.update(id, content, options)` | Update existing |
| `toast.dismiss(id)` | Dismiss specific |
| `toast.dismissAll()` | Clear all |

Options: `type` ("success"|"error"|"warning"|"info"|"default"), `duration` (3000), `position` ("top"|"bottom")
```tsx
const toast = useToast();
toast.show('Success!', { type: 'success', position: 'top', duration: 3000 });
```

---

### Vertical Flow Carousel
**Category:** Components | **Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add vertical-flow-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Items |
| `renderItem` | `function` | Required | Item renderer |
| `itemHeight` | `number` | `120` | Item height |
| `showBlur` | `boolean` | `true` | Blur inactive |
| `rotationAngle` | `number` | `12` | Rotation angle |
| `scaleInactive` | `number` | `0.85` | Inactive scale |
| `snapEnabled` | `boolean` | `true` | Snap scrolling |

---

### Vertical Page Carousel
**Category:** Components | **Deps:** `react-native-reanimated`, `@sbaiahmed1/react-native-blur`, `react-native-worklets`, `expo-haptics`
```bash
npx reacticx add vertical-page-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Items |
| `renderItem` | `function` | Required | Item renderer |
| `itemHeight` | `number` | `height*0.7` | Item height |
| `scaleRange` | `[number,number,number]` | `[0.9,1,0.9]` | Scale values |
| `opacityRange` | `[number,number,number]` | `[0.5,1,0.5]` | Opacity values |
| `useBlur` | `boolean` | `true` | Blur inactive |
| `pagingEnabled` | `boolean` | `true` | Snap paging |

---

## Common Dependencies Reference

| Package | Used By |
|---------|---------|
| `react-native-reanimated` | Nearly all components |
| `react-native-gesture-handler` | Carousels, sliders, switches, ripple |
| `@shopify/react-native-skia` | Shaders, gooey effects, theme switch |
| `react-native-svg` | Loaders, glow, curved marquee |
| `expo-blur` | Text effects, carousels, headers |
| `expo-haptics` | Accordion, pagination, pickers |
| `expo-linear-gradient` | Button, progress, headers |
| `react-native-worklets` | Many animation-heavy components |
| `@sbaiahmed1/react-native-blur` | Carousels (blur variant) |
| `@expo/vector-icons` | Icon-based components |
| `react-native-safe-area-context` | Headers, toast |
| `expo-symbols` | Gooey switch, empty state |

---

## Best Practices

1. **Always wrap with GestureHandlerRootView** when using gesture-based components
2. **Install dependencies** listed on each component's page before using
3. **Use `npx reacticx add`** for automatic file placement, or copy-paste manually
4. **Reanimated setup**: Ensure babel plugin is configured (`react-native-reanimated/plugin`)
5. **Skia components** require `@shopify/react-native-skia` native module installation
6. **Performance**: All animations target 60fps using Reanimated's UI thread execution
7. **Platform notes**: Some blur effects (expo-blur) work best on iOS; Android may need alternatives
