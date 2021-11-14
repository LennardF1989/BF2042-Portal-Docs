# Abort

Stops the execution of a list of **ACTIONS** in a **RULE**.

```blockly
<block type="ruleBlock">
    <mutation isOnGoingEvent="false"></mutation>
    <field name="NAME">New Rule</field>
    <field name="EVENTTYPE">OnPlayerEarnedKill</field>
    <statement name="CONDITIONS"></statement>
    <statement name="ACTIONS">
        <block type="If">
            <mutation></mutation>
            <value name="VALUE-0">
                <block type="Equals">
                    <value name="VALUE-0">
                        <block type="GetTeamId">
                            <value name="VALUE-0">
                                <block type="EventPlayer"></block>
                            </value>
                        </block>
                    </value>
                    <value name="VALUE-1">
                        <block type="GetTeamId">
                            <value name="VALUE-0">
                                <block type="Number">
                                    <field name="NUM">1</field>
                                </block>
                            </value>
                        </block>
                    </value>
                </block>
            </value>
            <statement name="DO">
                <block type="Abort"></block>
            </statement>
        </block>
    </statement>
</block>
```

# AbortIf

Stops the execution of a list of **ACTIONS** in a **RULE** if the provided **Bool** is _True_. Otherwise, the execution continues with the remaining **ACTIONS**.

### Inputs

1. Bool

```blockly
<block type="ruleBlock">
    <mutation isOnGoingEvent="false"></mutation>
    <field name="NAME">New Rule</field>
    <field name="EVENTTYPE">OnPlayerEarnedKill</field>
    <statement name="CONDITIONS"></statement>
    <statement name="ACTIONS">
        <block type="AbortIf">
            <value name="VALUE-0">
                <block type="Equals">
                    <value name="VALUE-0">
                        <block type="GetTeamId">
                            <value name="VALUE-0">
                                <block type="EventPlayer"></block>
                            </value>
                        </block>
                    </value>
                    <value name="VALUE-1">
                        <block type="GetTeamId">
                            <value name="VALUE-0">
                                <block type="Number">
                                    <field name="NUM">1</field>
                                </block>
                            </value>
                        </block>
                    </value>
                </block>
            </value>
        </block>
    </statement>
</block>
```

# AbsoluteValue

Returns the unsigned value of the provided **Number** input.

### Inputs

1. Number

### Output

-   Number

```blockly
<block type="AbsoluteValue">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">-5</field>
        </block>
    </value>
</block>
```

# Add

Returns the sum of two **Number** or two **Vector** values.

### Inputs

1. Number | Vector
2. Number | Vector

### Output

-   Number | Vector

```blockly
<block type="Add">
    <value name="VALUE-0">
       <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">1</field>
        </block>
    </value>
</block>
```

# And

Returns a **Bool** value based on whether both of the provided inputs return _True_.

### Inputs

1. Bool
2. Bool

### Output

-   Bool

```blockly
<block type="And">
    <value name="VALUE-0">
        <block type="GreaterThan">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="LessThan">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">4</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# AngleDifference

Returns the difference between two angles (in degrees).

### Inputs

1. Number

    (1st Angle)

2. Number

    (2nd Angle)

### Output

-   Number

```blockly
<block type="AngleDifference">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">180</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">270</field>
        </block>
    </value>
</block>
```

# AppendToArray

Returns a copy of an **Array** with the provided value appended to the end.

### Inputs

1. Array
2. Any Type

### Output

-   Array

```blockly
<block type="AppendToArray">
    <value name="VALUE-0">
        <block type="EmptyArray"></block>
    </value>
    <value name="VALUE-1">
        <block type="EventOtherPlayer"></block>
    </value>
</block>
```

# ApplyMedGadget

Applies the effect of a medical gadget to a target **Player**.

### Inputs

1. Player
2. MedGadgetTypesItem

```blockly
<block type="ApplyMedGadget">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="MedGadgetTypesItem">
            <field name="VALUE-0">MedGadgetTypes</field>
            <field name="VALUE-1">MedicCrate</field>
        </block>
    </value>
</block>
```

# ArraySlice

Returns a copy of the specified **Array** containing only values from a specified index range.

### Inputs

1. Array

2. Number

    (Start Index)

3. Number

    (Count)

### Output

-   Array

```blockly
<block type="ArraySlice">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">2</field>
        </block>
    </value>
</block>
```

# BackwardVector

Returns the backward directional **Vector** of (0, 0, 1).

### Output

-   Vector

```blockly
<block type="BackwardVector"></block>
```

# Break

Breaks and exits the execution of a looping block, such as While or LoopVariable.

```blockly
<block type="While">
    <value name="VALUE-0">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
    <statement name="DO">
        <block type="Wait">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
            <next>
                <block type="Break"></block>
            </next>
        </block>
    </statement>
</block>
```

# %{PYRITE_SUBROUTINE}

%{help.subroutineinstance.summary}

```
<block type="subroutineInstanceBlock">
    <field name="SUBROUTINE_NAME">Subroutine</field>
</block>
```

# ClearAllCustomMessages

Clears all custom messages for a provided **Player** or **TeamId**. If no **Player** or **TeamId** is provided, it will clear all custom messages for everyone.

### Inputs

1. Player | TeamId

    (Group)

    _Optional_

```blockly
<block type="ClearAllCustomNotificationMessages">
    <value name="VALUE-0">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# ClearCustomMessage

Clears text from the provided **CustomMessageSlotsItem** for the provided **Player** or **TeamId**. If no **Player** or **TeamId** is given, it clears all players text at that **CustomMessageSlotsItem**.

### Inputs

1. CustomMessageSlotsItem
2. Player | TeamId

    (Group)

    _Optional_

```blockly
<block type="ClearCustomNotificationMessage">
    <value name="VALUE-0">
        <block type="CustomMessagesItem">
            <field name="VALUE-0">CustomMessages</field>
            <field name="VALUE-1">MessageText3</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# ClosestPlayerTo

Returns the closest **Player** to a position in the world. Can be filtered using a **TeamId**.

### Inputs

1. Vector

    (Position)

2. TeamId

    _Optional_

### Output

-   Player

```blockly
<block type="ClosestPlayerTo">
    <value name="VALUE-0">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# %{PYRITE_CONDITION}

%{help.condition.summary}

### %{help.common.input}

1. %{PYRITE_TYPE_BOOLEAN}

