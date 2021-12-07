# IsKillerWeapon

Returns a **Bool** indicating if the given **HardwareId** is equivalent to the provided ability.

### Inputs

1. HardwareId
2. InventoryPrimaryWeaponsItem | InventorySecondaryWeaponsItem | InventoryCharacterSpecialtiesItem | InventoryOpenGadgetsItem | InventoryThrowablesItem | InventoryMeleeWeaponsItem

### Output

-   Bool

```
<block type="EventWeaponCompare">
    <value name="VALUE-0">
        <block type="EventWeapon"></block>
    </value>
    <value name="VALUE-1">
        <block type="PrimaryWeaponsItem">
            <field name="VALUE-0">PrimaryWeaponsGrafton</field>
            <field name="VALUE-1">Bazooka</field>
        </block>
    </value>
</block>
```
