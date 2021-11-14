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