```
<block type="ruleBlock">
    <mutation isOnGoingEvent="false"></mutation>
    <field name="NAME">New Rule</field>
    <field name="EVENTTYPE">OnPlayerEarnedKill</field>
    <statement name="CONDITIONS">
        <block type="conditionBlock">
            <value name="CONDITION">
                <block type="Equals">
                    <value name="VALUE-0">
                        <block type="GetTeamId">
                            <value name="VALUE-0">
                                <block type="EventPlayer"></block>
                            </value>
                        </block>
                    </value>
                    <value name="VALUE-1">
                        <block type="GetTeamId">
                            <value name="VALUE-0">
                                <block type="Number">
                                    <field name="NUM">1</field>
                                </block>
                            </value>
                        </block>
                    </value>
                </block>
            </value>
        </block>
    </statement>
    <statement name="ACTIONS">
        <block type="SetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="Add">
                    <value name="VALUE-0">
                        <block type="GetGamemodeScore">
                            <value name="VALUE-0">
                                <block type="EventPlayer"></block>
                            </value>
                        </block>
                    </value>
                    <value name="VALUE-1">
                        <block type="Number">npm start
                            <field name="NUM">1</field>
                        </block>
                    </value>
                </block>
            </value>
        </block>
    </statement>
</block>
```

# Continue

Forces the execution of a looping block (such as While or LoopVariable) to the start of the next iteration of that block.

```blockly
<block type="Continue"></block>
```

# CosineFromDegrees

Returns the cosine value of a specified angle in degrees.

### Inputs

1. Number

### Output

-   Number

```blockly
<block type="CosineFromDegrees">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">180</field>
        </block>
    </value>
</block>
```

# CosineFromRadians

Returns the cosine value of a specified angle in radians.

### Inputs

1. Number

### Output

-   Number

```blockly
<block type="CosineFromRadians">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">3.14</field>
        </block>
    </value>
</block>
```

# CountOf

Returns the **Number** of elements in the specified **Array**.

### Inputs

1. Array

### Output

-   Number

```blockly
<block type="CountOf">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
</block>
```

# CreateVector

Returns a **Vector** composed of three provided \'X\' (left), \'Y\' (up), and \'Z\' (forward) values.

### Inputs

1. Number

    (X Value)

2. Number

    (Y Value)

3. Number

    (Z Value)

### Output

-   Vector

```blockly
<block type="CreateVector">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">3</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">5</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">6</field>
        </block>
    </value>
</block>
```

# CrossProduct

Returns the cross product between two **Vector** values. If the two **Vector** inputs are parallel, the result will be zero.

### Inputs

1. Vector
2. Vector

### Output

-   Vector

```blockly
<block type="CrossProduct">
    <value name="VALUE-0">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">3</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">5</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">6</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="ForwardVector">
        </block>
    </value>
</block>
```

# CurrentArrayElement

Returns a reference to the current **Array** element being evaluated. Only used for FilteredArray, MappedArray, SortedArray, IsTrueForAll, and IsTrueForAny.

### Output

-   Any Type

```blockly
<block type="FilteredArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="Number">
                            <field name="NUM">1</field>
                        </block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="CurrentArrayElement"></block>
                    </value>
                </block>
            </value>
        </block>
    </value>
</block>
```

# CustomMessageSlot

Returns a **CustomMessageSlotsItem** which can be used with DisplayCustomMessage and ClearCustomMessage to display information on screen to players.

### Output

-   CustomMessageSlotsItem

```blockly
<block type="CustomMessagesItem">
    <field name="VALUE-0">CustomMessages</field>
    <field name="VALUE-1">MessageText1</field>
</block>
```

# DealDamage

Sets an amount of damage to be applied to a target **Player** by a giver **Player**.

### Inputs

1. Player

    (Target)

2. Number
3. Player

    (Giver)

    _Optional_

```blockly
<block type="SetPlayerDamage">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">25</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="EventOtherPlayer"></block>
    </value>
</block>
```

# DirectionFromAngles

Returns a directional **Vector** from the provided horizontal (yaw) and vertical (pitch) angles (in degrees).

### Inputs

1. Number (Horizontal)
2. Number (Vertical)

### Output

-   Vector

```blockly
<block type="DirectionFromAngles">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">90</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">130</field>
        </block>
    </value>
</block>
```

# DirectionTowards

Returns the direction, or normalized **Vector**, from a starting position and ending position.

### Inputs

1. Vector

    (Starting Position)

2. Vector

    (Ending Position)

### Output

-   Vector

```blockly
<block type="DirectionTowards">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateVectorItem">
                    <field name="VALUE-0">SoldierStateVector</field>
                    <field name="VALUE-1">GetPosition</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# DisplayCustomMessage

Display a **Message** on-screen exclusive to custom gamemodes. Using the **CustomMessageSlotsItem**, this **Message** can be displayed on multiple lines. It will stay up for the length of the provided duration, or stay up indefinitely if a negative **Number** is provided. It will be displayed to everyone unless a specific **Player** or **TeamId** is provided.  
  
_Note: It\'s your responsibility to ensure a safe and fair experience for others, violating the EA User Agreement by using offensive or inappropriate text may result in account bans._

### Inputs

1. Message
2. CustomMessageSlotsItem
3. Number

    (Duration)

4. Player | TeamId

    (Group)

    _Optional_

```blockly
<block type="DisplayCustomNotificationMessage">
    <value name="VALUE-0">
        <block type="Message">
            <value name="VALUE-0">
                <block type="Text">
                    <field name="TEXT">This is a Custom Message!</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="CustomMessagesItem">
            <field name="VALUE-0">CustomMessages</field>
            <field name="VALUE-1">HeaderText</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">-1</field>
        </block>
    </value>
    <value name="VALUE-3">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# DisplayGameModeMessage

Displays a **Message** on the screen for 6 seconds. If no target is provided, the **Message** will display to everyone.  
  
_Note: This will only appear to players that are deployed on the map. It\'s your responsibility to ensure a safe and fair experience for others, violating the EA User Agreement by using offensive or inappropriate text may result in account bans._

### Inputs

1. Message
2. Player | TeamId

    _Optional_

```blockly
<block type="ShowEventGameModeMessage">
    <value name="VALUE-0">
        <block type="Message">
            <value name="VALUE-0">
                <block type="Text">
                    <field name="TEXT">Hello World!</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# DisplayHighlightedWorldLogMessage

Displays a **Message** on the world log for 6 seconds. If no target is provided, it will display the **Message** to everyone.  
  
_Note: This will only appear to players that are deployed on the map. It\'s your responsibility to ensure a safe and fair experience for others, violating the EA User Agreement by using offensive or inappropriate text may result in account bans._

### Inputs

1. Message
2. Player | TeamId

    _Optional_

```blockly
<block type="ShowHighlightedGameModeMessage">
    <value name="VALUE-0">
        <block type="Message">
            <value name="VALUE-0">
                <block type="Text">
                    <field name="TEXT">Hello World!</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="EventTeam"></block>
    </value>
</block>
```

# DisplayCustomMessage

Displays a notification-type **Message** on the screen for 6 seconds. If no target is provided, it will display the **Message** to everyone.  
  
_Note: It\'s your responsibility to ensure a safe and fair experience for others, violating the EA User Agreement by using offensive or inappropriate text may result in account bans._

### Inputs

1. Message
2. Player | TeamId

    _Optional_

```blockly
<block type="ShowNotificationMessage">
    <value name="VALUE-0">
        <block type="Message">
            <value name="VALUE-0">
                <block type="Text">
                    <field name="TEXT">Hello World!</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# DistanceBetween

