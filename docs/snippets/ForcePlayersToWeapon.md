# Force players to a weapon

This snippet is used in Gun Master mode to force players to have an exact weapon of mode creator's choice. 

### Problem
In a current Portal's Rules Editor build, there is no way to remove a certain (or all) weapons from player's inventory, no way to empty out the inventory slots. You can only add a certain weapon by replacing it in a specific slot (see [ReplacePlayerInventory block](/docs/blocks/ReplacePlayerInventory))

### Prerequisites
1. Disable ALL weapons and gadgets. 

It might not be necessary, but will be useful since the code runs only after a full deploy (including the camera animation), so the player can technically use his current loadout before this swap happened. Also, this way players won't see any weapons on a deploy screen.

### Downsides
1. There is no way to determine the exact weapon player's using, because the function is not present in Rules Editor yet. *You have to track it down manually with variables, if you need to.*
2. Melee weapon will still be present for the melee fight (F key by default) and for finishers, even though it is not present in a slot. There is no way to have player without a knife. It won't be possible to switch to its slot though. There is also no way to determine a melle kill because of that.

## Code

### Disable all inventory
> This subroutine will ensure that the player cannot switch to another weapon slot. 

```blockly
<block
	xmlns="https://developers.google.com/blockly/xml" type="subroutineBlock" deletable="false" x="471" y="652">
	<field name="SUBROUTINE_NAME">DisableAllInventory</field>
	<statement name="ACTIONS">
		<block type="EnableInputRestriction">
			<value name="VALUE-0">
				<block type="EventPlayer"/>
			</value>
			<value name="VALUE-1">
				<block type="RestrictedInputsItem">
					<field name="VALUE-0">RestrictedInputs</field>
					<field name="VALUE-1">SelectCharacterGadget</field>
				</block>
			</value>
			<value name="VALUE-2">
				<block type="Boolean">
					<field name="BOOL">TRUE</field>
				</block>
			</value>
			<next>
				<block type="EnableInputRestriction">
					<value name="VALUE-0">
						<block type="EventPlayer"/>
					</value>
					<value name="VALUE-1">
						<block type="RestrictedInputsItem">
							<field name="VALUE-0">RestrictedInputs</field>
							<field name="VALUE-1">SelectMelee</field>
						</block>
					</value>
					<value name="VALUE-2">
						<block type="Boolean">
							<field name="BOOL">TRUE</field>
						</block>
					</value>
					<next>
						<block type="EnableInputRestriction">
							<value name="VALUE-0">
								<block type="EventPlayer"/>
							</value>
							<value name="VALUE-1">
								<block type="RestrictedInputsItem">
									<field name="VALUE-0">RestrictedInputs</field>
									<field name="VALUE-1">SelectOpenGadget</field>
								</block>
							</value>
							<value name="VALUE-2">
								<block type="Boolean">
									<field name="BOOL">TRUE</field>
								</block>
							</value>
							<next>
								<block type="EnableInputRestriction">
									<value name="VALUE-0">
										<block type="EventPlayer"/>
									</value>
									<value name="VALUE-1">
										<block type="RestrictedInputsItem">
											<field name="VALUE-0">RestrictedInputs</field>
											<field name="VALUE-1">SelectPrimary</field>
										</block>
									</value>
									<value name="VALUE-2">
										<block type="Boolean">
											<field name="BOOL">TRUE</field>
										</block>
									</value>
									<next>
										<block type="EnableInputRestriction">
											<value name="VALUE-0">
												<block type="EventPlayer"/>
											</value>
											<value name="VALUE-1">
												<block type="RestrictedInputsItem">
													<field name="VALUE-0">RestrictedInputs</field>
													<field name="VALUE-1">SelectSecondary</field>
												</block>
											</value>
											<value name="VALUE-2">
												<block type="Boolean">
													<field name="BOOL">TRUE</field>
												</block>
											</value>
											<next>
												<block type="EnableInputRestriction">
													<value name="VALUE-0">
														<block type="EventPlayer"/>
													</value>
													<value name="VALUE-1">
														<block type="RestrictedInputsItem">
															<field name="VALUE-0">RestrictedInputs</field>
															<field name="VALUE-1">SelectThrowable</field>
														</block>
													</value>
													<value name="VALUE-2">
														<block type="Boolean">
															<field name="BOOL">TRUE</field>
														</block>
													</value>
													<next>
														<block type="EnableInputRestriction">
															<value name="VALUE-0">
																<block type="EventPlayer"/>
															</value>
															<value name="VALUE-1">
																<block type="RestrictedInputsItem">
																	<field name="VALUE-0">RestrictedInputs</field>
																	<field name="VALUE-1">CyclePrimary</field>
																</block>
															</value>
															<value name="VALUE-2">
																<block type="Boolean">
																	<field name="BOOL">TRUE</field>
																</block>
															</value>
															<next>
																<block type="EnableInputRestriction">
																	<value name="VALUE-0">
																		<block type="EventPlayer"/>
																	</value>
																	<value name="VALUE-1">
																		<block type="RestrictedInputsItem">
																			<field name="VALUE-0">RestrictedInputs</field>
																			<field name="VALUE-1">CycleSecondary</field>
																		</block>
																	</value>
																	<value name="VALUE-2">
																		<block type="Boolean">
																			<field name="BOOL">TRUE</field>
																		</block>
																	</value>
																	<next>
																		<block type="EnableInputRestriction">
																			<value name="VALUE-0">
																				<block type="EventPlayer"/>
																			</value>
																			<value name="VALUE-1">
																				<block type="RestrictedInputsItem">
																					<field name="VALUE-0">RestrictedInputs</field>
																					<field name="VALUE-1">CycleAbilityDown</field>
																				</block>
																			</value>
																			<value name="VALUE-2">
																				<block type="Boolean">
																					<field name="BOOL">TRUE</field>
																				</block>
																			</value>
																			<next>
																				<block type="EnableInputRestriction">
																					<value name="VALUE-0">
																						<block type="EventPlayer"/>
																					</value>
																					<value name="VALUE-1">
																						<block type="RestrictedInputsItem">
																							<field name="VALUE-0">RestrictedInputs</field>
																							<field name="VALUE-1">CycleAbilityUp</field>
																						</block>
																					</value>
																					<value name="VALUE-2">
																						<block type="Boolean">
																							<field name="BOOL">TRUE</field>
																						</block>
																					</value>
																					<next>
																						<block type="Wait">
																							<value name="VALUE-0">
																								<block type="Number">
																									<field name="NUM">0.1</field>
																								</block>
																							</value>
																						</block>
																					</next>
																				</block>
																			</next>
																		</block>
																	</next>
																</block>
															</next>
														</block>
													</next>
												</block>
											</next>
										</block>
									</next>
								</block>
							</next>
						</block>
					</next>
				</block>
			</next>
		</block>
	</statement>
</block>

```

