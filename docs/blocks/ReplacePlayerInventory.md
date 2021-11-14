# ReplacePlayerInventory

Gives a target **Player** a new inventory item.

### Inputs

1. Player
2. InventoryPrimaryWeaponsItem | InventorySecondaryWeaponsItem | InventoryCharacterSpecialtiesItem | InventoryOpenGadgetsItem | InventoryThrowablesItem | InventoryMeleeWeaponsItem

```blockly
<block type="AddSoldierWeapon">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="PrimaryWeaponsItem">
            <field name="VALUE-0">PrimaryWeaponsGrafton</field>
            <field name="VALUE-1">Bazooka</field>
        </block>
    </value>
</block>
```