Returns the distance between a starting position and ending position.

### Inputs

1. Vector

    (Starting Position)

2. Vector

    (Ending Position)

### Output

-   Number

```blockly
<block type="DistanceBetween">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateVectorItem">
                    <field name="VALUE-0">SoldierStateVector</field>
                    <field name="VALUE-1">GetPosition</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# Divide

Returns the ratio between two **Number** values or a **Vector** and **Number** value. A **Vector** divided by a **Number** will yield a scaled **Vector**.

### Inputs

1. Number | Vector
2. Number

### Output

-   Number | Vector

```blockly
<block type="Divide">
    <value name="VALUE-0">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
</block>
```

# DotProduct

Returns the dot product between two **Vector** values. If the two values are orthogonal to each other, the result will be zero.

### Inputs

1. Vector
2. Vector

### Output

-   Number

```blockly
<block type="DotProduct">
    <value name="VALUE-0">
        <block type="LocalVectorOf">
            <value name="VALUE-0">
                <block type="ForwardVector"></block>
            </value>
            <value name="VALUE-1">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="LocalVectorOf">
            <value name="VALUE-0">
                <block type="ForwardVector"></block>
            </value>
            <value name="VALUE-1">
                <block type="EventOtherPlayer"></block>
            </value>
        </block>
    </value>
</block>
```

# DownVector

Returns the downward directional **Vector** of (0, -1, 0).

### Output

-   Vector

```blockly
<block type="DownVector"></block>
```

# EmptyArray

Returns an initialized empty **Array**.

### Output

-   Array

```blockly
<block type="AppendToArray">
    <value name="VALUE-0">
        <block type="EmptyArray"></block>
    </value>
    <value name="VALUE-1">
        <block type="EventOtherPlayer"></block>
    </value>
</block>
```

# EnableAllInputRestrictions

Enables or disables all available input restrictions for a target **Player**.

### Inputs

1. Player
2. Bool

```blockly
<block type="EnableAllInputRestrictions">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
</block>
```

# EnableAllPlayerDeploy

Enables or disables spawning from the deploy screen for all players.

### Inputs

1. Bool

```blockly
<block type="EnablePlayerSpawning">
    <value name="VALUE-0">
        <block type="Boolean">
            <field name="BOOL">FALSE</field>
        </block>
    </value>
</block>
```

# EnableDefaultGameModeScoring

Enables or disables default gamemode scoring logic. The default scoring logic refers to the base gamemode scoring rules (such as getting kills in Team Deathmatch or Free-for-All). Disable this if you want to implement your own custom scoring logic.

### Inputs

1. Bool

```blockly
<block type="EnableDefaultScoring">
    <value name="VALUE-0">
        <block type="Boolean">
            <field name="BOOL">FALSE</field>
        </block>
    </value>
</block>
```

# EnableDefaultGameModeWinCondition

Enables or disables the gamemode\'s default win condition logic. The win condition is checked when the time limit is reached or when a team or player reaches the target score. Disable this if you want to trigger your own win condition.

### Inputs

1. Bool

```blockly
<block type="EnableDefaultWinCondition">
    <value name="VALUE-0">
        <block type="Boolean">
            <field name="BOOL">FALSE</field>
        </block>
    </value>
</block>
```

# EnableInputRestriction

Enables or disables a specified **InputRestrictionsItem** on a target **Player**.

### Inputs

1. Player
2. InputRestrictionsItem
3. Bool

```blockly
<block type="EnableInputRestriction">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="RestrictedInputsItem">
            <field name="VALUE-0">RestrictedInputs</field>
            <field name="VALUE-1">FireWeapon</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
</block>
```

# EnablePlayerDeploy

Enables or disables the ability for a target **Player** to deploy.

### Inputs

1. Player
2. Bool

```blockly
<block type="SetSpawnOverride">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Boolean">
            <field name="BOOL">FALSE</field>
        </block>
    </value>
</block>
```

# EnableVOMessaging

Enables or disables the gamemode VO messaging.

### Inputs

1. Bool

```blockly
<block type="EnableVOMessaging">
    <value name="VALUE-0">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
</block>
```

# EndGameMode

Ends the current gamemode and designates the provided **Player** or **TeamId**. The gamemode ends in draw if TeamId is set to 0.

### Inputs

1. TeamId | Player

```blockly
<block type="EndRound">
    <value name="VALUE-0">
            <block type="GetTeamId">
                <value name="VALUE-0">
                    <block type="Number">
                        <field name="NUM">0</field>
                    </block>
                </value>
            </block>
    </value>
</block>
```

# Equals

Returns a **Bool** indicating if two values are equal to each other.

### Inputs

1. Any Type
2. Any Type

### Output

-   Bool

```blockly
<block type="Equals">
    <value name="VALUE-0">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# EventOtherPlayer

Returns the 2nd **Player** payload from the **RULE** **EVENT** context.

### Output

-   Player

```blockly
<block type="GetTeamId">
    <value name="VALUE-0">
        <block type="EventOtherPlayer"></block>
    </value>
</block>
```

# EventPlayer

Returns the 1st **Player** payload from the **RULE** **EVENT** context.

### Output

-   Player

```blockly
<block type="GetTeamId">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# EventTeam

Returns the **TeamId** payload from the Ongoing Team ****EVENT**** context.

### Output

-   TeamId

```blockly
<block type="FilteredArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="EventTeam"></block>
            </value>
            <value name="VALUE-1">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="CurrentArrayElement"></block>
                    </value>
                </block>
            </value>
        </block>
    </value>
</block>
```

# Factions

Returns a **FactionsItem** from the collection of all available factions.

### Output

-   FactionsItem

```blockly
<block type="FactionsItem">
    <field name="VALUE-0">Factions</field>
    <field name="VALUE-1">Grafton_UK</field>
</block>
```

# Farthest Player From

Returns the farthest **Player** from a position. Can be filtered using a **TeamId**.

### Inputs

1. Vector

    (Position)

2. TeamId

    _Optional_

### Output

-   Player

```blockly
<block type="FarthestPlayerFrom">
    <value name="VALUE-0">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">2</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# FilteredArray

Returns a filtered version of the specified **Array** based on the condition provided. This block cycles through the entire array. You can utilize the CurrentArrayElement block to represent the element in the **Array** for each iteration. For an **Array** like GetPlayers, CurrentArrayElement would represent each **Player** in that **Array**. You can then build your filter condition based on a property of that **Player** (like score, or some custom player **Variable** value).

### Inputs

1. Array
2. Any Type

### Output

-   Array

```blockly
<block type="FilteredArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="Number">
                            <field name="NUM">1</field>
                        </block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="CurrentArrayElement"></block>
                    </value>
                </block>
            </value>
        </block>
    </value>
</block>
```

# FirstOf

Returns the first value of the specified **Array**.

### Inputs

1. Array

### Output

-   Any Type

```blockly
<block type="FirstOf">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
</block>
```

