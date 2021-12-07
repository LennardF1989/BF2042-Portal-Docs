# TrackVariableOverTime

Gradually modifies the value of a **Variable** over time (in seconds). The variable's value will reach the limit at the end of the interval.

### Inputs

1. Variable
2. Number

    (Limit)

3. Number

    (Interval)

```blockly
<block type="ChaseVariableOverTime">
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">100</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">30</field>
        </block>
    </value>
</block>
```
