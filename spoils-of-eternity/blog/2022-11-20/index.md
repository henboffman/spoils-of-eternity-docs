---
slug: November Update
title: November Update
# authors: [hoffchops]
tags: [update]
---

It seems that the direction of the game for v1 will be a single set of skills, one character class, and a number of passive skills that can modify how the game is played, which somewhat helps circumvent the need for multiple character classes. But, the skill tree needs to be usable, and not overly complicated, as the goal is primarily accessibility. 

1. Add passive skill tree
2. Capture and track unlocked passives
3. Add a few new movement skill mechanics

    a. Add leap skill

    b. Add lunge skill

4. Add enemy ability which applies DoT to area (which will force use of movement mechanic skill. Maybe this is undesirable if the player does not have control over movement)



## TODO For development purposes
1. DONE- Add combat arena scene to build and test 
2. Most of the player components require the CharacterManager. Maybe create a single PlayerDataManager that exists on the player, and all the player components can then reference the PlayerDataManager, which would contain the single reference point to the CharacterManager. This would also make it possible to move dependency away from the CharacterManager?
3. Swap the PlayerSkills around so that that class references the PlayerController. Currently, PlayerController references PlayerSkills
4. Maybe create a generic post skill action cooldown that active skills can set, instead of having the attack cooldown check each of the skills independently. In PlayerSkills, create an ActionSkillCooldown, and then each of the action skill scan set the actionSkillCooldown when the skill is used. 

## Questions/Decisions
1. Almost every ARPG on the app store is designed for landscape ratio. This is likely due to the movement/joystick layout. However, I don't want to force landscape layout. The more successful games seem to largely prioritize portrait controls, which I think encourages/appeals to a more casual audience. I suppose in typing this out/thinking through, I've convinced myself to stick with portrait format. Even if I do add movement mechanics, Ubisoft was able to pull it off with Mighty Quest (RIP)
2. Last Epoch provides a training dummy instead of raw DPS values/calculations. This does make it a bit more difficult to decide on upgrades, but encourages trial and error for builds vs. using whatever minmax strategy is the first result on youtube. Maybe the combat arena scene can act as a way to test a build. This would be a nice feature for users, but additional development. For now, will keep that possible use-case in mind while building out the arena (for design and debug purposes)