# ForceDeployAllPlayers

Force spawns all players in the deploy screen.

```blockly
<block type="ForceSpawnAllPlayers"></block>
```

# ForceMandown

Puts the target **Player** into the mandown state (unless mandown is disabled).

### Inputs

1. Player

```blockly
<block type="ForceManDown">
    <value name="VALUE-0">
        <block type="EventOtherPlayer"></block>
    </value>
</block>
```

# ForceRevive

Revives a target **Player** that is in the mandown state.

### Inputs

1. Player

```blockly
<block type="ForceRevive">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# ForceSwitchInventory

Forces the target **Player** to switch to the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem

```blockly
<block type="ForceSwitchInventory">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="InventorySlotsItem">
            <field name="VALUE-0">InventorySlots</field>
            <field name="VALUE-1">SecondaryWeapon</field>
        </block>
    </value>
</block>
```

# ForwardVector

Returns the forward directional **Vector** of (0, 0, -1).

### Output

-   Vector

```blockly
<block type="ForwardVector"></block>
```

# GetGameModeScore

Returns the current gamemode score of the provided **Player** or **TeamId**.

### Inputs

1. Player | TeamId

### Output

-   Number

```blockly
<block type="GetGamemodeScore">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# GetGameModeTargetScore

Returns the gamemode target score needed for victory.

### Output

-   Number

```blockly
<block type="GetTargetScore"></block>
```

# GetGameModeTimeLimit

Returns the time limit set for the gamemode (in seconds).

### Output

-   Number

```blockly
<block type="GetRoundTime"></block>
```

# GetGameModeTimeRemaining

Returns the amount of time left (seconds) in the current gamemode.

### Output

-   Number

```blockly
<block type="GetMatchTimeElapsed"></block>
```

# GetInventoryAmmo

Returns the target **Player** loaded ammo of the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem

### Output

-   Number

```blockly
<block type="GetInventoryAmmo">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="InventorySlotsItem">
            <field name="VALUE-0">InventorySlots</field>
            <field name="VALUE-1">SecondaryWeapon</field>
        </block>
    </value>
</block>
```

# GetInventoryMagazineAmmo

Returns the target **Player** magazine ammo of the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem

### Output

-   Number

```blockly
<block type="GetInventoryMagazineAmmo">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="InventorySlotsItem">
            <field name="VALUE-0">InventorySlots</field>
            <field name="VALUE-1">PrimaryWeapon</field>
        </block>
    </value>
</block>
```

# GetPlayerDeaths

Returns the total amount of deaths for the target **Player**.

### Inputs

1. Player

### Output

-   Number

```blockly
<block type="GetPlayerDeaths">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# GetPlayerKills

Returns the total amount of kills for the target **Player**.

### Inputs

1. Player

### Output

-   Number

```blockly
<block type="GetPlayerKills">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# GetPlayers

Returns an **Array** of all players within a game.

### Output

-   Array

```blockly
<block type="AllPlayers"></block>
```

# GetPlayerState

Returns the value of the target **Player** state.

### Inputs

1. Player
2. PlayerStateBoolItem | PlayerStateNumberItem | PlayerStateVectorItem

### Output

-   Bool | Number | Vector

```blockly
<block type="GetSoldierState">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
        <value name="VALUE-1">
        <block type="SoldierStateBoolItem">
            <field name="VALUE-0">SoldierStateBool</field>
            <field name="VALUE-1">IsAISoldier</field>
        </block>
    </value>
</block>
```

# GetTeamId

Returns the **TeamId** value of the specified **Player** OR the corresponding **TeamId** of the provided **Number**.

### Inputs

1. Player | Number

### Output

-   TeamId

```blockly
<block type="GetTeamId">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# GetVariable

Returns the value of a **Variable**.

### Inputs

1. Variable

### Output

-   Any Type

```blockly
<block type="GetVariable"></block>
```

# GetXComponent

Returns the \'X\' component of a provided **Vector**.

### Inputs

1. Vector

### Output

-   Number

```blockly
<block type="XComponentOf">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateVectorItem">
                    <field name="VALUE-0">SoldierStateVector</field>
                    <field name="VALUE-1">GetPosition</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# GetZComponent

Returns the \'Y\' component of a provided **Vector**.

### Inputs

1. Vector

### Output

-   Number

```blockly
<block type="YComponentOf">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateVectorItem">
                    <field name="VALUE-0">SoldierStateVector</field>
                    <field name="VALUE-1">GetPosition</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# Get Z Component

Returns the \'Z\' component of a provided **Vector**.

### Inputs

1. Vector

### Output

-   Number

```blockly
<block type="ZComponentOf">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateVectorItem">
                    <field name="VALUE-0">SoldierStateVector</field>
                    <field name="VALUE-1">GetPosition</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# GreaterThan

Returns a **Bool** indicating if the 1st provided value is greater than the 2nd provided value.

### Inputs

1. Number
2. Number

### Output

-   Bool

```blockly
<block type="GreaterThan">
    <value name="VALUE-0">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
</block>
```

# GreaterThanEqualTo

Returns a **Bool** indicating if the 1st provided value is greater than the 2nd provided value.

### Inputs

1. Number
2. Number

### Output

-   Bool

```blockly
<block type="GreaterThanEqualTo">
    <value name="VALUE-0">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="GetTargetScore"></block>
    </value>
</block>
```

# HasInventory

Returns a **Bool** indicating if the provided **Player** has the specified ability.

### Inputs

1. Player
2. InventoryPrimaryWeaponsItem | InventorySecondaryWeaponsItem | InventoryCharacterSpecialtiesItem | InventoryOpenGadgetsItem | InventoryThrowablesItem | InventoryMeleeWeaponsItem

### Output

-   Bool

```blockly
<block type="HasInventory">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="PrimaryWeaponsItem">
            <field name="VALUE-0">PrimaryWeaponsKingston</field>
            <field name="VALUE-1">SLX Spear</field>
        </block>
    </value>
</block>
```

# Heal

Sets the amount of health gained in an instant for a target **Player** applied by a healer **Player**.

### Inputs

1. Player

    (Target)

2. Number
3. Player

    (Healer)

    _Optional_

```blockly
<block type="SetHeal">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">50</field>
        </block>
    </value>
</block>
```

# If

A special block which evaluates conditions to control the flow of **ACTIONS** in the If, Else If, and Else branches.

```blockly
<block type="If">
    <mutation elseif="1" else="1"></mutation>
    <value name="VALUE-0">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="Number">
                            <field name="NUM">1</field>
                        </block>
                    </value>
                </block>
            </value>
        </block>
    </value>
    <statement name="DO"></statement>
    <value name="IF1">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="Number">
                            <field name="NUM">2</field>
                        </block>
                    </value>
                </block>
            </value>
        </block>
    </value>
    <statement name="DO1"></statement>
    <statement name="ELSE"></statement>
</block>
```

# IfThenElse

Returns the 1st provided value if the condition is _True_, otherwise, returns the 2nd provided value.

