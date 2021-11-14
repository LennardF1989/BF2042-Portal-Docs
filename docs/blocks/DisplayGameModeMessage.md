# DisplayGameModeMessage

Displays a **Message** on the screen for 6 seconds. If no target is provided, the **Message** will display to everyone.  
  
_Note: This will only appear to players that are deployed on the map. It\'s your responsibility to ensure a safe and fair experience for others, violating the EA User Agreement by using offensive or inappropriate text may result in account bans._

### Inputs

1. Message
2. Player | TeamId

    _Optional_

```blockly
<block type="ShowEventGameModeMessage">
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
        <block type="EventPlayer"></block>
    </value>
</block>
```

### Notes
1. If you push several game mode messages one after another, they will stack and will be shown one by one in the order of execution.
2. This message will produce a sound when appears and disappears from the screen.
3. You can see all the message appearances [here](https://cdn.discordapp.com/attachments/907670279675842640/908647207023026196/unknown.png).