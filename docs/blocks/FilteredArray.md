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
