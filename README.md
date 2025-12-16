# Server Configuration
The server contains three worlds: 1) Hub, 2) WorldA, and 3) WorldB. 

The Hub is simply a landing place for all new players assigned to the WorldA and Admin groups. The Hub is a 64x64 block world without ability to break or place things. 

WorldA is a copy the RushinIvan world from the Realms. Only approved family members are allowed into this world by being assigned to group WorldA. 

WorldB is a regular world. Only approved friends are allowed into this world and all family members within GroupA.

# Groups
The server contains three groups: 1) WorldA, 2) WorldB, and 3) Admin.

WorldA group contains all family members from the "Minecrafters" group chat.

WorldB group contains all other guests and aqcuiaintances. 

Admin group is self-explanatory.

# The following commands are for world management
List all words\n
```mv list```
Get information for a specific world
```/mv info [world_name]```

Set the world alias
```/mv modify [world_name] set alias [alias_name]```

Set the world to spawn animals or monsters
```/mv entity-spawn-config modify [world_name] [animal/monster/etc.] set spawn [true/false]```

Freeze the world time or weather
```/mv gamerule set minecraft:[advance_time/advance_weather] [true/false] [world_name]```

Set the world spawn point
```/mvsetspawn [world_name]:[x],[y],[z]```

Set the center for the world border
```/mv worldborder center [x] [z] [world_name]```

Set the world border
```/mv worldborder set [radius] 0 [world_name]```
