# ui.theme Skill

Use this skill to work with Norm module `ui.theme` version 5. Use only declarations listed below.

## `ui.theme`

Source: `color.norm`

### `Color`

```norm
value Color
```

#### `Color`

```norm
Color(String hex)
```

Parameters:

- `hex`: `String`

#### `Color`

```norm
Color(Integer rgba)
```

Parameters:

- `rgba`: `Integer`

#### `hex`

```norm
String hex()
```

Returns: `String`

#### `alpha`

```norm
Double alpha()
```

Returns: `Double`

#### `withOpacity`

```norm
Color withOpacity(Double alpha)
```

Parameters:

- `alpha`: `Double`

Returns: `Color`

#### `contrast`

```norm
Double contrast(Color other)
```

Parameters:

- `other`: `Color`

Returns: `Double`

#### `mix`

```norm
Color mix(Color other, Double amount)
```

Parameters:

- `other`: `Color`
- `amount`: `Double`

Returns: `Color`

#### `tone`

```norm
Color tone(Double lightness, Double chromaScale)
```

Parameters:

- `lightness`: `Double`
- `chromaScale`: `Double`

Returns: `Color`

### `ColorPair`

```norm
value ColorPair
```

#### `background`

```norm
Color background
```

Type: `Color`

#### `foreground`

```norm
Color foreground
```

Type: `Color`

### `ControlState`

```norm
value ControlState
```

#### `background`

```norm
Color background
```

Type: `Color`

#### `foreground`

```norm
Color foreground
```

Type: `Color`

#### `border`

```norm
Color border
```

Type: `Color`

### `ControlColors`

```norm
value ControlColors
```

#### `normal`

```norm
ControlState normal
```

Type: `ControlState`

#### `hovered`

```norm
ControlState hovered
```

Type: `ControlState`

#### `pressed`

```norm
ControlState pressed
```

Type: `ControlState`

#### `disabled`

```norm
ControlState disabled
```

Type: `ControlState`

#### `focusRing`

```norm
Color focusRing
```

Type: `Color`

## `ui.theme.internal`

Source: `internal/ColorMath.norm`

### `ColorMath`

```norm
class ColorMath
```

#### `ColorMath`

```norm
ColorMath(__JarBindingToken token)
```

Parameters:

- `token`: `__JarBindingToken`

### `colorMathAlpha`

```norm
Double colorMathAlpha(Integer arg0)
```

Parameters:

- `arg0`: `Integer`

Returns: `Double`

### `colorMathContrast`

```norm
Double colorMathContrast(Integer arg0, Integer arg1)
```

Parameters:

- `arg0`: `Integer`
- `arg1`: `Integer`

Returns: `Double`

### `colorMathFormat`

```norm
String? colorMathFormat(Integer arg0)
```

Parameters:

- `arg0`: `Integer`

Returns: `String?`

### `colorMathMix`

```norm
Integer colorMathMix(Integer arg0, Integer arg1, Double arg2)
```

Parameters:

- `arg0`: `Integer`
- `arg1`: `Integer`
- `arg2`: `Double`

Returns: `Integer`

### `colorMathOpacity`

```norm
Integer colorMathOpacity(Integer arg0, Double arg1)
```

Parameters:

- `arg0`: `Integer`
- `arg1`: `Double`

Returns: `Integer`

### `colorMathParse`

```norm
Integer colorMathParse(String? arg0)
```

Parameters:

- `arg0`: `String?`

Returns: `Integer`

### `colorMathTone`

```norm
Integer colorMathTone(Integer arg0, Double arg1, Double arg2)
```

Parameters:

- `arg0`: `Integer`
- `arg1`: `Double`
- `arg2`: `Double`

Returns: `Integer`

## `ui.theme`

Source: `lifecycle.norm`

### `ThemeSource`

```norm
interface ThemeSource
```

#### `current`

```norm
Theme current()
```

Returns: `Theme`

#### `watch`

```norm
Resource watch(Void changed(Theme theme))
```

Parameters:

- `changed`: `Function<Void(Theme)>`

Returns: `Resource`

### `ThemeScope`

