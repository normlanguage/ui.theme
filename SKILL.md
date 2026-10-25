# ui.theme Skill

Use this skill to work with Norm module `ui.theme` version 3. Use only declarations listed below.

## `ui.theme`

### `Color`

```norm
value Color
```

#### `Color`

```norm
Color(String hex)
```

#### `Color`

```norm
Color(Integer rgba)
```

#### `hex`

```norm
String hex()
```

#### `alpha`

```norm
Double alpha()
```

#### `withOpacity`

```norm
Color withOpacity(Double alpha)
```

#### `contrast`

```norm
Double contrast(Color other)
```

#### `mix`

```norm
Color mix(Color other, Double amount)
```

#### `tone`

```norm
Color tone(Double lightness, Double chromaScale)
```

### `ColorPair`

```norm
value ColorPair
```

#### `background`

```norm
Color background
```

#### `foreground`

```norm
Color foreground
```

### `ControlState`

```norm
value ControlState
```

#### `background`

```norm
Color background
```

#### `foreground`

```norm
Color foreground
```

#### `border`

```norm
Color border
```

### `ControlColors`

```norm
value ControlColors
```

#### `normal`

```norm
ControlState normal
```

#### `hovered`

```norm
ControlState hovered
```

#### `pressed`

```norm
ControlState pressed
```

#### `disabled`

```norm
ControlState disabled
```

#### `focusRing`

```norm
Color focusRing
```

## `ui.theme`

### `ThemeSource`

```norm
interface ThemeSource
```

#### `current`

```norm
Theme current()
```

#### `watch`

```norm
Resource watch(Void changed(Theme theme))
```

### `ThemeScope`

```norm
interface ThemeScope extends ThemeSource, Resource
```

#### `setOverride`

```norm
Void setOverride(ThemeOverride override)
```

#### `scope`

```norm
ThemeScope scope(ThemeOverride override)
```

### `ThemeManager`

```norm
class ThemeManager implements ThemeSource, Resource
```

#### `ThemeManager`

```norm
ThemeManager(ThemeDefinition definition, ThemeMode mode)
```

#### `current`

```norm
Theme current()
```

#### `watch`

```norm
Resource watch(Void changed(Theme theme))
```

#### `scope`

```norm
ThemeScope scope(ThemeOverride override)
```

#### `setMode`

```norm
Void setMode(ThemeMode mode)
```

#### `setDefinition`

```norm
Void setDefinition(ThemeDefinition definition)
```

#### `configure`

```norm
Void configure(ThemeDefinition definition, ThemeMode mode)
```

#### `close`

```norm
Void close()
```

## `ui.theme`

### `ThemeMode`

```norm
enum ThemeMode
```

#### `Light`

```norm
Light
```

#### `Dark`

```norm
Dark
```

### `Tone`

```norm
enum Tone
```

#### `Neutral`

```norm
Neutral
```

#### `Primary`

```norm
Primary
```

#### `Secondary`

```norm
Secondary
```

#### `Success`

```norm
Success
```

#### `Warning`

```norm
Warning
```

#### `Danger`

```norm
Danger
```

#### `Info`

```norm
Info
```

### `Appearance`

```norm
enum Appearance
```

#### `Filled`

```norm
Filled
```

#### `Soft`

```norm
Soft
```

#### `Outlined`

```norm
Outlined
```

#### `Plain`

```norm
Plain
```

### `ThemeDefinition`

```norm
value ThemeDefinition
```

#### `primary`

```norm
Color primary
```

#### `secondary`

```norm
Color? secondary
```

#### `neutral`

```norm
Color? neutral
```

#### `success`

```norm
Color success
```

#### `warning`

```norm
Color warning
```

#### `danger`

```norm
Color danger
```

#### `info`

```norm
Color info
```

### `ThemeOverride`

```norm
value ThemeOverride
```

#### `mode`

```norm
ThemeMode? mode
```

#### `primary`

```norm
Color? primary
```

#### `secondary`

```norm
Color? secondary
```

#### `neutral`

```norm
Color? neutral
```

#### `success`

```norm
Color? success
```

#### `warning`

```norm
Color? warning
```

#### `danger`

```norm
Color? danger
```

#### `info`

```norm
Color? info
```

### `Theme`

```norm
value Theme
```

#### `definition`

```norm
ThemeDefinition definition
```

#### `mode`

```norm
ThemeMode mode
```

#### `canvas`

```norm
ColorPair canvas
```

#### `surface`

```norm
ColorPair surface
```

#### `surfaceRaised`

```norm
ColorPair surfaceRaised
```

#### `textMuted`

```norm
Color textMuted
```

#### `outline`

```norm
Color outline
```

#### `divider`

```norm
Color divider
```

#### `scrim`

```norm
Color scrim
```

#### `control`

```norm
ControlColors control(Tone tone, Appearance appearance, Boolean selected)
```

### `generateTheme`

```norm
Theme generateTheme(ThemeDefinition definition, ThemeMode mode)
```

