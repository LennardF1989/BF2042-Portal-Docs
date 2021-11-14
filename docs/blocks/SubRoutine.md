# SUBROUTINE

**SUBROUTINE** blocks are special blocks that are similar to **RULE** blocks, but do not have a designated **EVENT**. A **SUBROUTINE** block\'s **ACTIONS** will be executed when called from the **RULE** block. Like **RULE** blocks, **SUBROUTINE** blocks can have a **CONDITION** to determine whether or not the **ACTIONS** inside should execute.
  
  An important note is payload values, including EventPlayer, EventOtherPlayer, and EventTeam, use the context of the **RULE** block in which the **SUBROUTINE** instance block is placed in. An example of this would be, if your **RULE** block has an instance of EventPlayer, and the **SUBROUTINE** is called in OnPlayerDeployed, it would use the EventPlayer associated with OnPlayerDeployed. Be careful with this, as you will run into errors if your **SUBROUTINE** is placed inside a **RULE** block with non-existant payloads for that **EVENT**.

```blockly
<block type="subroutineBlock">
    <field name="SUBROUTINE_NAME">Subroutine</field>
</block>
```
