# Objects

### Command Format

**NameSpace**.**name**(_**requiredParameters**_, [_optionalParameters=defaultValue_]);

***

- void Client.Info(['serial'=targetRequest]);

Display information about the object "serial" in a text box.

Request target to be aimed at the desired object, if parameters were not specified.

***

- void Client.InfoTile(['lasttile'=targetRequest]);

Display information about 'lasttile' (tile, on which target was selected last time ) in the text box.

Request target to be aimed at the desired tile, if parameters were not specified.

***

- String Client.GetSerial('serial');

Returns real value of the serial.

For instance: Client.GetSerial(self) or Client.GetSerial(lastcontainer) - will return the serial of the player 0x12345678

***

- String Client.GetGraphic('graphic');

Return real value of "graphic".

For instance: Client.GetGraphic('bm') - will return type of blood moss, stated in Lists/Types

***

- String Client.GetContainer('serial');

Return serial of the object, in which an object with "serial" is located.

Client.GetContainer(self) will return 0xFFFFFFFF (worlds serial) or Client.GetContainer(backpack) - will return serial of the player 0x12345678, since backpack container is the player, who's owning it.

***

- void Client.Click(['serial'=self]);

Request click for the object serial.

***

- void Client.UseObject(['serial'=self]);

Request to use (doubleclick) the object serial.

***

- void Client.GetStatus(['serial'=self]);

Request for the object serial status.

***

- void Client.Attack('serial');

Request to attack the object serial.

***

- void Client.Hide(['serial'=targetRequest]);

Hide the object serial.

Request target selection for the object indication, if parameters were not specified.

***

- void Client.RenameMount('serial', 'new name');

Rename your mount "serial".

***

- void Client.Drop(['serial'=targetRequest], [count=0(all)], [x=-1, y=-1, z=0]);

Drop the item 'serial' with amount 'count' into coordinates x, y, z ; Use target if parameters were not specified.

***

- void Client.DropHere(['serial'=targetRequest], [count=0(all)]);

Drop the item 'serial' under the character with amount 'count'. Request target to be aimed at the desired object, if parameters were not specified.

***

- void Client.MoveItem(['serial'=targetRequest], [count=0(all)], ['container'=backpack], [x=-1, y=-1], [z=0]);

Move the object 'serial' with amount 'count' to the container 'container' into coordinates x, y, z (z when throwing on the ground), use target if parameters were not specified.

***

- int Client.GetDistance('serial');

Return distance to the object.

***

- int Client.GetDistance(x, y);

Return distance to the coordinates.

***

- void Client.BandageSelf();

Bandageself.

***

- String ClientLastTarget();

Get the state of the global client variable LastTarget.

Result: The string with the serial.

***

- void ClientLastTarget(serial);

Set the state of the client global variable LastTarget to the serial.

***

- String ClientLastAttack();

Get the state of the global client variable LastAttack

Result: The string with the serial.

***

- void ClientLastAttack(serial);

Set the state of the global client variable LastAttack to the serial.

***

- String TargetSystemSerial();

Get the state of the global client variable TargetSystemSerial (from new target system).

Result: The string with the serial.

***

- void TargetSystemSerial(serial);

Set the state of the global client variable TargetSystemSerial (from new target system) to the serial.

***

- void Client.GetFriendsStatus();

Retrieves statuses of all friends in update range ( required to get updates about their hp etc. ).

***

- void Client.GetEnemiesStatus();

Retrieves statuses of all enemies in update range ( required to get updates about their hp etc. ).

***

- PositionObject Client.GetLastTargetPosition();

Retrieves latest coordinates of LastTarget, if object has disappeared - it will retrieve last known coordinates.

Returns: a PositionObject data type.

***

- PositionObject Client.GetLastAttackPosition();

Retrieves latest coordinates of LastAttack, if object has disappeared - it will retrieve last known coordinates.

Returns: a PositionObject data type.

***

- bool Client.OpenContainer('serial', ['delay'=600], ['errorTextPattern']);

Open container.

- serial - serial of the container we're opening.

- delay - Maximum delay for container opening action.

- errorTextPattern - Error text. Default: 'reach that|too away'.

Returns: true if container was opened successfully.

***

- bool Client.ObjectExists('serial');

Returns: true if object with 'serial' is present in OA memory.

***

- String Client.RequestName('serial', ['delay'=200]);

Requests objects name. If the name is already present, it will return immediately. Otherwise name will be requested from the server.

- serial - serial of the object we're requesting name from.

- delay - Max delay for name requesting.

Returns: Objects name or an empty string if failed.

***

- bool Client.GetProfile('serial', ['delay'=300], ['errorTextPattern']);

Retrieves characters profile.

- serial - characters serial.

- delay - maximum wait time for profile retrievement.

- errorTextPattern - error pattern, default: 'reach that|too away'.

Returns true if a profile was retrieved.

***

- void Client.ShowStatusbar('serial', x, y, [minimized=true]);

Show/Move status bar gump in client screen.

serial - character serial.

x - screen X coordinate.

y - screen Y coordinate.

minimized - only for your character. true will show minimized status bar, false will show expanded one.

***

- void Client.CloseStatusbar('serial');

Close status bar which belongs to serial.


