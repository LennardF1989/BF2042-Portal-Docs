# SetPlayerSoldier

Sets a target **Player** soldier using a provided **PlayerSoldiersItem**. The soldier selected should be one that is available from that player team\'s faction, otherwise, the soldier will not be set. (_ex. if a team\'s faction is Bad Company 2 US, that player may only select Bad Company 2 US soldiers_).

### Inputs

1. Player
2. PlayerSoldiersItem

```blockly
<block type="SetPlayerKit">
    <value name="VALUE-0">
        <block type="EventPlayer"></block>
    </value>
    <value name="VALUE-1">
        <block type="SoldierKitsItem">
            <field name="VALUE-0">BFBC2_US</field>
            <field name="VALUE-1">USReconRUM</field>
        </block>
    </value>
</block>
```
