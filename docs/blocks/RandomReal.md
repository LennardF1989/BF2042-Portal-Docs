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
