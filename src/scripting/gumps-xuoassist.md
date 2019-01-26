# Gumps

### Command Format

**NameSpace**.**name**(_**requiredParameters**_, [_optionalParameters=defaultValue_]);

***

- void Client.HelpGump();

Request for the help menu gump of the server.

***

- void Client.InfoGump([index=-1]);

Outputs data of a gump by its index. If index equals -1, last gump is taken.

***

- GumpHookObjects Client.CreateGumpHook('index');

Creates a gump hook object.

index - Return-value of gump button or 'cancel' or a 0 when closing a gump with RMB.

***

- void Client.WaitGump(hook);

Enables a gump hook to catch an incomming gump.

When new hook is enabled by Client.WaitGump, it will be added to a stack. All previously enabled hooks will be waiting as well.

hook - an object created by Client.CreateGumpHook.

***

- void Client.CancelWaitGump();

Removes **all **enabled gump hooks .

***

- int Client.GumpCount();

Returns the amount of opened gumps from OA memory.

***

- GumpObject Client.GetLastGump();

Get last gump sent by server.

Returns a GumpObject or a null reference.

***

- GumpObject Client.GetGump(index);

Get gump by an index.

Returns a GumpObject or a null reference.

***

- GumpObject Client.GetGump(serial, id);

Get gump by serial and id.

Returns a GumpObject or a null reference.

***

- bool Client.WaitForGump([delay=1000]);

Enables a gump hook and blocks thread for 'delay' amount of time in ms. Removes gump hook afterwards.

Returns true if a gump was received during delay period.
