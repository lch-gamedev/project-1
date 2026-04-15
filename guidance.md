# Help Map
## If you want to...

### Move the player
Look up:
- `CharacterBody2D`
- input actions
- velocity
- `_physics_process()`

### Make walls solid
Look up:
- collision shapes
- `TileMap`
- static bodies
- collision layers

### Detect when the player touches something
Look up:
- `Area2D`
- `body_entered`
- signals

### Make a goal object
Look up:
- `Area2D`
- labels
- showing and hiding UI
- changing scenes

### Make a hazard
Look up:
- `Area2D`
- collision
- resetting player position
- timers

### Play sounds
Look up:
- `AudioStreamPlayer2D`
- importing audio
- playing sound on interaction

### Animate things
Look up:
- `AnimatedSprite2D`
- `AnimationPlayer`

### Restart the level
Look up:
- `get_tree().reload_current_scene()`

---

# Recipe Cards

## Recipe Card 1: Simple Player
### You need
- `CharacterBody2D`
- `Sprite2D` or `AnimatedSprite2D`
- `CollisionShape2D`

### Steps
1. Create a new scene with `CharacterBody2D`.
2. Add a sprite.
3. Add a collision shape.
4. Add movement code using input.
5. Instance the player into your level.

### Success check
- Can the player move?
- Does the player stop at walls?

---

## Recipe Card 2: Goal Object
### You need
- `Area2D`
- `Sprite2D`
- `CollisionShape2D`

### Steps
1. Create a goal scene using `Area2D`.
2. Add a sprite and collision shape.
3. Connect the `body_entered` signal.
4. Check if the body is the player.
5. Show a label: **You Win!**

### Success check
- Does touching the object trigger the win message?

---

## Recipe Card 3: Hazard
### You need
- `Area2D`
- `Sprite2D`
- `CollisionShape2D`

### Steps
1. Create a hazard scene.
2. Add a sprite and collision shape.
3. Connect `body_entered`.
4. When the player touches it, send them back to the start.

### Success check
- Does the obstacle make the game harder?

---

## Recipe Card 4: Key and Door
### You need
- one key object
- one door object
- a variable like `has_key`

### Steps
1. Start with `has_key = false`.
2. When the player touches the key, set `has_key = true`.
3. Remove or hide the key.
4. When the player touches the door, check `has_key`.
5. If `has_key` is true, open the door or win the game.

### Success check
- Can the player only open the door after finding the key?

---

## Recipe Card 5: Moving Enemy
### You need
- enemy sprite
- collision
- simple movement code

### Steps
1. Create an enemy scene.
2. Make it move left and right.
3. Reverse direction when it hits a point or timer.
4. If the player touches it, reset the player.

### Success check
- Does the enemy move?
- Does it create challenge?

---

## Recipe Card 6: Restart Button
### You need
- a `Button`
- a UI scene or label layer

### Steps
1. Add a button to the screen.
2. Set its text to **Restart**.
3. Connect the `pressed` signal.
4. Use:
   `get_tree().reload_current_scene()`

### Success check
- Can the player restart the game easily?
