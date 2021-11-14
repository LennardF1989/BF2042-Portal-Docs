# Multiply

Returns the product of two **Number** values or the product of a **Vector** and **Number** value.

### Inputs

1. Number | Vector
2. Number

### Output

-   Number | Vector

```blockly
<block type="Multiply">
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
            <field name="NUM">5</field>
        </block>
    </value>
</block>
```
