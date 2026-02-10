# Navigation & Layout Components

## Accordion
**Deps:** `react-native-reanimated`, `expo-haptics`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add accordion
```
Compound: `Accordion`, `Accordion.Item`, `Accordion.Trigger`, `Accordion.Content`

| Prop (Accordion) | Type | Default | Description |
|------|------|---------|-------------|
| `type` | `"single"|"multiple"` | `"single"` | Expansion mode |
| `theme` | `AccordionTheme` | light | Theme config |
| `spacing` | `number` | `0` | Gap between items |

| Prop (Item) | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `string` | Required | Unique ID |
| `pop` | `boolean` | `false` | Scale animation |
| `icon` | `"cross"|"chevron"` | `"chevron"` | Icon style |
```tsx
<Accordion type="single" spacing={8}>
  <Accordion.Item value="1" icon="chevron">
    <Accordion.Trigger><Text>Question</Text></Accordion.Trigger>
    <Accordion.Content><Text>Answer</Text></Accordion.Content>
  </Accordion.Item>
</Accordion>
```

## Bottom Sheet
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`
```bash
npx reacticx add bottom-sheet
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Sheet content |
| `snapPoints` | `array` | Required | Snap position values |
| `enableBackdrop` | `boolean` | `true` | Show overlay |
| `dismissOnBackdropPress` | `boolean` | `true` | Close on backdrop tap |
| `dismissOnSwipeDown` | `boolean` | `true` | Close on swipe down |
| `onClose` | `function` | -- | Close callback |
| `showHandle` | `boolean` | `true` | Show drag handle |
| `backgroundColor` | `string` | `"#FFFFFF"` | Sheet bg color |
| `borderRadius` | `number` | `24` | Corner radius |
| `enableDynamicSizing` | `boolean` | `false` | Dynamic height |

**Methods (ref):** `snapToIndex(i)`, `expand()`, `collapse()`, `close()`, `getCurrentIndex()`
```tsx
const sheetRef = useRef<BottomSheetMethods>(null);
<BottomSheet ref={sheetRef} snapPoints={["50%","90%"]} backgroundColor="#1c1c1e">
  <View style={{ padding: 20 }}><Text>Content</Text></View>
</BottomSheet>
```

## Bottom Sheet Stack
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`
```bash
npx reacticx add bottom-sheet-stack
```
Wrap app with `<BottomSheetStackProvider>`. Use hooks:
- `useBottomSheet()` returns `{ present(component), dismiss() }`
- `useBottomSheetStack()` returns `{ pushSheet(config), popSheet(id?), popToRoot(), getStackDepth() }`
```tsx
// Setup: wrap app with provider
import { BottomSheetStackProvider, useBottomSheet } from '@/components/templates/bottom-sheet-stack';
import BottomSheet from '@/components/templates/bottom-sheet';

// In App root:
<BottomSheetStackProvider><AppContent /></BottomSheetStackProvider>

// In any component:
const { present, dismiss } = useBottomSheet();
present(<BottomSheet snapPoints={["75%"]} backgroundColor="#1c1c1e"><Content /></BottomSheet>);
```

## Curved Bottom Tabs
**Deps:** `react-native-reanimated`, `@react-navigation/bottom-tabs`, `react-native-svg`
```bash
npx reacticx add curved-bottom-tabs
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `tabs` | `Tab[]` | Required | `{ id, title, icon, badge? }` array |
| `currentIndex` | `number` | Required | Active tab |
| `onPress` | `function` | Required | Tab select callback |
| `gradient` | `[string,string]` | `["#121212","#1A1A1A"]` | Background gradient |
| `activeColor` | `string` | `"#ffffff"` | Active icon color |
| `inactiveColor` | `string` | `"#cccccc"` | Inactive icon color |
| `hideWhenKeyboardShown` | `boolean` | `false` | Auto-hide on keyboard |

Integrates with Expo Router's `Tabs` navigator. Requires `GestureHandlerRootView`.
```tsx
import { Tabs } from "expo-router";
import { CurvedBottomTabs } from "@/components/base/curved-bottom-tabs";

