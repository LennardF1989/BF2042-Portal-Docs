# Normalize

Returns a unit-length normalization of a **Vector**.

### Inputs

1. Vector

### Output

-   Vector

```blockly
<block type="Normalize">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateVectorItem">
                    <field name="VALUE-0">SoldierStateVector</field>
                    <field name="VALUE-1">GetLinearVelocity</field>
                </block>
            </value>
        </block>
    </value>
</block>
```
