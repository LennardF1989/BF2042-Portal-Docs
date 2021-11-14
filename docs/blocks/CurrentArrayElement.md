# CurrentArrayElement

Returns a reference to the current **Array** element being evaluated. Only used for FilteredArray, MappedArray, SortedArray, IsTrueForAll, and IsTrueForAny.

### Output

-   Any Type

```blockly
<block type="FilteredArray">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
    <value name="VALUE-1">
        <block type="Equals">
            <value name="VALUE-0">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="Number">
                            <field name="NUM">1</field>
                        </block>
                    </value>
                </block>
            </value>
            <value name="VALUE-1">
                <block type="GetTeamId">
                    <value name="VALUE-0">
                        <block type="CurrentArrayElement"></block>
                    </value>
                </block>
            </value>
        </block>
    </value>
</block>
```
