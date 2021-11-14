# SortedArray

Returns a sorted version of the specified **Array** given a **Number** value to sort by (ascending). CurrentArrayElement can be utilized to represent each value in the **Array**. In the following example, CurrentArrayElement is used to represent each **Player** in GetPlayers. GetGameModeScore is used with CurrentArrayElement to return the score, used as a rank, to sort the **Array** in ascending order.

### Inputs

1. Array
2. Number

    (Rank)

### Output

-   Array

```blockly
<block type="SortedArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="GetGamemodeScore">
            <value name="VALUE-0">
                <block type="CurrentArrayElement"></block>
            </value>
        </block>
    </value>
</block>
```
