# EnableInputRestriction

Enables or disables a specified **InputRestrictionsItem** on a target **Player**.

### Inputs

1. Player
2. InputRestrictionsItem
3. Bool

```blockly
<block type="EnableInputRestriction">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="RestrictedInputsItem">
            <field name="VALUE-0">RestrictedInputs</field>
            <field name="VALUE-1">FireWeapon</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
</block>
```
