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
