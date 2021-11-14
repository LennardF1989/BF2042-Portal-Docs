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
