# RULE

**RULE** blocks are triggered from an in-game **EVENT**. When an **EVENT** triggers, this block will check if its **CONDITION** has been met and then execute all of the **ACTIONS**.  
  
_In the following example, the **CONDITION** is checking when a Player earns a kill, whether their team has reached the target score, Then, the **ACTIONS** execute, which in this case, is ending the gamemode for the **Player** team's favor._

```blockly
<block type="ruleBlock">
	<mutation isOnGoingEvent="false"></mutation>
    <field name="EVENTTYPE">OnPlayerEarnedKill</field>
    <statement name="CONDITIONS">
        <block type="conditionBlock">
            <value name="CONDITION">
                <block type="Equals">
                    <value name="VALUE-0">
                        <block type="GetGamemodeScore">
							<value name="VALUE-0">
								<block type="GetTeamId">
									<value name="VALUE-0">
										<block type="EventPlayer"></block>
									</value>
								</block>
							</value>
						</block>
                    </value>
                    <value name="VALUE-1">
                        <block type="GetTargetScore" />
                    </value>
                </block>
            </value>
        </block>
    </statement>
	<statement name="ACTIONS">
        <block type="EndRound">
            <value name="VALUE-0">
                <block type="GetTeamId">
					<value name="VALUE-0">
						<block type="EventPlayer"></block>
					</value>
				</block>
            </value>
        </block>
    </statement>
</block>
```

### Types of **RULE** Blocks Events

#### Ongoing

Ongoing **EVENT** types continually check if its **CONDITION** has become _True_. If so, the **ACTIONS** will be executed once. In order for the **EVENT** to execute again, the **CONDITION** must become _False_ before becoming _True_ again. Ongoing **EVENT** types exist within the  Global, Player, and Team context. Within the Player and Team contexts, payload value blocks, such as EventPlayer and EventTeam, can be used to refer to the specific Player or Team within the **EVENT**. _Note: In FFA, Ongoing Team will not execute at all._

#### OnPlayerDied

This will trigger whenever a **Player** dies. _Payloads: EventPlayer (Victim), EventOtherPlayer (Killer)_

#### OnPlayerDeployed

This will trigger whenever a **Player** deploys. _Payloads: EventPlayer (Deployed Player)_

#### OnPlayerJoinGame

This will trigger when a **Player** joins the game. _Payloads: EventPlayer (Joined Player)_

#### OnPlayerLeaveGame

This will trigger when any player leaves the game.

#### OnPlayerEarnedKill

This will trigger when a **Player** earns a kill against another **Player**. _Payloads: EventPlayer (Killer), EventOtherPlayer (Victim)_

#### OnGameModeEnding

This will trigger when the gamemode ends.

#### OnMandown

This will trigger when a **Player** is forced into the mandown state. _Payloads: EventPlayer  (Downed Player)_

#### OnRevived

This will trigger when a **Player** is revived by another **Player**. _Payloads: EventPlayer (Revived Player), EventOtherPlayer (Reviver Player)_

#### OnTimeLimitReached

This will trigger when the gamemode time limit has been reached.

#### OnGameModeStarted

This will trigger at the start of the gamemode.

#### OnPlayerIrreversiblyDead

This will trigger when the **Player** dies and returns to the deploy screen. _Payloads: EventPlayer (Dead Player)_
