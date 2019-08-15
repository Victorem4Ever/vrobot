# vrobot

⚠ _Work in progress. Windows is supported only._

Basic desktop automation functions for v lang.

## Plans

- [x] Add more mouse easing functions, currently it only has linear
- [ ] Screen related functions such as `screen_size()`, `get_pixel_color()`...
- [ ] Keyboard simulation and hooks

## Example

```go
import vrobot

pos := vrobot.get_mouse_pos()
println('Current mouse position: $pos.x, $pos.y')

// Moves mouse twice returning to starting position
vrobot.move_mouse_smooth(pos.x + 100, pos.y + 100, 1000)
vrobot.move_mouse_smooth_rel(-100, -100, 500)

// Drags from 100, 100 to 150, 150 with left click
vrobot.move_mouse(100, 100)
vrobot.drag(150, 150)
```

🖱️ Valid mouse buttons are: `left`, `right`, `middle`

## Functions

#### `get_mouse_pos() { x, y int }`

Returns struct with current mouse position.

#### `click(button string)`

Clicks with mouse.

#### `double_click(button string)`

Double clicks.

#### `drag(x, y int)`

Drags mouse (left) to specified position.

#### `drag_rel(offset_x, offset_y int)`

Drags mouse (left) relative to current position.

#### `move_mouse(x, y int)`

Moves mouse to x, y.

#### `move_mouse_rel(offset_x, offset_y, duration_ms int)`

Moves mouse relative to current position.

#### `move_mouse_smooth(dest_x, dest_y, duration_ms int, tween string)`

Moves mouse smoothly to dest_x, dest_y in duration_ms.

See list of available tweens below.

#### `move_mouse_smooth_rel(offset_x, offset_y, duration_ms int, tween string)`

Moves mouse smoothly, relative to current position in duration_ms.

See list of available tweens below.

## Available mouse tweens

- `ease_in_quad`
- `ease_out_quad`
- `ease_in_out_quad`
- `ease_in_cubic`
- `ease_out_cubic`
- `ease_in_out_cubic`
- `ease_in_quart`
- `ease_out_quart`
- `ease_in_out_quart`
- `ease_in_quint`
- `ease_out_quint`
- `ease_in_out_quint`
- `ease_in_sine`
- `ease_out_sine`
- `ease_in_out_sine`
- `ease_in_expo`
- `ease_out_expo`
- `ease_in_out_expo`
- `ease_in_circ`
- `ease_out_circ`
- `ease_in_out_circ`
- `ease_in_elastic`
- `ease_out_elastic`
- `ease_in_out_elastic`
- `ease_in_back`
- `ease_out_back`
- `ease_in_out_back`
- `ease_in_bounce`
- `ease_out_bounce`
- `ease_in_out_bounce`
