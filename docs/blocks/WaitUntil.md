# WaitUntil

Pauses the execution of **ACTIONS** in a **RULE** for a provided **Number** of seconds or if the provided condition evaluates to _True_ during that interval.

### Inputs

1. Number
2. Bool

## Output

```blockly
<block type="WaitUntil">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">5</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateBoolItem">
                    <field name="VALUE-0">SoldierStateBool</field>
                    <field name="VALUE-1">IsInAir</field>
                </block>
            </value>
        </block>
    </value>
</block>
```
