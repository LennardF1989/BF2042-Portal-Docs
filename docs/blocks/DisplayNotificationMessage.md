# DisplayCustomMessage

Displays a notification-type **Message** on the screen for 6 seconds. If no target is provided, it will display the **Message** to everyone.  
  
_Note: It's your responsibility to ensure a safe and fair experience for others, violating the EA User Agreement by using offensive or inappropriate text may result in account bans._

### Inputs

1. Message
2. Player | TeamId

    _Optional_

```blockly
<block type="ShowNotificationMessage">
    <value name="VALUE-0">
        <block type="Message">
            <value name="VALUE-0">
                <block type="Text">
                    <field name="TEXT">Hello World!</field>
                </block>
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
```

### Notes:
1. Notification messages will appear above all other UI elements and produce a sound.
2. You can see all the message appearances [here](https://cdn.discordapp.com/attachments/907670279675842640/908647207023026196/unknown.png).