<Tabs tabBar={(props) => <CurvedBottomTabs {...props} />}>
  <Tabs.Screen name="home" options={{
    title: "Home",
    tabBarIcon: ({ focused }) => <Ionicons name={focused ? "home" : "home-outline"} size={20} color={focused ? "#fff" : "#B9B9B9"} />
  }} />
</Tabs>
```

## Dialog
**Deps:** `react-native-reanimated`, `expo-blur`, `react-native-worklets`
```bash
npx reacticx add dialog
```
Compound: `Dialog`, `Dialog.Trigger`, `Dialog.Backdrop`, `Dialog.Content`, `Dialog.Close`

| Prop (Backdrop) | Type | Default | Description |
|------|------|---------|-------------|
| `blurAmount` | `number` | `20` | Blur intensity |
| `backgroundColor` | `string` | `"rgba(0,0,0,0.5)"` | Overlay color |

Open: 550ms, Close: 650ms. Tapping outside dismisses.
```tsx
<Dialog>
  <Dialog.Trigger><Pressable><Text>Open</Text></Pressable></Dialog.Trigger>
  <Dialog.Backdrop blurAmount={25} />
  <Dialog.Content>
    <Text>Content</Text>
    <Dialog.Close asChild><Pressable><Text>Close</Text></Pressable></Dialog.Close>
  </Dialog.Content>
</Dialog>
```

## Disclosure Group
**Deps:** `react-native-reanimated`, `expo-blur`
```bash
npx reacticx add disclosure-group
```
Compound: `DisclosureGroup`, `DisclosureGroup.Trigger`, `DisclosureGroup.Items`, `DisclosureGroup.Item`

| Prop (Trigger) | Type | Default | Description |
|------|------|---------|-------------|
| `showChevron` | `boolean` | `true` | Show chevron |
| `chevronColor` | `string` | `"#ffffff"` | Chevron color |

| Prop (Items) | Type | Default | Description |
|------|------|---------|-------------|
| `maxHeight` | `number` | `400` | Max scrollable height |
| `scrollable` | `boolean` | `true` | Enable scroll |
| `useBlur` | `boolean` | `false` | Blur overlay |

## Dropdown
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `react-native-worklets`, `expo-haptics`
```bash
npx reacticx add dropdown
```
Compound: `Dropdown`, `Dropdown.Trigger`, `Dropdown.Content`, `Dropdown.Item`

| Prop (Content) | Type | Default | Description |
|------|------|---------|-------------|
| `position` | `"auto"|"top"|"bottom"|"left"|"right"` | `"auto"` | Menu position |
```tsx
<Dropdown>
  <Dropdown.Trigger><Text>Menu</Text></Dropdown.Trigger>
  <Dropdown.Content>
    <Dropdown.Item onPress={() => {}}><Text>Edit</Text></Dropdown.Item>
  </Dropdown.Content>
</Dropdown>
```

## Dynamic Island
**Deps:** `react-native-reanimated`, `expo-blur`, `expo-haptics`
```bash
npx reacticx add dynamic-island
```
Compound: `DynamicIsland.Provider`, `DynamicIsland.Trigger`, `DynamicIsland.Content`

| Prop (Provider) | Type | Default | Description |
|------|------|---------|-------------|
| `config` | `object` | -- | collapsedWidth/Height, expandedWidth/Height |
| `haptics` | `boolean` | `true` | Haptic feedback |
| `onExpand`/`onCollapse` | `function` | -- | State callbacks |

Hook: `useDynamicIsland()` returns `{ isExpanded, expand, collapse, toggle }`
```tsx
<DynamicIsland.Provider>
  <DynamicIsland.Trigger><Text>Tap</Text></DynamicIsland.Trigger>
  <DynamicIsland.Content><Text>Expanded!</Text></DynamicIsland.Content>
