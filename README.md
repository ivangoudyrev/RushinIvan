## Server Configuration
- Minecraft Paper
- [List plugins]

## RushinIvan Server Overview
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
The server contains three groups: 
- WorldA: contains all family members from the "Minecrafters" group chat.
- WorldB: contains all other guests.
- Admin.

### User Management Commands
Users inherit permissions from the groups they are assigned to.  In other words, instead of assigning permissions to each user, we pre-assign permissions to the groups and then place users in them.

User permissions are managed using the LuckPerms plugin commands. The complete list of commands is available at https://luckperms.net/wiki/Command-Usage. The following are frequently used commands (note, each command must be prefaced by ```/``` in the game chat box, and Bedrock user named must be prefixed with ```.```):

- IMPORTANT!: After making changes to user permissions during a running game, you must run ```lp sync``` for permission changes to take effect.

- Add a new user to a user group, which gives them permission to access the worlds:  
Lookup the user's UUID at ```https://mcprofile.io/``` and insert it into the command below (use Floodgate UUID for Bedrock players):  
```lp user <UUID> parent add <group name>```

- Remove a user from the assigned user group. There is no need to look up the UUID again. You should be able to enter the user's name instead (add a ```.``` prefix for Bedrock players, like ```.rushinivan```):  
```lp user <user name> parent remove <group name>```

- Lookup user's information, including assigned groups:  
```lp user <user name> info```

- Lookup group's assigned permissions:  
```lp group <group name> permission info```

- Add permissions to a group:  
```lp group <group name> permission set <node> <true/false> [context...]```    
There are many nodes that represent different permissions. For example, a node ```luckperms.*``` is used to allow access to all LuckPerms commands.  Setting the value to ```true``` grants the permission and ```false``` explicitly denies it. See permissions below for the full list of nodes.

- Remove permissions from a group:  
```lp group <group name> permission unset <node> [context...]```

- Lookup user's assigned permissions (Note: our policy is to assign permissions to groups, not individual users, so this command should not produce any results. Use this command only as a test or an exception to the rule):  
```lp user <user name> permission info```

- Add permissions to a user:  
```lp user <user name> permission set <node> <true/false> [context...]```    

- Remove permissions from a user:  
```lp user <user name> permission unset <node> [context...]```

- List user groups on the server:  
```lp listgroups```

- List users assigned to the user group:  
```lp group <group name> listmembers```

- Rename a user group:  
```lp group <group name> rename <new group name>```

### World Management Commands
The Multiverse plugins, installed in this server, allow us to combine multiple worlds into a multiverse of connected worlds. The Multiverse-Core plugin controls mob spawning, environment type and other functions. The Multiverse-Portals plugin allows us to create portals for users to easily move between worlds. The Multiverse-NetherPortals plugin allows us to customize how different worlds integrate with their Nether sub-worlds. The following sections provide basic commands for these plugins. Please refer to the plugin wiki pages for a full list of commands:  
- https://github.com/Multiverse/Multiverse-Core/wiki/Command-Reference
- https://github.com/Multiverse/Multiverse-Core/wiki/Command-Reference-%28Portals%29
- https://github.com/Multiverse/Multiverse-Core/wiki/Command-Reference-(NetherPortals)

### Permissions


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
