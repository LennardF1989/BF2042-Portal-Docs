# IfThenElse

Returns the 1st provided value if the condition is _True_, otherwise, returns the 2nd provided value.

### Inputs

1. Bool
2. Any Type

    (Output Value if the Condition is _True_)

3. Any Type

    (Output Value if the Condition is _False_)

### Output

-   Any Type

```blockly
<block type="IfThenElse">
    <value name="VALUE-0">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="EventPlayer"></block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="Number">
                            <field name="NUM">1</field>
                        </block>
                    </value>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
</block>
```
