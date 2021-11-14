# DealDamage

Sets an amount of damage to be applied to a target **Player** by a giver **Player**.

### Inputs

1. Player

    (Target)

2. Number
3. Player

    (Giver)

    _Optional_

```blockly
<block type="SetPlayerDamage">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">25</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="EventOtherPlayer"></block>
    </value>
</block>
```