### Empty all weapons

> This subroutine will ensure that the player cannot choose other slots, because they will be out of ammo. `DisableAllInventory` accompanies this subroutine to prevent switching, but it won't prevent from the switch once your forced weapon is run out of ammo.

```blockly
<block
	xmlns="https://developers.google.com/blockly/xml" type="subroutineBlock" deletable="false" x="-621" y="114">
	<field name="SUBROUTINE_NAME">EmptyAllWeapons</field>
	<statement name="ACTIONS">
		<block type="SetInventoryMagazineAmmo">
			<value name="VALUE-0">
				<block type="EventPlayer"/>
			</value>
			<value name="VALUE-1">
				<block type="InventorySlotsItem">
					<field name="VALUE-0">InventorySlots</field>
					<field name="VALUE-1">CharacterGadget</field>
				</block>
			</value>
			<value name="VALUE-2">
				<block type="Number">
					<field name="NUM">0</field>
				</block>
			</value>
			<next>
				<block type="SetInventoryMagazineAmmo">
					<value name="VALUE-0">
						<block type="EventPlayer"/>
					</value>
					<value name="VALUE-1">
						<block type="InventorySlotsItem">
							<field name="VALUE-0">InventorySlots</field>
							<field name="VALUE-1">MeleeWeapon</field>
						</block>
					</value>
					<value name="VALUE-2">
						<block type="Number">
							<field name="NUM">0</field>
						</block>
					</value>
					<next>
						<block type="SetInventoryMagazineAmmo">
							<value name="VALUE-0">
								<block type="EventPlayer"/>
							</value>
							<value name="VALUE-1">
								<block type="InventorySlotsItem">
									<field name="VALUE-0">InventorySlots</field>
									<field name="VALUE-1">OpenGadget</field>
								</block>
							</value>
							<value name="VALUE-2">
								<block type="Number">
									<field name="NUM">0</field>
								</block>
							</value>
							<next>
								<block type="SetInventoryMagazineAmmo">
									<value name="VALUE-0">
										<block type="EventPlayer"/>
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
									<next>
										<block type="SetInventoryMagazineAmmo">
											<value name="VALUE-0">
												<block type="EventPlayer"/>
											</value>
											<value name="VALUE-1">
												<block type="InventorySlotsItem">
													<field name="VALUE-0">InventorySlots</field>
													<field name="VALUE-1">SecondaryWeapon</field>
												</block>
											</value>
											<value name="VALUE-2">
												<block type="Number">
													<field name="NUM">0</field>
												</block>
											</value>
											<next>
												<block type="SetInventoryMagazineAmmo">
													<value name="VALUE-0">
														<block type="EventPlayer"/>
													</value>
													<value name="VALUE-1">
														<block type="InventorySlotsItem">
															<field name="VALUE-0">InventorySlots</field>
															<field name="VALUE-1">Throwable</field>
														</block>
													</value>
													<value name="VALUE-2">
														<block type="Number">
															<field name="NUM">0</field>
														</block>
													</value>
													<next>
														<block type="Wait">
															<value name="VALUE-0">
																<block type="Number">
																	<field name="NUM">0.1</field>
																</block>
															</value>
															<next>
																<block type="SetInventoryAmmo">
																	<value name="VALUE-0">
																		<block type="EventPlayer"/>
																	</value>
																	<value name="VALUE-1">
																		<block type="InventorySlotsItem">
																			<field name="VALUE-0">InventorySlots</field>
																			<field name="VALUE-1">CharacterGadget</field>
																		</block>
																	</value>
																	<value name="VALUE-2">
																		<block type="Number">
																			<field name="NUM">0</field>
																		</block>
																	</value>
																	<next>
																		<block type="SetInventoryAmmo">
																			<value name="VALUE-0">
																				<block type="EventPlayer"/>
																			</value>
																			<value name="VALUE-1">
																				<block type="InventorySlotsItem">
																					<field name="VALUE-0">InventorySlots</field>
																					<field name="VALUE-1">MeleeWeapon</field>
																				</block>
																			</value>
																			<value name="VALUE-2">
																				<block type="Number">
																					<field name="NUM">0</field>
																				</block>
																			</value>
																			<next>
																				<block type="SetInventoryAmmo">
																					<value name="VALUE-0">
																						<block type="EventPlayer"/>
																					</value>
																					<value name="VALUE-1">
																						<block type="InventorySlotsItem">
																							<field name="VALUE-0">InventorySlots</field>
																							<field name="VALUE-1">OpenGadget</field>
																						</block>
																					</value>
																					<value name="VALUE-2">
																						<block type="Number">
																							<field name="NUM">0</field>
																						</block>
																					</value>
																					<next>
																						<block type="SetInventoryAmmo">
																							<value name="VALUE-0">
																								<block type="EventPlayer"/>
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
																							<next>
																								<block type="SetInventoryAmmo">
																									<value name="VALUE-0">
																										<block type="EventPlayer"/>
																									</value>
																									<value name="VALUE-1">
																										<block type="InventorySlotsItem">
																											<field name="VALUE-0">InventorySlots</field>
																											<field name="VALUE-1">SecondaryWeapon</field>
																										</block>
																									</value>
																									<value name="VALUE-2">
																										<block type="Number">
																											<field name="NUM">0</field>
																										</block>
																									</value>
																									<next>
																										<block type="SetInventoryAmmo">
																											<value name="VALUE-0">
																												<block type="EventPlayer"/>
																											</value>
																											<value name="VALUE-1">
																												<block type="InventorySlotsItem">
																													<field name="VALUE-0">InventorySlots</field>
																													<field name="VALUE-1">Throwable</field>
																												</block>
																											</value>
																											<value name="VALUE-2">
																												<block type="Number">
																													<field name="NUM">0</field>
																												</block>
																											</value>
																											<next>
																												<block type="Wait">
																													<value name="VALUE-0">
																														<block type="Number">
																															<field name="NUM">0.1</field>
																														</block>
																													</value>
																												</block>
																											</next>
																										</block>
																									</next>
																								</block>
																							</next>
																						</block>
																					</next>
																				</block>
																			</next>
																		</block>
																	</next>
																</block>
															</next>
														</block>
													</next>
												</block>
											</next>
										</block>
									</next>
								</block>
							</next>
						</block>
					</next>
				</block>
			</next>
		</block>
	</statement>
</block>
```

