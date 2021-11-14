# SetInventoryMagazineAmmo

Sets the target **Player** magazine ammo for the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem
3. Number

```blockly
<block type="SetInventoryMagazineAmmo">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="InventorySlotsItem">
            <field name="VALUE-0">InventorySlots</field>
            <field name="VALUE-1">PrimaryWeapon</field>
        </block>
    </value>
    <value name="VALUE-2">
        <block type="Number">
            <field name="NUM">0</field>
        </block>
    </value>
</block>
```
