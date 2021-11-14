# Divide

Returns the ratio between two **Number** values or a **Vector** and **Number** value. A **Vector** divided by a **Number** will yield a scaled **Vector**.

### Inputs

1. Number | Vector
2. Number

### Output

-   Number | Vector

```blockly
<block type="Divide">
    <value name="VALUE-0">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
</block>
```
