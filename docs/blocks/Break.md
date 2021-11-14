# Break

Breaks and exits the execution of a looping block, such as While or LoopVariable.

```blockly
<block type="While">
    <value name="VALUE-0">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
    <statement name="DO">
        <block type="Wait">
            <value name="VALUE-0">
                <block type="Number">
                    <field name="NUM">1</field>
                </block>
            </value>
            <next>
                <block type="Break"></block>
            </next>
        </block>
    </statement>
</block>
```
