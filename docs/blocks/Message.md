# Message

Returns a constructed **Message** object which can be used with DisplayGameModeMessage, DisplayNotificationMessage, DisplayHighlightedWorldLogMessage, and DisplayCustomMessage. The **Message** object is created by providing a format **String**, which can take up to 3 format items.
A format **String** is a **String** that contains `{}` (called braces) within them, which can be substituted for parameters. For example, the **String** - `{} gained {} points!` - can be given a **Player** and **Number** parameter and could output as `John gained 2 points!`. See the example below for how this can be used with blocks.  
  
_Note: It\'s your responsibility to ensure a safe and fair experience for others, violating the EA User Agreement by using offensive or inappropriate text may result in account bans._

### Inputs

1. String
2. String | Number | Player

    _Optional_

3. String | Number | Player

    _Optional_

4. String | Number | Player

    _Optional_

### Output

-   Message

```blockly
<block type="Message">
    <value name="VALUE-0">
        <block type="Text">
            <field name="TEXT">{} took the lead! They have {} points!</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-2">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
</block>
```
