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
