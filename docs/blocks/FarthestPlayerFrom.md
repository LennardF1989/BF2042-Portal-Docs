# Farthest Player From

Returns the farthest **Player** from a position. Can be filtered using a **TeamId**.

### Inputs

1. Vector

    (Position)

2. TeamId

    _Optional_

### Output

-   Player

```blockly
<block type="FarthestPlayerFrom">
    <value name="VALUE-0">
        <block type="CreateVector">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
            <value name="VALUE-2">
                <block type="Number">
                    <field name="NUM">0</field>
                </block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="GetTeamId">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">2</field>
                </block>
            </value>
        </block>
    </value>
</block>
```
