# IsVictimDeathType

Returns a **Bool** indicating if the victim died by the provided **DeathType**.

### Inputs

1. DeathType
2. DeathTypesItem

### Output

-   Bool

```
<block type="EventDeathTypeCompare">
    <value name="VALUE-0">
        <block type="EventDeathType"></block>
    </value>
    <value name="VALUE-1">
        <block type="PlayerDeathTypesItem">
            <field name="VALUE-0">PlayerDeathTypes</field>
            <field name="VALUE-1">Headshot</field>
        </block>
    </value>
</block>
```
