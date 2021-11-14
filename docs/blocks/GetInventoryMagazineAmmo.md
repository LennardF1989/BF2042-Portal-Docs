# GetInventoryMagazineAmmo

Returns the target **Player** magazine ammo of the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem

### Output

-   Number

```blockly
<block type="GetInventoryMagazineAmmo">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="InventorySlotsItem">
            <field name="VALUE-0">InventorySlots</field>
            <field name="VALUE-1">PrimaryWeapon</field>
        </block>
    </value>
</block>
```
