# IsFaction

Returns _True_ whether or not the provided **TeamId** is using soldiers from the provided **FactionsItem**.

### Inputs

1. TeamId
2. FactionsItem

```blockly
<block type="IsFaction">
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
        <block type="FactionsItem">
            <field name="VALUE-0">Factions</field>
            <field name="VALUE-1">Grafton_GER</field>
        </block>
    </value>
</block>
```
