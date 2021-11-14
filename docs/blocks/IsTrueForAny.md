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
