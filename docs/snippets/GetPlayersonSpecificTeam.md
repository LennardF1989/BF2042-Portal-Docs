# Get Teams from Specific Team

This snippet is fairly simple but is a fairly common operation one would need to perform. This block will return an array of players that belong to a specific team (In this case, team 1).

```blocky
<block xmlns="https://developers.google.com/blockly/xml" type="FilteredArray" id="Mx3AU9*E|b8[,B?G0]FI">
  <value name="VALUE-0">
    <block type="AllPlayers" id="(KF/TI]!3WA@b4z3ILk)"></block>
  </value>
  <value name="VALUE-1">
    <block type="Equals" id="lN8xmrVXDTj^c~ja9w{5">
      <value name="VALUE-0">
        <block type="GetTeamId" id="/GxI73TG=#U}*_QSryLg">
          <value name="VALUE-0">
            <block type="Number" id="QQ(~?gH~[Td3OSn*CXOQ">
              <field name="NUM">1</field>
            </block>
          </value>
        </block>
      </value>
      <value name="VALUE-1">
        <block type="GetTeamId" id="qqxj+8eJ4WgCI7c?^z7S">
          <value name="VALUE-0">
            <block type="EventPlayer" id="z6,+PTKf$Dxbt`]]2fH+"></block>
          </value>
        </block>
      </value>
    </block>
  </value>