### Inputs

1. Bool
2. Any Type

    (Output Value if the Condition is _True_)

3. Any Type

    (Output Value if the Condition is _False_)

### Output

-   Any Type

```blockly
<block type="IfThenElse">
    <value name="VALUE-0">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="Number">
                            <field name="NUM">1</field>
                        </block>
                    </value>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
</block>
```


# InputRestrictions

Returns a **InputRestrictionsItem** from the collection of all inputs which can be restricted with EnableInputRestriction.

### Output

-   InputRestrictionsItem

```blockly
<block type="RestrictedInputsItem">
    <field name="VALUE-0">RestrictedInputs</field>
    <field name="VALUE-1">SelectMelee</field>
</block>
```

# InventoryCharacterSpecialties

Returns a **InventoryCharacterSpecialtiesItem** from the collection of all character specialties.

### Output

-   InventoryCharacterSpecialtiesItem

```blockly
<block type="CharacterGadgetsItem">
    <field name="VALUE-0">CharacterGadgetsAlexandria</field>
    <field name="VALUE-1">RepairTool_ALX</field>
</block>
```

# InventoryMeleeWeapons

Returns an **InventoryMeleeWeaponsItem** from the collection of all melee weapons.

### Output

-   InventoryMeleeWeaponsItem

```blockly
<block type="MeleeWeaponsItem">
    <field name="VALUE-0">MeleeRumney</field>
    <field name="VALUE-1">Knife_BC2</field>
</block>
```

# InventoryOpenGadgets

Returns an **InventoryOpenGadgetsItem** from the collection of all open gadgets.

### Output

-   InventoryOpenGadgetsItem

```blockly
<block type="OpenGadgetsItem">
    <field name="VALUE-0">OpenGadgetsRumney</field>
    <field name="VALUE-1">RPG7_RUM</field>
</block>
```

# InventoryPrimaryWeapons

Returns an **InventoryPrimaryWeaponsItem** from the collection of all primary weapons.

### Output

-   InventoryPrimaryWeaponsItem

```blockly
<block type="PrimaryWeaponsItem">
    <field name="VALUE-0">PrimaryWeaponsKingston</field>
    <field name="VALUE-1">Keltec</field>
</block>
```

# InventorySecondaryWeapons

Returns an **InventorySecondaryWeaponsItem** from the collection of all secondary weapons.

### Output

-   InventorySecondaryWeaponsItem

```blockly
<block type="SecondaryWeaponsItem">
    <field name="VALUE-0">SecondaryWeaponsAlexandria</field>
    <field name="VALUE-1">M1911_ALX</field>
</block>
```

# InventoryThrowables

Returns an **InventoryThrowablesItem** from the collection of all throwables.

### Output

-   [Unknown: PYRITE_TYPE_THORWABLESITEMINDEX]

```blockly
<block type="ThrowablesItem">
    <field name="VALUE-0">ThrowablesKingston</field>
    <field name="VALUE-1">SmokeGrenade</field>
</block>
```

# IsFaction

Returns _True_ whether or not the provided **TeamId** is using soldiers from the provided **FactionsItem**.

### Inputs

1. TeamId
2. FactionsItem

```blockly
<block type="IsFaction">
    <value name="VALUE-0">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="FactionsItem">
            <field name="VALUE-0">Factions</field>
            <field name="VALUE-1">Grafton_GER</field>
        </block>
    </value>
</block>
```

# IsInventorySlotActive

Returns _True_ whether or not the active inventory slot of the target **Player** is the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem

### Output

-   Bool

```blockly
<block type="IsInventorySlotActive">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="InventorySlotsItem">
            <field name="VALUE-0">InventorySlots</field>
            <field name="VALUE-1">SecondaryWeapon</field>
        </block>
    </value>
</block>
```

# IsPlayerUsingSoldier

Returns a **Bool** indicating if the target **Player** is a specified **PlayerSoldiersItem**.

### Inputs

1. Player
2. PlayerSoldiersItem

```blockly
<block type="IsUsingKit">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="SoldierKitsItem">
            <field name="VALUE-0">BF1942_US</field>
            <field name="VALUE-1">USAntiTankGRA</field>
        </block>
    </value>
</block>
```

# IsTrueForAll

Returns _True_ if the provided condition is _True_ for every element in the provided **Array**.

### Inputs

1. Array
2. Bool

### Output

-   Bool

```blockly
<block type="IsTrueForAll">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="GreaterThan">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="CurrentArrayElement"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">2</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# IsTrueForAny

Returns _True_ if the provided condition is _True_ for at least one element in the provided **Array**.

### Inputs

1. Array
2. Bool

### Output

-   Bool

```blockly
<block type="IsTrueForAny">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="GetPlayerDeaths">
                    <value name="VALUE-0">
                        <block type="CurrentArrayElement"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">10</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# Kill

Kills a target **Player** (skips the Mandown state).

### Inputs

1. Player

```blockly
<block type="Kill">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# LastOf

Returns the value at the end of the specified **Array**.

### Inputs

1. Array

### Output

-   Any Type

```blockly
<block type="LastOf">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
</block>
```

# LeftVector

Returns the leftward directional **Vector** of (1, 0, 0).

### Output

-   Vector

```blockly
<block type="LeftVector"></block>
```

# LessThan

Returns a **Bool** indicating if the 1st provided value is less than the 2nd provided value.

### Inputs

1. Number
2. Number

### Output

-   Bool

```blockly
<block type="LessThan">
    <value name="VALUE-0">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
</block>
```

# LessThanEqualTo

Returns a **Bool** indicating if the 1st provided value is less than or equal to the 2nd provided value.

### Inputs

1. Number
2. Number

### Output

-   Bool

```blockly
<block type="LessThanEqualTo">
    <value name="VALUE-0">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
</block>
```

# LocalToWorldPosition

Converts the provided local **Player** position to the corresponding position in the world space.

### Inputs

1. Vector

    (Local Position)

2. Player

### Output

-   Vector

    (World Position)

```blockly
<block type="WorldPositionOf">
    <value name="VALUE-0">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# LocalToWorldVector

Converts the provided local **Player** vector to the corresponding vector in the world space.

### Inputs

1. Vector

    (Local Vector)

2. Player

### Output

-   Vector

    (World Vector)

```blockly
<block type="WorldVectorOf">
    <value name="VALUE-0">
        <block type="RightVector"></block>
    </value>
    <value name="VALUE-1">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# LoopVariable

The start of a series of **ACTIONS** that will execute in a loop, modifying the control variable on each iteration. If the control Variable reaches or passes the range end value, the loop exits, and execution continues through the remaining **ACTIONS** in the **RULE**.

### Inputs

1. Variable
2. Number

    (Start)

3. Number

    (End)

4. Number

    (Interval)

```blockly
<block type="ForVariable">
    <value name="VALUE-0">
        <block type="variableReferenceBlock">
            <mutation isObjectVar="false"></mutation>
            <field name="OBJECTTYPE">Global</field>
            <field name="VAR" variabletype="Global">Iter</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
    <value name="VALUE-3">
        <block type="Number">
            <field name="NUM">1</field>
        </block>
    </value>
    <statement name="DO">
        <block type="PrintNumberQueued">
            <value name="VALUE-0">
                <block type="GetVariable">
                    <value name="VALUE-0">
                        <block type="variableReferenceBlock">
                            <mutation isObjectVar="false"></mutation>
                            <field name="OBJECTTYPE">Global</field>
                            <field name="VAR" variabletype="Global">Iter</field>
                        </block>
                    </value>
                </block>
            </value>
        </block>
    </statement>