</DynamicIsland.Provider>
```

## Morphing Tab Bar
**Deps:** `react-native-reanimated`, `@shopify/react-native-skia`, `expo-haptics`
```bash
npx reacticx add morphing-tabbar
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `items` | `{ keyPath: string, name: string }[]` | DEFAULT | Tab items |
| `onTabChange` | `function` | Optional | Tab change callback |
| `initialActiveIndex` | `number` | `0` | Starting tab |
| `animationDuration` | `number` | `300` | Morph duration |
| `borderRadius` | `number` | `12` | Container radius |
| `enableGlass` | `boolean` | `false` | Glassmorphism effect |
```tsx
<MorphicTabBar
  items={[{ keyPath: '/home', name: 'Home' }, { keyPath: '/search', name: 'Search' }]}
  onTabChange={(keyPath, index) => console.log(keyPath)}
/>
```

## Segmented Control
**Deps:** `react-native-reanimated`, `expo-blur`, `react-native-worklets`, `react-native-gesture-handler`, `expo-haptics`
```bash
npx reacticx add segmented-control
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | `ReactNode` | Required | Segment content |
| `onChange` | `function` | Required | Selection callback |
| `currentIndex` | `number` | Required | Active segment |
| `preset` | `string` | `"ios"` | Visual style |
| `borderRadius` | `number` | `8` | Corner radius |
```tsx
<SegmentedControl currentIndex={index} onChange={setIndex} borderRadius={200}>
  <Text>Tab 1</Text><Text>Tab 2</Text><Text>Tab 3</Text>
</SegmentedControl>
```

## Split View
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `react-native-safe-area-context`
```bash
npx reacticx add split-view
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `topSectionItems` | `array` | Required | Top section data |
| `bottomSectionItems` | `array` | Required | Bottom section data |
| `bottomSectionTitle` | `string` | Required | Bottom title |
| `initialTopSectionHeight` | `number` | Required | Initial top height |
| `minSectionHeight` | `number` | Required | Min section height |
| `maxTopSectionHeight` | `number` | Required | Max top height |
| `springConfig` | `SpringConfig` | Required | Spring physics |
| `renderTopItem`/`renderBottomItem` | `function` | Required | Item renderers |
```tsx
import { SplitView } from "@/components/molecules/split-view";

<SplitView
  topSectionItems={notes} bottomSectionItems={tasks}
  bottomSectionTitle="Tasks"
  initialTopSectionHeight={300} minSectionHeight={10} maxTopSectionHeight={500}
  velocityThreshold={800} springConfig={{ damping: 20, stiffness: 150, mass: 0.5 }}
  containerBackgroundColor="#0a0a0a" sectionBackgroundColor="#141414"
  dividerBackgroundColor="#0a0a0a" dragHandleColor="#333"
  renderTopItem={({ item }) => <Text>{item.content}</Text>}
  renderBottomItem={({ item }) => <Text>{item.label}</Text>}
  topKeyExtractor={(item) => item.id} bottomKeyExtractor={(item) => item.id}
/>
```

## Stack Aware Tabs
**Deps:** `react-native-reanimated`, `react-native-gesture-handler`, `@expo/vector-icons`, `expo-haptics`, `expo-router`, `expo-blur`
```bash
npx reacticx add stack-aware-tabs
```
Bottom tab bar with animated focus scaling for Expo Router.
Use: `<Tabs tabBar={(props) => <StackAwareTabBar {...props} />}>`
```tsx
import { Tabs } from "expo-router";
import { StackAwareTabBar } from "@/components/base/stack-aware-tabs";

<Tabs tabBar={(props) => <StackAwareTabBar {...props} />}>
  <Tabs.Screen name="home" options={{ title: "Home", tabBarIcon: ({ focused }) => <Ionicons name={focused ? "home" : "home-outline"} size={20} /> }} />
</Tabs>
```

## Tabs
**Deps:** `react-native-reanimated`, `@sbaiahmed1/react-native-blur`
```bash
npx reacticx add tabs
```
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `tabs` | `Tab[]` | Required | `{ id, title?, contentComponent? }` |
| `activeColor` | `string` | `"#007AFF"` | Active tab color |
| `inactiveColor` | `string` | `"#666"` | Inactive color |
| `underlineColor` | `string` | `"#007AFF"` | Underline color |
| `underlineHeight` | `number` | `3` | Underline height |
