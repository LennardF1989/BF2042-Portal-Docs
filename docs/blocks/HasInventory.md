# HasInventory

Returns a **Bool** indicating if the provided **Player** has the specified ability.

### Inputs

1. Player
2. InventoryPrimaryWeaponsItem | InventorySecondaryWeaponsItem | InventoryCharacterSpecialtiesItem | InventoryOpenGadgetsItem | InventoryThrowablesItem | InventoryMeleeWeaponsItem

### Output

-   Bool

```blockly
<block type="HasInventory">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="PrimaryWeaponsItem">
            <field name="VALUE-0">PrimaryWeaponsKingston</field>
            <field name="VALUE-1">SLX Spear</field>
        </block>
    </value>
</block>
```
