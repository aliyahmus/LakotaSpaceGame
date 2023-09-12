# obj_player 
**Step Event**

```

/// @description Insert description here
// You can write your code in this editor


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

/// @description Insert description here
// You can write your code in this editor
effect_create_above(ef_firework, x, y, 1, c_lime);
instance_destroy();
obj_game.alarm[0] = 120;

```

# obj_
