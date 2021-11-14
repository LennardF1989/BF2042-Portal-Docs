# While

A block of **ACTIONS** that will execute in a loop as long as the provided condition is _True_.  
  
_Note: You must utilize a Wait block at the beginning or the end of the iteration._

### Inputs

1. Bool

```blockly
<block type="While">
    <value name="VALUE-0">
        <block type="GetSoldierState">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
            <value name="VALUE-1">
                <block type="SoldierStateBoolItem">
                    <field name="VALUE-0">SoldierStateBool</field>
                    <field name="VALUE-1">IsAlive</field>
                </block>
            </value>
        </block>
    </value>
    <statement name="DO">
        <block type="Wait">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </statement>
</block>
```