### Give a weapon

> Gives a specific weapon, gives a maximum amount of ammo in the inventory and a currently used mazagine. `EnableInputRestrictions` are used to prevent from doing weird stuff.
> 
> *NOTE: This code will produce error messages for weapons without ability to hold ammo. It doesn't affect its work though for other weapons.*

```blockly
<block
	xmlns="https://developers.google.com/blockly/xml" type="subroutineBlock" deletable="false" x="477" y="-165">
	<field name="SUBROUTINE_NAME">GiveWeapon</field>
	<statement name="ACTIONS">
		<block type="EnableInputRestriction">
			<value name="VALUE-0">
				<block type="EventPlayer"/>
			</value>
			<value name="VALUE-1">
				<block type="RestrictedInputsItem">
					<field name="VALUE-0">RestrictedInputs</field>
					<field name="VALUE-1">FireWeapon</field>
				</block>
			</value>
			<value name="VALUE-2">
				<block type="Boolean">
					<field name="BOOL">TRUE</field>
				</block>
			</value>
			<next>
				<block type="subroutineInstanceBlock">
					<field name="SUBROUTINE_NAME">EmptyAllWeapons</field>
					<next>
						<block type="AddSoldierWeapon">
							<value name="VALUE-0">
								<block type="EventPlayer"/>
							</value>
							<value name="VALUE-1">
								<block type="PrimaryWeaponsItem">
									<field name="VALUE-0">PrimaryWeaponsAlexandria</field>
									<field name="VALUE-1">A-91</field>
								</block>
							</value>
							<next>
								<block type="SetInventoryAmmo">
									<value name="VALUE-0">
										<block type="EventPlayer"/>
									</value>
									<value name="VALUE-1">
										<block type="InventorySlotsItem">
											<field name="VALUE-0">InventorySlots</field>
											<field name="VALUE-1">PrimaryWeapon</field>
										</block>
									</value>
									<value name="VALUE-2">
										<block type="Number">
											<field name="NUM">999</field>
										</block>
									</value>
									<next>
										<block type="SetInventoryMagazineAmmo">
											<value name="VALUE-0">
												<block type="EventPlayer"/>
											</value>
											<value name="VALUE-1">
												<block type="InventorySlotsItem">
													<field name="VALUE-0">InventorySlots</field>
													<field name="VALUE-1">PrimaryWeapon</field>
												</block>
											</value>
											<value name="VALUE-2">
												<block type="Number">
													<field name="NUM">999</field>
												</block>
											</value>
											<next>
												<block type="ForceSwitchInventory">
													<value name="VALUE-0">
														<block type="EventPlayer"/>
													</value>
													<value name="VALUE-1">
														<block type="InventorySlotsItem">
															<field name="VALUE-0">InventorySlots</field>
															<field name="VALUE-1">PrimaryWeapon</field>
														</block>
													</value>
													<next>
														<block type="EnableInputRestriction">
															<value name="VALUE-0">
																<block type="EventPlayer"/>
															</value>
															<value name="VALUE-1">
																<block type="RestrictedInputsItem">
																	<field name="VALUE-0">RestrictedInputs</field>
																	<field name="VALUE-1">FireWeapon</field>
																</block>
															</value>
															<value name="VALUE-2">
																<block type="Boolean">
																	<field name="BOOL">FALSE</field>
																</block>
															</value>
															<next>
																<block type="Wait">
																	<value name="VALUE-0">
																		<block type="Number">
																			<field name="NUM">0.1</field>
																		</block>
																	</value>
																</block>
															</next>
														</block>
													</next>
												</block>
											</next>
										</block>
									</next>
								</block>
							</next>
						</block>
					</next>
				</block>
			</next>
		</block>
	</statement>
</block>
```

### Author
@cjmaxik, "Gun Master - BF2042 Rendition" experience