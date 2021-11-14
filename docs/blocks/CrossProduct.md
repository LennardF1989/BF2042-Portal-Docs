# CrossProduct

Returns the cross product between two **Vector** values. If the two **Vector** inputs are parallel, the result will be zero.

### Inputs

1. Vector
2. Vector

### Output

-   Vector

```blockly
<block type="CrossProduct">
    <value name="VALUE-0">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">3</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">5</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">6</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="ForwardVector">
        </block>
    </value>
</block>
```
