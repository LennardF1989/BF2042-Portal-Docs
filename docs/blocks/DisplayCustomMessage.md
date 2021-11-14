# DisplayCustomMessage

Display a **Message** on-screen exclusive to custom gamemodes. Using the **CustomMessageSlotsItem**, this **Message** can be displayed on multiple lines. It will stay up for the length of the provided duration, or stay up indefinitely if a negative **Number** is provided. It will be displayed to everyone unless a specific **Player** or **TeamId** is provided.  
  
_Note: It\'s your responsibility to ensure a safe and fair experience for others, violating the EA User Agreement by using offensive or inappropriate text may result in account bans._

### Inputs

1. Message
2. CustomMessageSlotsItem
3. Number

    (Duration)

4. Player | TeamId

    (Group)

    _Optional_

```blockly
<block type="DisplayCustomNotificationMessage">
    <value name="VALUE-0">
        <block type="Message">
            <value name="VALUE-0">
                <block type="Text">
                    <field name="TEXT">This is a Custom Message!</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="CustomMessagesItem">
            <field name="VALUE-0">CustomMessages</field>
            <field name="VALUE-1">HeaderText</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">-1</field>
        </block>
    </value>
    <value name="VALUE-3">
        <block type="EventPlayer"></block>
    </value>
</block>
```

### Notes:
1. Custom messages will be covered by a kill card (when killed) and a deploy screen background. If you want to make sure the player sees the message, use [NotificationMessage](/docs/blocks/DisplayNotificationMessage.md)
2. You can see all the message appearances [here](https://cdn.discordapp.com/attachments/907670279675842640/908647207023026196/unknown.png).