</block>
```

# MappedArray

Returns a copy of the provided **Array** with the values evaluated using the mapped expression provided. The following example utilizes the GetPlayers **Array** with GetGameModeScore and CurrentArrayElement to return an **Array** of **Player** scores.

### Inputs

1. Array
2. Any Type

    (Mapped Expression)

### Output

-   Array

```blockly
<block type="MappedArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="Subtract">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="CurrentArrayElement"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">2</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# Max

Returns the greater of the two **Number** values provided.

### Inputs

1. Number
2. Number

### Output

-   Number

```blockly
<block type="Max">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateNumberItem">
                    <field name="VALUE-0">SoldierStateNumber</field>
                    <field name="VALUE-1">CurrentHealth</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">50</field>
        </block>
    </value>
</block>
```

# MedGadgetTypes

Returns a **MedGadgetTypesItem** from the collection of medical gadget types which can be used with the ApplyMedGadget.

### Output

-   MedGadgetTypesItem

```blockly
<block type="MedGadgetTypesItem">
    <field name="VALUE-0">MedGadgetTypes</field>
    <field name="VALUE-1">MedicCrate</field>
</block>
```

# Message

Returns a constructed **Message** object which can be used with DisplayGameModeMessage, DisplayNotificationMessage, DisplayHighlightedWorldLogMessage, and DisplayCustomMessage. The **Message** object is created by providing a format **String**, which can take up to 3 format items.
A format **String** is a **String** that contains `{}` (called braces) within them, which can be substituted for parameters. For example, the **String** - `{} gained {} points!` - can be given a **Player** and **Number** parameter and could output as `John gained 2 points!`. See the example below for how this can be used with blocks.  
  
_Note: It\'s your responsibility to ensure a safe and fair experience for others, violating the EA User Agreement by using offensive or inappropriate text may result in account bans._

### Inputs

1. String
2. String | Number | Player

    _Optional_

3. String | Number | Player

    _Optional_

4. String | Number | Player

    _Optional_

### Output

-   Message

```blockly
<block type="Message">
    <value name="VALUE-0">
        <block type="Text">
            <field name="TEXT">{} took the lead! They have {} points!</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-2">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
</block>
```

# %{PYRITE_MOD}

%{help.mod.summary}

```
<block type="modBlock"></block>
```

# Modulo

Returns the remainder of the 1st provided value divided by the 2nd provided value.

### Inputs

1. Number
2. Number

### Output

-   Number

```blockly
<block type="Modulo">
    <value name="VALUE-0">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
</block>
```

# Multiply

Returns the product of two **Number** values or the product of a **Vector** and **Number** value.

### Inputs

1. Number | Vector
2. Number

### Output

-   Number | Vector

```blockly
<block type="Multiply">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateNumberItem">
                    <field name="VALUE-0">SoldierStateNumber</field>
                    <field name="VALUE-1">CurrentHealth</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">5</field>
        </block>
    </value>
</block>
```

# Normalize

Returns a unit-length normalization of a **Vector**.

### Inputs

1. Vector

### Output

-   Vector

```blockly
<block type="Normalize">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateVectorItem">
                    <field name="VALUE-0">SoldierStateVector</field>
                    <field name="VALUE-1">GetLinearVelocity</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# Not

Return a **Bool** of the opposite value of the **Bool** input.

### Inputs

1. Bool

### Output

-   Bool

```blockly
<block type="Not">
    <value name="VALUE-0">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="EventOtherPlayer"></block>
            </value>
        </block>
    </value>
</block>
```

# NotEqualTo

Returns a **Bool** indicating if two values are not equal to each other.

### Inputs

1. Any Type
2. Any Type

### Output

-   Bool

```blockly
<block type="NotEqualTo">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="EventOtherPlayer"></block>
    </value>
</block>
```

# Or

Returns a **Bool** based on whether either of the two inputs are _True_.

### Inputs

1. Bool
2. Bool

### Output

-   Bool

```blockly
<block type="Or">
    <value name="VALUE-0">
        <block type="GreaterThanEqualTo">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">25</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="LessThanEqualTo">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="EventOtherPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# PauseGameModeTime

Pauses or unpauses the gamemode timer based on the provided **Bool** input.

### Inputs

1. Bool

```blockly
<block type="PauseRoundTime">
    <value name="VALUE-0">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
</block>
```

# PlayerInventorySlots

Returns a **PlayerInventorySlotsItem** from the collection of all available player inventory slots.

### Output

-   PlayerInventorySlotsItem

```blockly
<block type="InventorySlotsItem">
    <field name="VALUE-0">InventorySlots</field>
    <field name="VALUE-1">CharacterGadget</field>
</block>
```

# PlayerSoldiers

Returns an **PlayerSoldiersItem** from a list of all soldiers.

### Output

-   PlayerSoldiersItem

```blockly
<block type="SoldierKitsItem">
    <field name="VALUE-0">BF2042</field>
    <field name="VALUE-1">Foxtrot</field>
</block>
```

# PlayerStateBool

Returns the **PlayerStateBoolItem** of the selected **Bool**-based player property.

### Output

-   PlayerStateBoolItem

```blockly
<block type="SoldierStateBoolItem">
    <field name="VALUE-0">SoldierStateBool</field>
    <field name="VALUE-1">IsSprinting</field>
</block>
```

# PlayerStateNumber

Returns the **PlayerStateNumberItem** of the selected **Number**-based player property.

### Output

-   PlayerStateNumberItem

```blockly
<block type="SoldierStateNumberItem">
    <field name="VALUE-0">SoldierStateNumber</field>
    <field name="VALUE-1">MaxHealth</field>
</block>
```

# PlayerStateVector

Returns the **PlayerStateVectorItem** of the selected **Vector**-based player property.

### Output

-   PlayerStateVectorItem

```blockly
<block type="SoldierStateVectorItem">
    <field name="VALUE-0">SoldierStateVector</field>
    <field name="VALUE-1">GetPosition</field>
</block>
```

# RaiseToPower

Returns the 1st provided value raised to the power of the 2nd provided value.

### Inputs

1. Number

    (Base)

2. Number

    (Exponent)

### Output

-   Number

```blockly
<block type="RaiseToPower">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">2</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">4</field>
        </block>
    </value>
</block>
```

# RandomizedArray

Returns a copy of the specified **Array** with the values in a random order.

