# TrackVariableAtRate

Gradually modifies the value of a **Variable** at a specified rate (value/second) until it reaches the provided limit.

### Inputs

1. Variable
2. Number

    (Limit)

3. Number

    (Rate)

```blockly
<block type="ChaseVariableAtRate">
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">30</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">1</field>
        </block>
    </value>
</block>
```
