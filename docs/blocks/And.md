# And

Returns a **Bool** value based on whether both of the provided inputs return _True_.

### Inputs

1. Bool
2. Bool

### Output

-   Bool

```blockly
<block type="And">
    <value name="VALUE-0">
        <block type="GreaterThan">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
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
    <value name="VALUE-1">
        <block type="LessThan">
            <value name="VALUE-0">
                <block type="GetGamemodeScore">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">4</field>
                </block>
            </value>
        </block>
    </value>
</block>
```
