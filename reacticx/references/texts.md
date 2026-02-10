# Text Animation Components

## Animated Text
**Deps:** `react-native-reanimated`, `expo-blur`
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
| `exitFrom`/`exitTo` | `object` | defaults | Exit states |
```tsx
<AnimatedText
  text="Hello World"
  animationConfig={{ spring: { damping: 15, stiffness: 210, mass: 1 }, characterDelay: 15 }}
  enterFrom={{ opacity: 0, translateY: 55, scale: 0.2 }}
  style={{ color: "#fff", fontSize: 40 }}
/>
```

## Dynamic Text
**Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add dynamic-text
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `items` | `DynamicTextItem[]` | Required | `{ text, id? }` items to cycle |
| `loop` | `boolean` | `false` | Enable looping |
| `loopCount` | `number` | `-1` | Loop count (-1 = infinite) |
| `animationPreset` | `"fade"|"zoom"|"custom"` | `"fade"` | Animation style |
| `animationDirection` | `"up"|"down"` | `"up"` | Direction |
| `paused` | `boolean` | `false` | Pause animation |
| `onIndexChange` | `function` | undefined | Index change callback |
```tsx
<DynamicText items={[{ text: "Hello" }, { text: "World" }]} loop dot={{ size: 5 }} />
```

## Fade Text
**Deps:** `react-native-reanimated`, `expo-blur`
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
<FadeText inputs={["Hello World!", "Reacticx rocks!"]} duration={3500} wordDelay={300} />
```

## Gooey Text
**Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
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
<GooeyText texts={["REACTICX", "IS", "AWESOME!"]} color="white" fontSize={50} />
```

## Curved Marquee
**Deps:** `react-native-reanimated`, `react-native-svg`
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

## Staggered Text
**Deps:** `react-native-reanimated`, `@shopify/react-native-skia`
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
<StaggeredText texts={["Hello", "World"]} activeIndex={0} fontSize={35} color="#fff" />
```
