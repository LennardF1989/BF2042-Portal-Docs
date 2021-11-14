# ClearCustomMessage

Clears text from the provided **CustomMessageSlotsItem** for the provided **Player** or **TeamId**. If no **Player** or **TeamId** is given, it clears all players text at that **CustomMessageSlotsItem**.

### Inputs

1. CustomMessageSlotsItem
2. Player | TeamId

    (Group)

    _Optional_

```blockly
<block type="ClearCustomNotificationMessage">
    <value name="VALUE-0">
        <block type="CustomMessagesItem">
            <field name="VALUE-0">CustomMessages</field>
            <field name="VALUE-1">MessageText3</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="EventPlayer"></block>
    </value>
</block>
```
