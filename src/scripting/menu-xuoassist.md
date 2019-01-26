# Menu

### Command Format

**NameSpace**.**name**(_**requiredParameters**_, [_optionalParameters=defaultValue_]);

***

- void Client.InfoMenu();

Display information about the content of the last menu in the journal that came from the server.

index - gump index, -1 or lastmenu will display information about last gump ( if it was there ).

***

- void Client.WaitMenu('prompt', 'choice');

Waiting for the menu with the title 'prompt' to select object 'choice'.

Choice can be numeric, it will chose a choice according to its index. You can also use 'random' - to get a random one.

***

- void Client.CancelWaitMenu();

Cancel the menu waiting.

***

- int Client.MenuCount();

Information about the number of open menus.

Result: the amount of open menus.

***

- MenuObject Client.GetMenu('nameOrIndex');

Get the menu object by name/index.

Result: the object of type MenuObject or null if the menu with the specified name or index does not exist.

***

- void Client.SelectMenu('name', 'itemName');

Make a choice in the client's open menu - 'name' of the item that named itemName.

***

- void Client.CloseMenu('name');

Close the open menu 'name' in the client.

***

- bool Client.WaitForMenu([delay=1000]);

Awaits ( blocks execution ) for a menu for a given 'delay' of time in ms.

Returns true is a menu was received during the given delay.