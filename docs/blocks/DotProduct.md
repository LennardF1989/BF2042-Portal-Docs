# DotProduct

Returns the dot product between two **Vector** values. If the two values are orthogonal to each other, the result will be zero.

### Inputs

1. Vector
2. Vector

### Output

-   Number

```blockly
<block type="DotProduct">
    <value name="VALUE-0">
        <block type="LocalVectorOf">
            <value name="VALUE-0">
                <block type="ForwardVector"></block>
            </value>
            <value name="VALUE-1">
                <block type="EventPlayer"></block>
            </value>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="LocalVectorOf">
            <value name="VALUE-0">
                <block type="ForwardVector"></block>
            </value>
            <value name="VALUE-1">
                <block type="EventOtherPlayer"></block>
            </value>
        </block>
    </value>
</block>
```
