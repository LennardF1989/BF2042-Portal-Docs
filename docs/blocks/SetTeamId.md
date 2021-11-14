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
