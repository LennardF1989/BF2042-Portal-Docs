# ClearAllCustomMessages

Clears all custom messages for a provided **Player** or **TeamId**. If no **Player** or **TeamId** is provided, it will clear all custom messages for everyone.

### Inputs

1. Player | TeamId

    (Group)

    _Optional_

```blockly
<block type="ClearAllCustomNotificationMessages">
    <value name="VALUE-0">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
        </block>
    </value>
</block>
```
