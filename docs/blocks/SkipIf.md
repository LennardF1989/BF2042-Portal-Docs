# SkipIf

Skips a provided number of **ACTIONS** in the **RULE** following this block if the condition evaluates to _True_. If it does not, execution continues with the remaining **ACTIONS**.

### Inputs

1. Number
2. Bool

```blockly
<block type="SkipIf">
    <value name="VALUE-0">
        <block type="Number">
            <field name="NUM">3</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Boolean">
            <field name="BOOL">TRUE</field>
        </block>
    </value>
</block>
```