### Inputs

1. Array

### Output

-   Array

```blockly
<block type="RandomizedArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
</block>
```

# RandomReal

Returns a random **Number** between a specified minimum and maximum value (inclusive).

### Inputs

1. Number

    (Minimum)

2. Number

    (Maximum)

### Output

-   Number

```blockly
<block type="RandomReal">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Subtract">
            <value name="VALUE-0">
                <block type="CountOf">
                    <value name="VALUE-0">
                        <block type="AllPlayers"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# RandomValueInArray

Returns a random value from the specified **Array**.

### Inputs

1. Array

### Output

-   Any Type

```blockly
<block type="RandomValueInArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
</block>
```

# ReplacePlayerInventory

Gives a target **Player** a new inventory item.

### Inputs

1. Player
2. InventoryPrimaryWeaponsItem | InventorySecondaryWeaponsItem | InventoryCharacterSpecialtiesItem | InventoryOpenGadgetsItem | InventoryThrowablesItem | InventoryMeleeWeaponsItem

```blockly
<block type="AddSoldierWeapon">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="PrimaryWeaponsItem">
            <field name="VALUE-0">PrimaryWeaponsGrafton</field>
            <field name="VALUE-1">Bazooka</field>
        </block>
    </value>
</block>
```

# ResetGameModeTime

Resets the gamemode time.

```blockly
<block type="ResetRoundTime"></block>
```

# Resupply

Resupplies the target **Player** using a provided **ResupplyTypesItem**.

### Inputs

1. Player
2. ResupplyTypesItem

```blockly
<block type="Resupply">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="ResupplyTypesItem">
            <field name="VALUE-0">ResupplyTypes</field>
            <field name="VALUE-1">SupplyBag</field>
        </block>
    </value>
</block>
```

# ResupplyTypes

Returns a **ResupplyTypesItem** from the collection of resupply types which can be used with Resupply.

### Output

-   ResupplyTypesItem

```blockly
<block type="ResupplyTypesItem">
    <field name="VALUE-0">ResupplyTypes</field>
    <field name="VALUE-1">AmmoCrate</field>
</block>
```

# RightVector

Returns the rightward directional **Vector** of (-1, 0, 0).

### Output

-   Vector

```blockly
<block type="RightVector"></block>
```

# RoundToInteger

Returns a whole **Number** rounded from the input value. The value rounds up if the decimal of the **Number** is greater than or equal to 0.5, and rounds down if it is less than 0.5.

### Inputs

1. Number

### Output

-   Number

```blockly
<block type="RoundToInteger">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">4.51</field>
        </block>
    </value>
</block>
```

# %{PYRITE_RULE}

%{help.rule.summary}

```
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

### %{help.rule.typesofrule}

#### %{PYRITE_EVENT_ONGOING}

%{help.rule.ongoing}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONPLAYERDIED}

%{help.rule.onplayerdied}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONPLAYERDEPLOYED}

%{help.rule.onplayerdeployed}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONPLAYERJOINGAME}

%{help.rule.onplayerjoingame}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONPLAYERLEAVEGAME}

%{help.rule.onplayerleavegame}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONPLAYEREARNEDKILL}

%{help.rule.onplayerearnedkill}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONGAMEMODE}

%{help.rule.ongamemodeending}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONMANDOWN}

%{help.rule.onmandown}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONREVIVED}

%{help.rule.onrevived}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONTIMELIMITREACHED}

%{help.rule.ontimelimitreached}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONGAMEMODESTARTED}

%{help.rule.ongamemodestarted}

#### %{ID_ARRIVAL_MODBUILDER_EVENT_ONPLAYERIRREVERSIBLYDEAD}

%{help.rule.onplayerirreversiblydead}

# SetGameModeScore

Sets the gamemode score of the provided **Player** or **TeamId**.

### Inputs

1. Player | TeamId
2. Number

```blockly
<block type="SetGamemodeScore">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Add">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# SetGameModeTargetScore

Sets the gamemode target score used to determine victory.

### Inputs

1. Number

```blockly
<block type="SetTargetScore">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">25</field>
        </block>
    </value>
</block>
```

# SetGameModeTimeLimit

Sets the duration of the gamemode (in seconds).

### Inputs

1. Number

```blockly
<block type="SetRoundTimeLimit">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">300</field>
        </block>
    </value>
</block>
```

# SetInventoryAmmo

Sets the target **Player** loaded ammo for the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem
3. Number

```blockly
<block type="SetInventoryAmmo">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="InventorySlotsItem">
            <field name="VALUE-0">InventorySlots</field>
            <field name="VALUE-1">SecondaryWeapon</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">1</field>
        </block>
    </value>
</block>
```

# SetInventoryMagazineAmmo

Sets the target **Player** magazine ammo for the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem
3. Number

```blockly
<block type="SetInventoryMagazineAmmo">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="InventorySlotsItem">
            <field name="VALUE-0">InventorySlots</field>
            <field name="VALUE-1">PrimaryWeapon</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
</block>
```

# SetPlayerMaxHealth

Sets the max health of a target **Player**.  
  
_Note: the max health of a player cannot be higher than 1000._

### Inputs

1. Player
2. Number

```blockly
<block type="SetPlayerMaxHealth">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">500</field>
        </block>
    </value>
</block>
```

# SetPlayerSoldier

Sets a target **Player** soldier using a provided **PlayerSoldiersItem**. The soldier selected should be one that is available from that player team\'s faction, otherwise, the soldier will not be set. (_ex. if a team\'s faction is Bad Company 2 US, that player may only select Bad Company 2 US soldiers_).

### Inputs

1. Player
2. PlayerSoldiersItem

```blockly
<block type="SetPlayerKit">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="SoldierKitsItem">
            <field name="VALUE-0">BFBC2_US</field>
            <field name="VALUE-1">USReconRUM</field>
        </block>
    </value>
</block>
```

# SetRedeployTime

Overrides the time to redeploy for a target **Player**.  
  
_Note: the redeploy time of a player cannot exceed 60 seconds._

### Inputs

1. Player
2. Number

```blockly
<block type="SetRedeployTime">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">5</field>
        </block>
    </value>
</block>
```

# SetTeamId

Sets the target **Player** team using the provided **TeamId**. This will force the **Player** back to the deploy screen.  
  
_Note: this block is not supported in Free For All and currently does not work with AI._

### Inputs

1. Player
2. TeamId

```blockly
<block type="SetTeam">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">2</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# SetVariable

Sets the value of a **Variable**.

### Inputs

1. Variable
2. Any Type

```blockly
<block type="SetVariable"></block>
```

# SetVariableAtIndex

Finds or initializes an **Array** on a provided **Variable**, and stores a provided value in that **Array** at the specified index.

### Inputs

1. Variable
2. Number

    (Index)

3. Any Type

    (Value)

