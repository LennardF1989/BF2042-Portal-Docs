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