```norm
interface ThemeScope extends ThemeSource, Resource
```

#### `setOverride`

```norm
Void setOverride(ThemeOverride override)
```

Parameters:

- `override`: `ThemeOverride`

Returns: `Void`

#### `scope`

```norm
ThemeScope scope(ThemeOverride override)
```

Parameters:

- `override`: `ThemeOverride`

Returns: `ThemeScope`

### `ThemeManager`

```norm
class ThemeManager implements ThemeSource, Resource
```

#### `ThemeManager`

```norm
ThemeManager(ThemeDefinition definition, ThemeMode mode)
```

Parameters:

- `definition`: `ThemeDefinition`
- `mode`: `ThemeMode`

#### `current`

```norm
Theme current()
```

Returns: `Theme`

#### `watch`

```norm
Resource watch(Void changed(Theme theme))
```

Parameters:

- `changed`: `Function<Void(Theme)>`

Returns: `Resource`

#### `scope`

```norm
ThemeScope scope(ThemeOverride override)
```

Parameters:

- `override`: `ThemeOverride`

Returns: `ThemeScope`

#### `setMode`

```norm
Void setMode(ThemeMode mode)
```

Parameters:

- `mode`: `ThemeMode`

Returns: `Void`

#### `setDefinition`

```norm
Void setDefinition(ThemeDefinition definition)
```

Parameters:

- `definition`: `ThemeDefinition`

Returns: `Void`

#### `configure`

```norm
Void configure(ThemeDefinition definition, ThemeMode mode)
```

Parameters:

- `definition`: `ThemeDefinition`
- `mode`: `ThemeMode`

Returns: `Void`

#### `close`

```norm
Void close()
```

Returns: `Void`

## `ui.theme`

Source: `palette.norm`

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

Type: `Color`

#### `secondary`

```norm
Color? secondary
```

Type: `Color?`

#### `neutral`

```norm
Color? neutral
```

Type: `Color?`

#### `success`

```norm
Color success
```

Type: `Color`

#### `warning`

```norm
Color warning
```

Type: `Color`

#### `danger`

```norm
Color danger
```

Type: `Color`

#### `info`

```norm
Color info
```

Type: `Color`

### `ThemeOverride`

```norm
value ThemeOverride
```

#### `mode`

```norm
ThemeMode? mode
```

Type: `ThemeMode?`

#### `primary`

```norm
Color? primary
```

Type: `Color?`

#### `secondary`

```norm
Color? secondary
```

Type: `Color?`

#### `neutral`

```norm
Color? neutral
```

Type: `Color?`

#### `success`

```norm
Color? success
```

Type: `Color?`

#### `warning`

```norm
Color? warning
```

Type: `Color?`

#### `danger`

```norm
Color? danger
```

Type: `Color?`

#### `info`

```norm
Color? info
```

Type: `Color?`

### `Theme`

```norm
value Theme
```

#### `definition`

```norm
ThemeDefinition definition
```

Type: `ThemeDefinition`

#### `mode`

```norm
ThemeMode mode
```

Type: `ThemeMode`

#### `canvas`

```norm
ColorPair canvas
```

Type: `ColorPair`

#### `surface`

```norm
ColorPair surface
```

Type: `ColorPair`

#### `surfaceRaised`

```norm
ColorPair surfaceRaised
```

Type: `ColorPair`

#### `textMuted`

```norm
Color textMuted
```

Type: `Color`

#### `outline`

```norm
Color outline
```

Type: `Color`

#### `divider`

```norm
Color divider
```

Type: `Color`

#### `scrim`

```norm
Color scrim
```

Type: `Color`

#### `control`

```norm
ControlColors control(Tone tone, Appearance appearance, Boolean selected)
```

Parameters:

- `tone`: `Tone`
- `appearance`: `Appearance`
- `selected`: `Boolean`

Returns: `ControlColors`

### `generateTheme`

```norm
Theme generateTheme(ThemeDefinition definition, ThemeMode mode)
```

Parameters:

- `definition`: `ThemeDefinition`
- `mode`: `ThemeMode`

Returns: `Theme`

