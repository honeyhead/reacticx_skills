# Display & Feedback Components

## Animated Chip Group
**Deps:** `react-native-reanimated`
```bash
npx reacticx add animated-chip
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `chips` | `ChipItem[]` | Required | `{ label, icon, activeColor, labelColor, inActiveBackgroundColor }` |
| `selectedIndex` | `number` | Optional | Selected index |
| `onChange` | `function` | Optional | Selection callback |
```tsx
import { ChipGroup } from "@/components";

const chips = [
  { label: "All", activeColor: "#fff", inActiveBackgroundColor: "#1a1a1a", labelColor: "#000",
    icon: () => <SymbolView name="square.grid.2x2.fill" size={18} tintColor={selected === 0 ? "#000" : "#555"} /> },
];

<ChipGroup chips={chips} selectedIndex={selected} onChange={setSelected} />
```

## Animated Header ScrollView
**Deps:** `react-native-reanimated`, `expo-linear-gradient`, `@react-native-masked-view/masked-view`, `expo-blur`, `react-native-safe-area-context`
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
  <Text>Content</Text>
</AnimatedHeaderScrollView>
```

## Animated Masked Text
**Deps:** `expo-linear-gradient`, `@react-native-masked-view/masked-view`
```bash
npx reacticx add animated-masked-text
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `string` | Required | Text content |
| `speed` | `number` | `1` | Animation speed |
| `baseTextColor` | `string` | `"#000000"` | Base text color |

## Avatar
**Deps:** `react-native-reanimated`, `react-native-worklets`
```bash
npx reacticx add avatar
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `image` | `{ uri, name? }` | Required | Image source |
| `size` | `number` | `40` | Avatar size |
| `showBorder` | `boolean` | `true` | Show border |
| `loading` | `boolean` | `false` | Shimmer loading |
| `showOnlineIndicator` | `boolean` | `false` | Status dot |
| `showText` | `boolean` | `false` | Show name |
| `textPosition` | `"bottom"|"right"|"top"` | `"bottom"` | Name position |

## Avatar Group
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`, `expo-haptics`
```bash
npx reacticx add avatar-group
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `avatars` | `{ id, uri?, name? }[]` | Required | Avatar items |
| `size` | `number` | `40` | Diameter |
| `max` | `number` | `5` | Max visible |
| `overlap` | `number` | `10` | Overlap distance |
| `onPress` | `function` | Optional | Press callback (id) |

## Badge
No additional deps required.
```bash
npx reacticx add badge
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `label` | `string` | Required | Badge text |
| `variant` | `"pending"|"notifications"|"error"|"warning"|"success"|"default"` | `"default"` | Style |
| `size` | `"lg"|"md"|"sm"` | `"md"` | Size |
| `icon` | `ReactNode` | -- | Optional icon |

## Circle Loader
**Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add circle-loader
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `dotColor` | `string` | `"#007AFF"` | Dot color |
| `dotRadius` | `number` | `6` | Dot radius |
| `dotSpacing` | `number` | `20` | Dot spacing |
| `duration` | `number` | `950` | Animation ms |

## Circular Loader
**Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add circular-loader
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `size` | `number` | `40` | Diameter |
| `strokeWidth` | `number` | `4` | Stroke width |
| `activeColor` | `string` | `"#000000"` | Arc color |
| `duration` | `number` | `1000` | Animation ms |
| `enableBlur` | `boolean` | `false` | Motion blur |

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

## Empty State
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

## Glow
**Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add glow
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Content to wrap |
| `size` | `number` | `4` | Border thickness |
| `color` | `string` | `"#8b5cf6"` | Primary glow color |
| `secondaryColor` | `string` | `"#ec4899"` | Secondary color |
| `duration` | `number` | `3000` | Cycle ms |
| `style` | `"pulse"|"wave"|"breathe"|"snap"|"spinner"|"linear"` | `"pulse"` | Animation |
| `intensity` | `number` | `1` | Opacity multiplier |
| `enabled` | `boolean` | `true` | Toggle glow |
```tsx
<Glow size={2} style="pulse" color="#8b5cf6">
  <View style={{ width: 280, height: 56, backgroundColor: "#151515", borderRadius: 28 }}>
    <Text>Glowing Button</Text>
  </View>
</Glow>
```

## Infinite Menu
**Deps:** `@shopify/react-native-skia`, `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`
```bash
npx reacticx add infinite-menu
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `items` | `{ image: string }[]` | Required | Menu items |
| `scale` | `number` | `1` | Sphere scale |
| `backgroundColor` | `string` | `"#000000"` | Background color |

3D radial menu using quaternion-based sphere projections.

## Lanyard
**Deps:** `@shopify/react-native-skia`, `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`, `expo-haptics`
```bash
npx reacticx add lanyard
```
Draggable card on flexible rope with gravity simulation. Experimental/unstable.

