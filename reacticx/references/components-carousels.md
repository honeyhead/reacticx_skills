# Carousel & Scrollable Components

## Contents
- [Blur Carousel](#blur-carousel)
- [Cinematic Carousel](#cinematic-carousel)
- [Circular Carousel](#circular-carousel)
- [Circular List](#circular-list)
- [Material Carousel](#material-carousel)
- [Parallax Carousel](#parallax-carousel)
- [Rotate Carousel](#rotate-carousel)
- [Scale Carousel](#scale-carousel)
- [Tilt Carousel](#tilt-carousel)
- [Vertical Flow Carousel](#vertical-flow-carousel)
- [Vertical Page Carousel](#vertical-page-carousel)
- [Marquee](#marquee)
- [Matched Geometry](#matched-geometry)

> Most carousels follow the same pattern: `data` array + `renderItem` callback. One representative example shown below for Parallax Carousel applies to all carousel variants.

## Blur Carousel
**Deps:** `react-native-reanimated`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add blur-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Carousel items |
| `renderItem` | `function` | Required | Item renderer |
| `spacing` | `number` | `20` | Item spacing |
| `itemWidth` | `number` | `SCREEN_WIDTH * 0.75` | Item width |

## Cinematic Carousel
**Deps:** `react-native-reanimated`, `@sbaiahmed1/react-native-blur`
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

## Circular Carousel
**Deps:** `react-native-reanimated`, `expo-blur`, `react-native-worklets`
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

## Circular List
**Deps:** `react-native-reanimated`, `react-native-worklets`, `expo-blur`, `expo-haptics`
```bash
npx reacticx add circular-list
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `string[]` | Required | Image URI array |
| `scaleEnabled` | `boolean` | `false` | Enable scale animation |

## Material Carousel
**Deps:** `react-native-reanimated`
```bash
npx reacticx add material-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `string[]` | Required | Image URI array |
| `renderItem` | `function` | Optional | Custom renderer |

## Parallax Carousel
**Deps:** `react-native-reanimated`, `expo-haptics`, `react-native-worklets`
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

Requires `GestureHandlerRootView`.

```tsx
import { ParallaxCarousel } from "@/components/molecules/parallax-carousel";

const DATA = [
  { image: { uri: "https://example.com/1.jpg" } },
  { image: { uri: "https://example.com/2.jpg" } },
];

<GestureHandlerRootView style={{ flex: 1 }}>
  <ParallaxCarousel
    data={DATA}
    parallaxIntensity={0.9}
    renderItem={({ item }) => (
      <Image source={item.image} style={{ width: "100%", height: "100%", borderRadius: 20 }} />
    )}
  />
</GestureHandlerRootView>
```

## Rotate Carousel
**Deps:** `react-native-reanimated`, `expo-haptics`, `react-native-worklets`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add rotate-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Carousel data |
| `renderItem` | `function` | Required | Item renderer |
| `rotatePercentage` | `number` | `90` | 3D rotation angle |
| `spacing` | `number` | `20` | Item spacing |

## Scale Carousel
**Deps:** `react-native-reanimated`, `expo-haptics`, `react-native-worklets`
```bash
npx reacticx add scale-carousel
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `data` | `array` | Required | Carousel items |
| `renderItem` | `function` | Required | Item renderer |
| `scaleRange` | `[number,number,number]` | `[1.6,1,1.6]` | Scale [prev,center,next] |
| `rotationRange` | `[number,number,number]` | `[15,0,-10]` | Rotation degrees |
| `pagingEnabled` | `boolean` | `true` | Snap paging |

## Tilt Carousel
**Deps:** `react-native-reanimated`, `@sbaiahmed1/react-native-blur`
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

## Vertical Flow Carousel
**Deps:** `react-native-reanimated`, `expo-blur`
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

## Vertical Page Carousel
**Deps:** `react-native-reanimated`, `@sbaiahmed1/react-native-blur`, `react-native-worklets`, `expo-haptics`
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

## Marquee
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`
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

## Matched Geometry
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `expo-blur`, `react-native-worklets`
```bash
npx reacticx add matched-geometry
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `id` | `string` | Required | Unique transition ID |
| `children` | `ReactNode` | Required | Content |
| `onPress` | `function` | Optional | Press callback |

Requires `GestureHandlerRootView`. Drag ~300px triggers dismissal.
