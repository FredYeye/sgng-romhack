# Commentary on changes

## General

### Use fastrom to reduce slowdown
Super Ghouls is an early SNES title and thus uses the slower ROM access mode. Changing it to FastROM removes much of the slowdown.

### Pot system now works across stages instead of resetting on stage start
It's hard to say if this was an oversight or intentional. This now works the same way the previous entry (Ghouls 'n Ghosts) worked. Be on the lookout for the 1-up drop!

### Restore the shell peeking animation (and adjust waiting times to compensate)
An unused animation for the shell. Possibly cut for taking to much time.

## Stage 2

### Speed up raft section: 200s -> 177s
The raft section could feel very punishing if you had to retry it many times since it's so long.

## Difficulty

### Change beginner loop 2 difficulty: expert -> normal
A cruel joke played by the devs or simply an oversight? This tunes down beginner's loop 2 to normal difficulty, in any case.

## HP adjustments
Todo

## Weapons
While not all weapons need to be equally well performing, many weapons are simply too difficult to use for the average player: if you get a particularly gnarly weapon it's common to just die over and over to open an early chest for a new weapon. I'd love to hear about the design decisions going into the weapons...

### Bracelet
* Projectile is slightly taller (8px -> 10px)
* Decay rate updated: [6f, 7f, 7f, 8f] -> [8f, 8f, 8f, 9f]
The bracelet gradually powers up as you get better armors, but getting hit still takes you back down to zero making it very weak. The decay rate change makes it travel and retain power a little bit longer.

### Lance, level 2:
* Projectile limit: 1 -> 2 (also reduce fire trails to prevent sprite dropouts)
* Base damage: 9 -> 8
The upgraded lance can only have one projectile on screen at a time. This often makes it worse than the base lance! Maybe it was done so the fire trail VFX wouldn't slow down the game / cause flickering sprites? This makes the lance a solid choice.

### Axe, level 2:
* Spawns a bit more forward to prevent hitting walls behind arthur
* Lower upwards trajectory so it travels forward faster (time: 32f -> 21f)
The axe is, simply put, a strange weapon. The upgraded axe gains the piercing property which maybe sounds good but is actually quite bad! If you didn't kill the enemy in front of you, you'll have to wait for the axe to awkwardly exit the screen before shooting again. These changes makes the axe collide less often in tight quarters.

### Scythe, level 2:
* Swipe count: 3 -> 2
Similar to the axe, the scythe is very slow. This shortens the hit animation so you can fire another scythe quicker.
