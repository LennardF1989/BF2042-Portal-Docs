# LoopVariable

The start of a series of **ACTIONS** that will execute in a loop, modifying the control variable on each iteration. If the control Variable reaches or passes the range end value, the loop exits, and execution continues through the remaining **ACTIONS** in the **RULE**.

### Inputs

1. Variable
2. Number

    (Start)

3. Number

    (End)

4. Number

    (Interval)

```blockly
<block type="ForVariable">
    <value name="VALUE-0">
        <block type="variableReferenceBlock">
            <mutation isObjectVar="false"></mutation>
            <field name="OBJECTTYPE">Global</field>
            <field name="VAR" variabletype="Global">Iter</field>
        </block>
    </value>
    <value name="VALUE-1">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">10</field>
        </block>
    </value>
    <value name="VALUE-3">
        <block type="Number">
            <field name="NUM">1</field>
        </block>
    </value>
    <statement name="DO">
        <block type="PrintNumberQueued">
            <value name="VALUE-0">
                <block type="GetVariable">
                    <value name="VALUE-0">
                        <block type="variableReferenceBlock">
                            <mutation isObjectVar="false"></mutation>
                            <field name="OBJECTTYPE">Global</field>
                            <field name="VAR" variabletype="Global">Iter</field>
                        </block>
                    </value>
                </block>
            </value>
        </block>
    </statement>
</block>
```
