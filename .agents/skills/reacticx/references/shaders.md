# Shaders

All shader components require `react-native-reanimated` and `@shopify/react-native-skia`.

## Aurora
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

## Chroma Ring
```bash
npx reacticx add chroma-ring
```
Animated chromatic ring shader effect with customizable colors and animation speed.

## Energy Orb
```bash
npx reacticx add energy-orb
```
Glowing energy orb with shader-based rendering and customizable glow parameters.

## Siri Orb
```bash
npx reacticx add siri-orb
```
Siri-inspired orb animation using Skia shaders with fluid motion effects.

## Mesh Gradient
```bash
npx reacticx add mesh-gradient
```
Animated mesh gradient background with customizable control points and colors.

## Grainy Gradient
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

## Skia Ripple
**Additional deps:** `react-native-gesture-handler`
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

**RippleImage** adds: `source` (string), `fit` ("cover"|"contain"|"fill"|"none"|"scaleDown")
**RippleRect** adds: `color` (string), `children` (ReactNode)
```tsx
import { RippleImage } from "@/components/organisms/skia-ripple";
<GestureHandlerRootView>
  <RippleImage width={350} height={420} borderRadius={28} source="https://..." />
</GestureHandlerRootView>
```

## Wave Scrawler
**Additional deps:** `react-native-worklets`
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
