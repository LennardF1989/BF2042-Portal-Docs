# CountOf

Returns the **Number** of elements in the specified **Array**.

### Inputs

1. Array

### Output

-   Number

```blockly
<block type="CountOf">
    <value name="VALUE-0">
        <block type="AllPlayers"></block>
    </value>
</block>
```

### Notes
{alert=warning} **BE CAREFUL:** This block will return the highest array index + 1 (like in Python), NOT the real element count.

**Example:**  
This subroutine will send a notification with text `1001`, not `2`.
```blockly
<block xmlns="https://developers.google.com/blockly/xml" type="subroutineBlock" deletable="false" x="-837.0625725" y="-1904.428075"><field name="SUBROUTINE_NAME">CountOfTest</field><statement name="ACTIONS"><block type="SetVariableAtIndex"><value name="VALUE-0"><block type="variableReferenceBlock"><mutation isObjectVar="false"/><field name="OBJECTTYPE">Global</field><field name="VAR" id="7{w%w#%4Q=G~hHdZ7x*?" variabletype="Global">TestVariable</field></block></value><value name="VALUE-1"><block type="Number"><field name="NUM">1</field></block></value><value name="VALUE-2"><block type="SecondaryWeaponsItem"><field name="VALUE-0">SecondaryWeaponsAlexandria</field><field name="VALUE-1">MP443_ALX</field></block></value><next><block type="SetVariableAtIndex"><value name="VALUE-0"><block type="variableReferenceBlock"><mutation isObjectVar="false"/><field name="OBJECTTYPE">Global</field><field name="VAR" id="7{w%w#%4Q=G~hHdZ7x*?" variabletype="Global">TestVariable</field></block></value><value name="VALUE-1"><block type="Number"><field name="NUM">1000</field></block></value><value name="VALUE-2"><block type="SecondaryWeaponsItem"><field name="VALUE-0">SecondaryWeaponsAlexandria</field><field name="VALUE-1">M93R_ALX</field></block></value><next><block type="ShowNotificationMessage"><value name="VALUE-0"><block type="Message"><value name="VALUE-0"><block type="Text"><field name="TEXT">{}</field></block></value><value name="VALUE-1"><block type="CountOf"><value name="VALUE-0"><block type="GetVariable"><value name="VALUE-0"><block type="variableReferenceBlock"><mutation isObjectVar="false"/><field name="OBJECTTYPE">Global</field><field name="VAR" id="7{w%w#%4Q=G~hHdZ7x*?" variabletype="Global">TestVariable</field></block></value></block></value></block></value></block></value></block></next></block></next></block></statement></block>
```
![Example](https://i.imgur.com/MJOmNdk.png)