## Orbitdot Loader
**Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add orbiting-dots
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `dotColor` | `string` | `"#fff"` | Dot color |
| `dotRadius` | `number` | `4` | Dot radius |
| `size` | `number` | `40` | Component size |
| `duration` | `number` | `900` | Animation ms |
| `numDots` | `number` | `4` | Number of dots |

## Pagination
**Deps:** `react-native-reanimated`, `react-native-worklets`, `expo-haptics`, `react-native-gesture-handler`
```bash
npx reacticx add pagination
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `activeIndex` | `number` | Required | Current page |
| `totalItems` | `number` | Required | Total pages |
| `activeColor` | `string` | `"#c4c4c4"` | Active color |
| `inactiveColor` | `string` | `"#363636"` | Inactive color |
| `dotSize` | `number` | `10` | Dot diameter |
| `onIndexChange` | `function` | Optional | Callback |

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

## Pulsing Loader
**Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add pulsing-dots
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `dotCount` | `number` | `3` | Number of dots |
| `radius` | `number` | `6` | Dot radius |
| `duration` | `number` | `800` | Animation ms |
| `color` | `string` | `"#00C896"` | Dot color |

## QR Code
**Deps:** `react-native-reanimated`, `expo-blur`, `@expo/vector-icons`, `react-native-qrcode-styled`
```bash
npx reacticx add qr-code
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `QRCodevalue` | `string` | default URL | QR data |
| `springConfig` | `object` | defaults | Spring physics |
| `backgroundColorFocused` | `string` | defaults | Expanded bg |

Requires `GestureHandlerRootView`.

## Radial Intro
**Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add radial-intro
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `orbitItems` | `{ id, src }[]` | Required | Orbit images |
| `stageSize` | `number` | `320` | Container size |
| `imageSize` | `number` | `60` | Image size |
| `spinDuration` | `number` | `30` | Spin seconds |
| `expanded` | `boolean` | `false` | Expanded state |
| `onCenterPress` | `function` | Optional | Center callback |

## Ripple
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `expo-blur`, `react-native-worklets`
```bash
npx reacticx add ripple
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Content |
| `onPress` | `function` | undefined | Press callback |
| `rippleConfig.color` | `string` | `"rgba(255,255,255,0.2)"` | Color |
| `rippleConfig.duration` | `number` | `600` | Duration ms |
| `rippleConfig.blur.enabled` | `boolean` | `false` | Enable blur |
| `centered` | `boolean` | `false` | Center ripple |

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

## Rotating Square
**Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add rotating-square
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `color` | `string` | `"#FF5722"` | Square color |
| `squareSize` | `number` | `10` | Square size |
| `spacing` | `number` | `20` | Center distance |
| `size` | `number` | `60` | SVG size |
| `duration` | `number` | `1000` | Animation ms |

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

## Spinner Arc
**Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add spinner-arc
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `size` | `number` | `40` | Diameter |
| `colorStart` | `string` | `"#FF4E4E"` | Gradient start |
| `colorEnd` | `string` | `"#FF7A00"` | Gradient end |
| `strokeWidth` | `number` | `4` | Stroke width |
| `speed` | `number` | `1000` | Animation ms |
| `arcLength` | `number` | `90` | Arc degrees |

## Stack Cards
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `expo-blur`
```bash
npx reacticx add stack-cards
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Card items |
| `renderItem` | `function` | Required | Card renderer |
| `visibleCount` | `number` | `4` | Visible cards |
| `cardWidth`/`cardHeight` | `number` | `300` | Card dimensions |
| `blurIntensity` | `number` | `40` | Background blur |
| `useBlur` | `boolean` | `true` | Enable blur |

Vertical fling gesture navigation.

## Title
**Deps:** `react-native-reanimated`
```bash
npx reacticx add title
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `string` | Required | Text content |
| `level` | `"h1"-"h6"` | Optional | Heading level |
| `weight` | `FontWeight` | `"normal"` | Font weight |
| `color` | `string` | theme | Text color |
| `animated` | `boolean` | `false` | Fade-in |
| `loading` | `boolean` | `false` | Skeleton loader |

Presets: `Title.H1` through `Title.H6`

## Toast
**Deps:** `react-native-reanimated`, `react-native-worklets`, `react-native-safe-area-context`
```bash
npx reacticx add toast
```
Wrap app with `<ToastProviderWithViewport>`, use `useToast()` hook.

| Method | Description |
|--------|-------------|
| `toast.show(content, options)` | Show toast, returns ID |
| `toast.update(id, content, options)` | Update existing |
| `toast.dismiss(id)` | Dismiss specific |
| `toast.dismissAll()` | Clear all |

Options: `type` ("success"|"error"|"warning"|"info"|"default"), `duration` (3000), `position` ("top"|"bottom")
```tsx
const toast = useToast();
toast.show('Success!', { type: 'success', position: 'top' });
```
