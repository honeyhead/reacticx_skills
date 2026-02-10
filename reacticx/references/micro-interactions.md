# Micro Interaction Components

## Animated Scroll Progress
**Deps:** `react-native-reanimated`, `react-native-worklets`
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
```tsx
<AnimatedScrollProgress
  fabWidth={280} fabHeight={56} fabBottomOffset={50}
  fabBackgroundColor="#151515" fabEndBackgroundColor="#fff" fabBorderRadius={28}
  renderInitialContent={() => <Text style={{ color: "#fff" }}>Chapter 1</Text>}
  renderEndContent={() => <Text style={{ color: "#000" }}>Well done!</Text>}
>
  {/* Scrollable content */}
</AnimatedScrollProgress>
```

## Animated Theme Toggle
**Deps:** `react-native-reanimated`, `react-native-svg`
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
<AnimatedThemeToggle isDark={isDark} onToggle={() => setIsDark(!isDark)} size={98} />
```

## Animated Countdown
**Deps:** `react-native-reanimated`
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
<CountdownTimer targetDate={new Date("2026-12-31")} customization={{ numberColor: "#fff" }} />
```

## Elastic Slider
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`
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

## Flexi Button
**Deps:** `react-native-reanimated`, `expo-blur`, `@expo/vector-icons`
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

## Gooey Switch
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `@shopify/react-native-skia`, `react-native-worklets`, `@expo/vector-icons`, `expo-symbols`
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
<GooeySwitch activeColor="#8093ff" size={200} trackColor="#1a1a1a" gooey={35} />
```

## Hamburger
**Deps:** `react-native-reanimated`, `expo-blur`
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
const progress = useSharedValue(0);
<Hamburger progress={progress} color="#fff" size={90}
  onPress={() => { progress.value = withTiming(progress.value === 1 ? 0 : 1); }} />
```

## Spin Button
**Deps:** `react-native-reanimated`
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

## Stacked Chips
**Deps:** `react-native-reanimated`, `expo-haptics`, `expo-blur`
```bash
npx reacticx add stacked-chips
```
Compound: `StackedChips`, `StackedChips.Trigger`, `StackedChips.Content`
```tsx
<StackedChips>
  <StackedChips.Trigger><Text>Create</Text></StackedChips.Trigger>
  <StackedChips.Content><Text>Document</Text></StackedChips.Content>
</StackedChips>
```
