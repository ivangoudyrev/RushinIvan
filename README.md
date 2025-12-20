## Server Configuration
- Minecraft Paper
- [List plugins]

## Minecraft Multiverse Worlds
The Minecraft Server contains three worlds:
- Hub
- RushinIvan
- WorldB

### Hub  
The Hub is simply an initial landing place for all new players assigned to the "RushinIvan" and "Admin" user groups. The Hub is a peaceful 64x64-block world, without ability to break or place things. It's always daytime and weather is always sunny in the Hub.  

The Hub contains a spawning platform, where users will spawn initially, and portals to other worlds. Each portal is labeled with its destination; at this time there are only two: one portal leads to the RushinIvan world and the other portal leads to WorldB.

### RushinIvan
RushinIvan world is a copy the RushinIvan world from Minecraft Realms, and is open to players in the WorldA user group. The difficulty is set to hard, it has normal daylight and weather cycles.  
[insert world settings here]

### WorldB
WorldB is a regular world, open to all users.

## User Groups
The server contains three groups: 1) WorldA, 2) WorldB, and 3) Admin.

WorldA group contains all family members from the "Minecrafters" group chat.

WorldB group contains all other guests. 

Admin group is self-explanatory.

# The following commands are for world management
List all words: \
```/mv list``` \
Get information for a specific world: \
```/mv info [world_name]``` \
Set the world alias: \
```/mv modify [world_name] set alias [alias_name]``` \
Set the world to spawn animals or monsters \
```/mv entity-spawn-config modify [world_name] [animal/monster/etc.] set spawn [true/false]``` \
Freeze the world time or weather \
```/mv gamerule set minecraft:[advance_time/advance_weather] [true/false] [world_name]``` \
Set the world spawn point \
```/mvsetspawn [world_name]:[x],[y],[z]``` \
Set the center for the world border \
```/mv worldborder center [x] [z] [world_name]``` \
Set the world border \
```/mv worldborder set [radius] 0 [world_name]``` \

# The following commands are for player management
List all groups: \
```/lp listgroups```
