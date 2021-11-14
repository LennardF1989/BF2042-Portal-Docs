# IsInventorySlotActive

Returns _True_ whether or not the active inventory slot of the target **Player** is the provided **PlayerInventorySlotsItem**.

### Inputs

1. Player
2. PlayerInventorySlotsItem

### Output

-   Bool

```blockly
<block type="IsInventorySlotActive">
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