</block>
```

# Example uses
Please note that these are just snippets. If you intend to use them they may need to be modified to fit your use case. These are provided as is.

## Example 1
Force deploy all dead players if all players on team 1 have died/are dead.

```blocky
<block xmlns="https://developers.google.com/blockly/xml" type="modBlock" id="^15vAkBG@_ba7/8zyu60" deletable="false">
  <statement name="RULES">
    <block type="ruleBlock" id="][;03?;kx[,i|$vI=rLC">
      <mutation isOnGoingEvent="false"></mutation>
      <field name="NAME">Wave Respawn</field>
      <field name="EVENTTYPE">OnPlayerDied</field>
      <statement name="CONDITIONS">
        <block type="conditionBlock" id="1mfRM:z3W,ksAx2h5bZc">
          <value name="CONDITION">
            <block type="IsTrueForAll" id="Y@OGD*2@.j|md1lM]dSy" inline="false">
              <value name="VALUE-0">
                <block type="FilteredArray" id="EOd#k{jWxFG))_9qff$N">
                  <value name="VALUE-0">
                    <block type="AllPlayers" id=":A%vHz8b`rtEM.?^qyr!"></block>
                  </value>
                  <value name="VALUE-1">
                    <block type="Equals" id="A2$Tj/S[@eFHe!MsGR08">
                      <value name="VALUE-0">
                        <block type="GetTeamId" id=";fU4ypjeB$_,9*%X`,bs">
                          <value name="VALUE-0">
                            <block type="Number" id="g~-UztfpfzvnL|{.qO*}">
                              <field name="NUM">1</field>
                            </block>
                          </value>
                        </block>
                      </value>
                      <value name="VALUE-1">
                        <block type="GetTeamId" id="lT|6+X1_d;V|R*LHS2=Z">
                          <value name="VALUE-0">
                            <block type="CurrentArrayElement" id="|6R6g~/n?)yswDz0gK:{"></block>
                          </value>
                        </block>
                      </value>
                    </block>
                  </value>
                </block>
              </value>
              <value name="VALUE-1">
                <block type="FilteredArray" id="Yk+j@VXx7GZcR=lrU@NF">
                  <value name="VALUE-0">
                    <block type="AllPlayers" id="!T^C]F]#K[q!zB2zY}8q"></block>
                  </value>
                  <value name="VALUE-1">
                    <block type="And" id="6dpf!!SXe|@aT$g+Pw2C">
                      <value name="VALUE-0">
                        <block type="Equals" id="qOy_AU()mCviF`d(nVQH">
                          <value name="VALUE-0">
                            <block type="GetTeamId" id="@8~sWMqQixkWZ22Fe%=a">
                              <value name="VALUE-0">
                                <block type="Number" id="Qs[IV~2L_6]pFSd1FC1*">
                                  <field name="NUM">1</field>
                                </block>
                              </value>
                            </block>
                          </value>
                          <value name="VALUE-1">
                            <block type="GetTeamId" id="IO/4^ESO9U{8aJ$wsabu">
                              <value name="VALUE-0">
                                <block type="CurrentArrayElement" id="X^{}1F%9DHMsLRV].tS."></block>
                              </value>
                            </block>
                          </value>
                        </block>
                      </value>
                      <value name="VALUE-1">
                        <block type="GetSoldierState" id="|W~$8Df8HTwOj1l]([A1">
                          <value name="VALUE-0">
                            <block type="CurrentArrayElement" id="45}SEAeWU{+C/5tG]JK{"></block>
                          </value>
                          <value name="VALUE-1">
                            <block type="SoldierStateBoolItem" id="hjk*`B?UIvhgqhEPmUMa">
                              <field name="VALUE-0">SoldierStateBool</field>
                              <field name="VALUE-1">IsDead</field>
                            </block>
                          </value>
                        </block>
                      </value>
                    </block>
                  </value>
                </block>
              </value>
            </block>
          </value>
        </block>
      </statement>
      <statement name="ACTIONS">
        <block type="ForceSpawnAllPlayers" id="uY5)j%{tr9ge3C81/vm:"></block>
      </statement>
      <next>
        <block type="ruleBlock" id="d2G1H7eL)bJvki;}GRPk">
          <mutation isOnGoingEvent="false"></mutation>
          <field name="NAME">Prevent Spawn</field>
          <field name="EVENTTYPE">OnPlayerDied</field>
          <statement name="CONDITIONS">
            <block type="conditionBlock" id=".dR(V6Qb0f[%lk67*:P$">
              <value name="CONDITION">
                <block type="Equals" id="oz]-wqPIUY^#{fkZ?)kW">
                  <value name="VALUE-0">
                    <block type="GetTeamId" id="hc+-lXJhKZ#0,!g=S4~W">
                      <value name="VALUE-0">
                        <block type="Number" id="S/LAj@zawtq,(FIvz`U*">
                          <field name="NUM">1</field>
                        </block>
                      </value>
                    </block>
                  </value>
                  <value name="VALUE-1">
                    <block type="GetTeamId" id="Bz2*{_mCRD=RdYN#mIUe">
                      <value name="VALUE-0">
                        <block type="EventPlayer" id="6uU-%!/a_z(!v+CDvc.U"></block>
                      </value>
                    </block>
                  </value>
                </block>
              </value>
            </block>
          </statement>
          <statement name="ACTIONS">
            <block type="SetSpawnOverride" id="3~M;62gnN%zhXuoQ*_^f">
              <value name="VALUE-0">
                <block type="EventPlayer" id="t^_Otpk/#$Jwy7lY?1r9"></block>
              </value>
              <value name="VALUE-1">
                <block type="Boolean" id="`K2%Y*;s^3%BX*VS%z`5">
                  <field name="BOOL">FALSE</field>
                </block>
              </value>
            </block>
          </statement>
        </block>
      </next>
    </block>
  </statement>
