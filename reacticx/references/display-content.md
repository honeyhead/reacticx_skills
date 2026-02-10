# Content & Display Components

## Contents
- [Animated Chip Group](#animated-chip-group)
- [Animated Header ScrollView](#animated-header-scrollview)
- [Animated Masked Text](#animated-masked-text)
- [Avatar](#avatar)
- [Avatar Group](#avatar-group)
- [Badge](#badge)
- [Empty State](#empty-state)
- [Title](#title)
- [Toast](#toast)
- [QR Code](#qr-code)

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
