# Or

Returns a **Bool** based on whether either of the two inputs are _True_.

### Inputs

1. Bool
2. Bool

### Output

-   Bool

```blockly
<block type="Or">
    <value name="VALUE-0">
        <block type="GreaterThanEqualTo">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">25</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="LessThanEqualTo">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="EventOtherPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
</block>
```
