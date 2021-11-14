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
