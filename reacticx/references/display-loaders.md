# Loader Components

## Contents
- [Circle Loader](#circle-loader)
- [Circular Loader](#circular-loader)
- [Orbitdot Loader](#orbitdot-loader)
- [Pulsing Loader](#pulsing-loader)
- [Rotating Square](#rotating-square)
- [Spinner Arc](#spinner-arc)

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
