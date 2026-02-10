# Input & Control Components

## Animated Input Bar
**Deps:** `react-native-reanimated`, `expo-blur`
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
```tsx
import AnimatedInputBar from "@/components/base/animated-input-bar";

const PLACEHOLDERS = ["Share your thoughts...", "What's on your mind?", "Type something..."];
const [text, setText] = useState("");

<AnimatedInputBar placeholders={PLACEHOLDERS} value={text} onChangeText={setText} animationInterval={900} />
```

## Button
**Deps:** `react-native-reanimated`, `react-native-worklets`, `expo-linear-gradient`
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
```tsx
import { Button } from "@/components/base/button";

<Button isLoading={loading} onPress={onPress} loadingText="Fetching..." showLoadingIndicator>
  <View style={{ flexDirection: "row", gap: 10, padding: 16 }}>
    <Ionicons name="arrow-forward" size={18} color="black" />
    <Text>Click Me!</Text>
  </View>
</Button>
```

## CheckBox
**Deps:** `react-native-reanimated`, `react-native-svg`
```bash
npx reacticx add check-box
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `checked` | `boolean` | `false` | Checkbox state |
| `checkmarkColor` | `string` | -- | Checkmark color |
| `stroke` | `number` | `1.5` | Stroke width |
| `size` | `number` | -- | Checkbox size |

## Flip Card
**Deps:** `react-native-reanimated`, `expo-haptics`, `@sbaiahmed1/react-native-blur`
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
```tsx
import { FlipCard } from "@/components";

<FlipCard width={340} height={320} animationDuration={700} borderRadius={16} enableHaptics blurTint="dark">
  <FlipCard.Front>{/* Front content */}</FlipCard.Front>
  <FlipCard.Back>{/* Back content */}</FlipCard.Back>
  <FlipCard.Trigger asChild={false} />
</FlipCard>
```

## OTP Input
**Deps:** `react-native-reanimated`
```bash
npx reacticx add otp-input
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `otpCount` | `number` | `6` | Fields (4-6) |
| `error` | `boolean` | `false` | Error state (shake) |
| `onInputChange` | `function` | -- | Input callback |
| `onInputFinished` | `function` | -- | Completion callback |
| `inputWidth` | `number` | `60` | Field width |
| `inputHeight` | `number` | `60` | Field height |
| `animationVariant` | `string` | `"fadeSlideDown"` | Entry animation |
```tsx
<OtpInput otpCount={4} error={error} onInputFinished={(code) => verify(code)} />
```

## Picker
**Deps:** `react-native-reanimated`, `react-native-worklets`, `expo-blur`, `react-native-gesture-handler`, `expo-linear-gradient`, `expo-haptics`
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
<Picker items={["Day","Afternoon","Evening","Night"]} onItemChange={setSelected} />
```

## Ruler
**Deps:** `react-native-reanimated`, `expo-haptics`, `react-native-gesture-handler`, `react-native-worklets`, `@shopify/react-native-skia`
```bash
npx reacticx add ruler
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `height`/`width` | `number` | -- | Dimensions |
| `minValue`/`maxValue` | `number` | -- | Range |
| `step` | `number` | -- | Tick increment |
| `onValueChange` | `function` | -- | Value callback |
| `tickColor` | `string` | `"rgba(255,255,255,0.6)"` | Tick color |
| `activeTickColor` | `string` | `"#00D4FF"` | Active color |
| `showCursor` | `boolean` | `true` | Center cursor |
| `enableHaptics` | `boolean` | `false` | Haptics |

## Scrollable Search
**Deps:** `react-native-reanimated`, `react-native-worklets`, `react-native-safe-area-context`, `expo-blur`
```bash
npx reacticx add scrollable-search
```
Compound: `ScrollableSearch`, `.ScrollContent`, `.Overlay`, `.FocusedScreen`

| Prop (ScrollContent) | Type | Default | Description |
|------|------|---------|-------------|
| `pullThreshold` | `number` | `80` | Pull distance for activation |

| Prop (Overlay) | Type | Default | Description |
|------|------|---------|-------------|
| `enableBlur` | `boolean` | `true` | Blur background |
| `maxBlurIntensity` | `number` | `80` | Max blur |
```tsx
import { ScrollableSearch, useScrollableSearch } from "@/components/base/scrollable-search";

<ScrollableSearch>
  <ScrollableSearch.ScrollContent>{/* Scrollable content */}</ScrollableSearch.ScrollContent>
  <SearchBarComponent />
  <ScrollableSearch.Overlay>
    <ScrollableSearch.FocusedScreen>{/* Search results */}</ScrollableSearch.FocusedScreen>
  </ScrollableSearch.Overlay>
</ScrollableSearch>
```

## Search Bar
**Deps:** `react-native-reanimated`, `@expo/vector-icons`, `react-native-worklets`, `expo-blur`, `expo-symbols`
```bash
npx reacticx add search-bar
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `placeholder` | `string` | `"Search"` | Placeholder |
| `onSearch` | `function` | -- | Text callback |
| `tint` | `string` | `"#007AFF"` | Accent color |
| `containerWidth` | `number` | `screenWidth-32` | Width |
| `enableWidthAnimation` | `boolean` | `true` | Animate focus |
| `centerWhenUnfocused` | `boolean` | `true` | Center content |

## Seekbar
**Deps:** `react-native-reanimated`, `react-native-worklets`, `react-native-gesture-handler`, `expo-haptics`
```bash
npx reacticx add seekbar
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `number` | Required | Progress 0-1 |
| `onValueChange` | `function` | Required | Value callback |
| `width` | `number` | `300` | Track width |
| `height` | `number` | `8` | Track height |
| `activeColor` | `string` | `"#FFFFFF"` | Fill color |
| `thumbSize` | `number` | `35` | Thumb diameter |
| `tapToSeek` | `boolean` | `true` | Tap-to-seek |

## Stepper
**Deps:** `react-native-reanimated`, `@expo/vector-icons`
```bash
npx reacticx add stepper
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `number` | Required | Current value |
| `onValueChange` | `function` | Required | Value callback |
| `min` | `number` | `0` | Min value |
| `max` | `number` | `100` | Max value |
| `step` | `number` | `1` | Increment |
| `disabled` | `boolean` | `false` | Disable |
| `size` | `number` | `40` | Height |

## Switch
**Deps:** `react-native-reanimated`
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
| `thumbOnIcon`/`thumbOffIcon` | `ReactNode` | -- | Thumb icons |
| `iconAnimationType` | `"fade"|"scale"|"rotate"|"bounce"` | `"fade"` | Icon transition |

## Theme Switch
**Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
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

Supports: Circular, CircularInverted, Wipe, WipeRight, WipeDown, WipeUp.
```tsx
import { ThemeSwitcher, AnimationType, ThemeMode } from "@/components/organisms/theme-switch";

<ThemeSwitcher theme={theme} onThemeChange={setTheme} animationType={AnimationType.Circular}>
  {/* Your app content */}
</ThemeSwitcher>
```