```blockly
<block type="SetVariableAtIndex">
    <value name="VALUE-0">
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# SineFromDegrees

Returns the sine value of a specified angle in degrees.

### Inputs

1. Number

### Output

-   Number

```blockly
<block type="SineFromDegrees">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">180</field>
        </block>
    </value>
</block>
```

# SineFromRadians

Returns the sine value of a specified angle in radians.

### Inputs

1. Number

### Output

-   Number

```blockly
<block type="SineFromRadians">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">3.14</field>
        </block>
    </value>
</block>
```

# Skip

Skips a provided number of **ACTIONS** in the **RULE** following this block.

### Inputs

1. Number

```blockly
<block type="Skip">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">3</field>
        </block>
    </value>
</block>
```

# SkipIf

Skips a provided number of **ACTIONS** in the **RULE** following this block if the condition evaluates to _True_. If it does not, execution continues with the remaining **ACTIONS**.

### Inputs

1. Number
2. Bool

```blockly
<block type="SkipIf">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">3</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
</block>
```

# SkipMandown

Sets the target **Player** to skip the mandown state and go directly to the deploy screen when killed.

### Inputs

1. Player
2. Bool

```blockly
<block type="SkipManDown">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
</block>
```

# SortedArray

Returns a sorted version of the specified **Array** given a **Number** value to sort by (ascending). CurrentArrayElement can be utilized to represent each value in the **Array**. In the following example, CurrentArrayElement is used to represent each **Player** in GetPlayers. GetGameModeScore is used with CurrentArrayElement to return the score, used as a rank, to sort the **Array** in ascending order.

### Inputs

1. Array
2. Number

    (Rank)

### Output

-   Array

```blockly
<block type="SortedArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="CurrentArrayElement"></block>
            </value>
        </block>
    </value>
</block>
```

# SpotTarget

Spots a target **Player** for a specified duration of time (in seconds).

### Inputs

1. Player
2. Number

    (Duration)

```blockly
<block type="SpotTarget">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
</block>
```

# SquareRoot

Returns the square root of a provided **Number** value.

### Inputs

1. Number

### Output

-   Number

```blockly
<block type="SquareRoot">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">64</field>
        </block>
    </value>
</block>
```

# StopTrackingVariable

Stops an in-progress tracking of a **Variable**, leaving it at its current value.

### Inputs

1. Variable

```blockly
<block type="StopChasingVariable"></block>
```

# %{PYRITE_SUBROUTINE}

%{help.subroutine.summary}

```
<block type="subroutineBlock">
    <field name="SUBROUTINE_NAME">Subroutine</field>
</block>
```

# Subtract

Returns the difference between two **Number** values or two **Vector** values.

### Inputs

1. Number | Vector
2. Number | Vector

### Output

-   Number | Vector

```blockly
<block type="Subtract">
    <value name="VALUE-0">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">1</field>
        </block>
    </value>
</block>
```

# Teleport

Teleports a target to a provided valid position.

### Inputs

1. Player
2. Vector

    (Position)

3. Number

    (Yaw Rotation)

```blockly
<block type="Teleport">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">180</field>
        </block>
    </value>
</block>
```

# TrackVariableAtRate

Gradually modifies the value of a **Variable** at a specified rate (value/second) until it reaches the provided limit.

### Inputs

1. Variable
2. Number

    (Limit)

3. Number

    (Rate)

```blockly
<block type="ChaseVariableAtRate">
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">30</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">1</field>
        </block>
    </value>
</block>
```

# TrackVariableOverTime

Gradually modifies the value of a **Variable** over time (in seconds). The variable\'s value will reach the limit at the end of the interval.

### Inputs

1. Variable
2. Number

    (Limit)

3. Number

    (Interval)

```blockly
<block type="ChaseVariableOverTime">
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">100</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">30</field>
        </block>
    </value>
</block>
```

# UndeployAllPlayers

Undeploys all players that are alive on the battlefield back to the deploy screen.

```blockly
<block type="UnspawnAllPlayers"></block>
```

# UndeployPlayer

Undeploys a target **Player** that is alive on the battlefield back to the deploy screen.

### Inputs

1. Player

```blockly
<block type="UnspawnPlayer">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# UnspotTarget

Unspots a target **Player**.

### Inputs

1. Player

```blockly
<block type="UnspotTarget">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# UpVector

Returns the upward directional **Vector** of (0, 1, 0).

### Output

-   Vector

```blockly
<block type="UpVector"></block>
```

# ValueInArray

Returns the value found at a provided index of an **Array**.

### Inputs

1. Array
2. Number

### Output

-   Any Type

```blockly
<block type="ValueInArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
</block>
```

# %{PYRITE_TYPE_VARIABLE}

%{help.variablereference.summary}

# VectorTowards

Returns the displacement **Vector** from a starting position to an ending position.

### Inputs

1. Vector

    (Starting Position)

2. Vector (Ending Position)

    (Ending Position)

### Output

-   Vector

```blockly
<block type="VectorTowards">
    <value name="VALUE-0">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateVectorItem">
                    <field name="VALUE-0">SoldierStateVector</field>
                    <field name="VALUE-1">GetPosition</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# Wait

Pauses the execution of **ACTIONS** in a **RULE** for a provided **Number** of seconds.

### Inputs

1. Number

```blockly
<block type="Wait">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">1</field>
        </block>
    </value>
</block>
```

# WaitUntil

Pauses the execution of **ACTIONS** in a **RULE** for a provided **Number** of seconds or if the provided condition evaluates to _True_ during that interval.

### Inputs

1. Number
2. Bool

## Output

```blockly
<block type="WaitUntil">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">5</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateBoolItem">
                    <field name="VALUE-0">SoldierStateBool</field>
                    <field name="VALUE-1">IsInAir</field>
                </block>
            </value>
        </block>
    </value>
</block>
```

# While

A block of **ACTIONS** that will execute in a loop as long as the provided condition is _True_.  
  
_Note: You must utilize a Wait block at the beginning or the end of the iteration._

### Inputs

1. Bool

```blockly
<block type="While">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateBoolItem">
                    <field name="VALUE-0">SoldierStateBool</field>
                    <field name="VALUE-1">IsAlive</field>
                </block>
            </value>
        </block>
    </value>
    <statement name="DO">
        <block type="Wait">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </statement>
</block>
```

# WorldToLocalPosition

Converts the provided world position to the corresponding position in local **Player** space.

### Inputs

1. Vector

    (World Position)

2. Player

### Output

-   Vector

    (Local Position)

```blockly
<block type="LocalPositionOf">
    <value name="VALUE-0">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="EventPlayer"></block>
    </value>
</block>
```

# WorldToLocalVector

Converts the provided world vector to the corresponding vector in local **Player** space.

### Inputs

1. Vector

    (World Vector)

2. Player

### Output

-   Vector

    (Local Vector)

```blockly
<block type="LocalVectorOf">
    <value name="VALUE-0">
        <block type="ForwardVector"></block>
    </value>
    <value name="VALUE-1">
        <block type="EventPlayer"></block>
    </value>
</block>
```

