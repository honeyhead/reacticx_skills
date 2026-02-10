# Effects & Visual Components

## Contents
- [Glow](#glow)
- [Ripple](#ripple)
- [Stack Cards](#stack-cards)
- [Infinite Menu](#infinite-menu)
- [Lanyard](#lanyard)
- [Radial Intro](#radial-intro)
- [Pagination](#pagination)

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
