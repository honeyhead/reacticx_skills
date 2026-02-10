# Progress & Transition Components

## Contents
- [Circular Progress](#circular-progress)
- [Progress](#progress)
- [Shimmer](#shimmer)
- [Shimmer Wave Text](#shimmer-wave-text)
- [Rolling Counter](#rolling-counter)

## Circular Progress
**Deps:** `react-native-reanimated`, `react-native-svg`
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
```tsx
import { useSharedValue, withTiming, Easing } from "react-native-reanimated";
import { CircularProgress } from "@/components/organisms/circular-progress";

const progress = useSharedValue(0);
useEffect(() => { progress.value = withTiming(72, { easing: Easing.bezier(0.95, 0.1, 0.95, 1), duration: 2000 }); }, []);

<CircularProgress progress={progress} size={120} strokeWidth={12} progressCircleColor="#ff4757"
  renderIcon={() => <FontAwesome name="heart" size={40} color="#ff4757" />} />
```

## Progress
**Deps:** `react-native-reanimated`, `expo-linear-gradient`
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

## Shimmer
**Deps:** `react-native-reanimated`, `expo-linear-gradient`
```bash
npx reacticx add shimmer
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `isLoading` | `boolean` | `true` | Loading state |
| `variant` | `"pulse"|"shimmer"` | `"shimmer"` | Animation |
| `direction` | `"leftToRight"|"rightToLeft"|"topToBottom"|"bottomToTop"` | `"leftToRight"` | Direction |
| `preset` | `"dark"|"light"|"twitter"|"neutral"` | `"dark"` | Color preset |
| `duration` | `number` | `1500` | Animation ms |

Group: `<ShimmerGroup isLoading={loading}>` wraps multiple `<Shimmer>` children.
```tsx
import { ShimmerGroup, Shimmer } from "@/components";

<ShimmerGroup isLoading={isLoading} preset="dark" duration={1000}>
  <Shimmer style={{ width: 100, height: 100, borderRadius: 50 }}>{/* Loaded content */}</Shimmer>
  <Shimmer style={{ width: 180, height: 28, borderRadius: 8 }}>{/* Loaded content */}</Shimmer>
</ShimmerGroup>
```

## Shimmer Wave Text
**Deps:** `react-native-reanimated`, `@react-native-masked-view/masked-view`, `expo-linear-gradient`
```bash
npx reacticx add shimmer-wave
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `text` | `string` | default text | Text to display |
| `textColor` | `string` | `"#212121"` | Text color |
| `textStyle` | `TextStyle` | -- | Text styling |

## Rolling Counter
**Deps:** `react-native-reanimated`, `expo-blur`, `react-native-worklets`
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
```tsx
import { useSharedValue } from "react-native-reanimated";
import { RollingCounter } from "@/components/organisms/rolling-counter";

const counter = useSharedValue(10);

<RollingCounter value={counter} height={64} width={42} fontSize={52} color="#fff"
  springConfig={{ stiffness: 110, damping: 14, mass: 0.5 }} />
```
