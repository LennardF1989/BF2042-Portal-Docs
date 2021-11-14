# Teleport

Teleports a target to a provided valid position.

### Inputs

1. Player
2. Vector

    (Position)

3. Number

    (Yaw Rotation)

```blockly
<block type="Teleport">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
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
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">180</field>
        </block>
    </value>
</block>
```