</block>
```
## Example 2
Set the primary weapon of Team 2 to the 12M Auto from Battlefield 2042

```blocky
<block xmlns="https://developers.google.com/blockly/xml" type="subroutineBlock" id="IIUjuG$5ddEhC*iw[FS-" deletable="false">
  <field name="SUBROUTINE_NAME">Demo</field>
  <statement name="ACTIONS">
    <block type="SetVariable" id="$H,6A-$rcv_]P!Kz*4On">
      <value name="VALUE-0">
        <block type="variableReferenceBlock" id="m)z#3Sy=r1tC~0~v.d!p">
          <mutation isObjectVar="false"></mutation>
          <field name="OBJECTTYPE">Global</field>
          <field name="VAR" id="jFbshv)sO5|11uF.(.9{" variabletype="Global">players</field>
        </block>
      </value>
      <value name="VALUE-1">
        <block type="FilteredArray" id="Mx3AU9*E|b8[,B?G0]FI">
          <value name="VALUE-0">
            <block type="AllPlayers" id="(KF/TI]!3WA@b4z3ILk)"></block>
          </value>
          <value name="VALUE-1">
            <block type="Equals" id="lN8xmrVXDTj^c~ja9w{5">
              <value name="VALUE-0">
                <block type="GetTeamId" id="/GxI73TG=#U}*_QSryLg">
                  <value name="VALUE-0">
                    <block type="Number" id="QQ(~?gH~[Td3OSn*CXOQ">
                      <field name="NUM">1</field>
                    </block>
                  </value>
                </block>
              </value>
              <value name="VALUE-1">
                <block type="GetTeamId" id="qqxj+8eJ4WgCI7c?^z7S">
                  <value name="VALUE-0">
                    <block type="EventPlayer" id="z6,+PTKf$Dxbt`]]2fH+"></block>
                  </value>
                </block>
              </value>
            </block>
          </value>
        </block>
      </value>
      <next>
        <block type="ForVariable" id="$tdeEP$URBaSNL84YjBN">
          <value name="VALUE-0">
            <block type="variableReferenceBlock" id=".=hfUCb72ccPjG7SObJJ">
              <mutation isObjectVar="false"></mutation>
              <field name="OBJECTTYPE">Global</field>
              <field name="VAR" id="jFbshv)sO5|11uF.(.9{" variabletype="Global">players</field>
            </block>
          </value>
          <value name="VALUE-1">
            <block type="Number" id="k5`E=isH0j7i6GRqyxDQ">
              <field name="NUM">123</field>
            </block>
          </value>
          <value name="VALUE-2">
            <block type="CountOf" id="qb@T2r5u}C/n-Os9!_oQ">
              <value name="VALUE-0">
                <block type="FilteredArray" id="ody7Y|]@W58)uePX@b,m">
                  <value name="VALUE-0">
                    <block type="AllPlayers" id="tkv!:tVP,p$$3y]6L#,u"></block>
                  </value>
                  <value name="VALUE-1">
                    <block type="Equals" id="~fTzs!SH(QdE2=_F-AWW">
                      <value name="VALUE-0">
                        <block type="GetTeamId" id="s]HFIRGvV]frBcI^8zTP">
                          <value name="VALUE-0">
                            <block type="Number" id="9xkJPs^4J4]*x)m9OT$!">
                              <field name="NUM">2</field>
                            </block>
                          </value>
                        </block>
                      </value>
                      <value name="VALUE-1">
                        <block type="GetTeamId" id="nl?2[_~6IdXFPk}vKf}|">
                          <value name="VALUE-0">
                            <block type="EventPlayer" id="(Ndg,*gr1YYUT{a+Xm8y"></block>
                          </value>
                        </block>
                      </value>
                    </block>
                  </value>
                </block>
              </value>
            </block>
          </value>
          <statement name="DO">
            <block type="AddSoldierWeapon" id="d@)sdVuLdE2VJ0;V/!D5">
              <value name="VALUE-0">
                <block type="CurrentArrayElement" id="4}h~CKYd!Y^I[a_-%_()"></block>
              </value>
              <value name="VALUE-1">
                <block type="PrimaryWeaponsItem" id="$yL6IY~6F/g0yw?*%cwS">
                  <field name="VALUE-0">PrimaryWeaponsKingston</field>
                  <field name="VALUE-1">Saiga12</field>
                </block>
              </value>
            </block>
          </statement>
        </block>
      </next>
    </block>
  </statement>
</block>
```

# Author
Mailstorm#2920
