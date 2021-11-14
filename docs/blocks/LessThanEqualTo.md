# LessThanEqualTo

Returns a **Bool** indicating if the 1st provided value is less than or equal to the 2nd provided value.

### Inputs

1. Number
2. Number

### Output

-   Bool

```blockly
<block type="LessThanEqualTo">
    <value name="VALUE-0">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
</block>
```
