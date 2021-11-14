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

### Notes
1. You don't need to use this block if you want to change the message's text.
2. If you want to push a custom message after this block, use [`Wait(0.1)`](/docs/blocks/Wait.md) block before that, otherwise it won't work.