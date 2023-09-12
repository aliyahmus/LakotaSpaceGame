# obj_player 
**Step Event**

```

if keyboard_check(vk_up)
{
		motion_add(image_angle, 0.1);	
}


if keyboard_check(vk_left)
{
		image_angle +=4;
}

if keyboard_check(vk_right)
{
		image_angle -=4;
}
move_wrap(true, true, 0)


if mouse_check_button_pressed(mb_left)
{
	instance_create_layer(x, y, "Instances", obj_bullet)
}
```

**Collision Event with obj_rock**

```
effect_create_above(ef_firework, x, y, 1, c_lime);
instance_destroy();
obj_game.alarm[0] = 120;

```

# obj_rock 

**Create Event**

```

speed = 1; 
direction = random(360);
image_angle = random (360); 

```

**Step Event**

```
move_wrap(true, true, 100);
image_angle += 1;

```

# obj_game

**Create Event**
```
points = 0;
```

**Alarm Event**

```
room_restart();
```

**Draq GUI**

```
draw_text(10, 10, points);
```

# obj_bullet

**Create Event**

```
speed = 10 
direction = obj_player.image_angle;
```
