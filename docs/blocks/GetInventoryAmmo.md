# GetInventoryAmmo

Returns the target **Player** loaded ammo of the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem

### Output

-   Number

```blockly
<block type="GetInventoryAmmo">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="InventorySlotsItem">
            <field name="VALUE-0">InventorySlots</field>
            <field name="VALUE-1">SecondaryWeapon</field>
        </block>
    </value>
</block>
```
