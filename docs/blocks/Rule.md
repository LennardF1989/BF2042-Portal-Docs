# Rule

RULE blocks are triggered from an in-game **EVENT**. When an **EVENT** triggers, this block will check if its **CONDITION** has been met and then execute all of the ACTIONS.

# Triggers

## Ongoing

Continually check if the **CONDITION** has become True. If no **CONDITION** has been provided the blocks in the Action section will always execute.

The Ongoing event can be ran in a Global, Team, or Player context. These are asyncronous and will run the entire context scope at the same time. IE: Running under the Player context will run the Action blocks for all players in the server at the same time.

### Global Context Outputs:
- None

### Team Context Outputs:
- **EventTeam** when the Experience gamemode is Team Deathmatch. FFA Experiences cannot use Team Context and will **NOT** run if configured.

### Player Context Outputs:
- **EventPlayer**

------------

## OnPlayerDied

This rule will execute action blocks when a Player dies. The type of death is irrelevant.

### Outputs
1. **EventPlayer** (Victim)
2. **EventOtherPlayer** (Killer)(Same as **EventPlayer** if suicide and ??? if unknown killer)

------------

## OnPlayerDeployed

This rule will execute when a player deploys regardless of side.

### Outputs
1. **EventPlayer**

------------

## OnPlayerJoinGame

This will execute when a player joins the server.

### Outputs
1. **EventPlayer**

------------

## OnPlayerLeaveGame

This will execute when a player leaves the server.

### Outputs
1. **EventPlayer**

------------

## OnPlayerEarnedKill

[comment]: # (Currently unknown if this gets triggered in Friendly Fire situations)

This will execute when a player earns a kill against another player.

### Outputs
1. **EventPlayer** (Killer)
2. **OtherEventPlayer** (Victim)

------------

## OnGameModeEnding

This will execute when the gamemode ends.

### Outputs
- None

------------

## OnMandown

[comment]: # (Currently unknown if this gets triggered when the down type ios "Crawl")

This will execute when a player enters the mandown state.

### Outputs
1. **EventPlayer** (Downed Player)

------------

## OnRevived

This will execute when a player is revived.

### Outputs
1. **EventPlayer** (Revived Player)
2. **OtherEventPlayer** (Savior)

------------

## OnTimeLimitReached

This will execute when the set timelimit for the gamemode reaches 0.

### Outputs
- None

------------

## OnGameModeStarted

[comment]: # (Currently unknown if this starts on the first player connecting or not)

This will execute when the gamemode starts.

### Outputs
- None

------------

## OnPlayerIrreversiblyDead

This will execute when a player goes dies and goes to the redeploy screen.

### Outputs
1. **EventPlayer**