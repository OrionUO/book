# Context Menu

### Command Format

NameSpace.name(requiredParameters, [optionalParameters=defaultValue]);

***

- void Client.RequestContextMenu('serial');

Send a context menu request for given serial.

***

- void Client.WaitContextMenu('serial', index);

Add context menu wait hook.

- serial - serial of context menu object. If serial equals 0, serial check will be ignored.

- index - index of context menu choice, starting with 0.

***

- void Client.CancelContextMenu();

Cancel all context menu hooks.

***

- bool Client.WaitForContextMenu([delay=1000]);

Awaits context menu for 'delay' amount of time in ms.

Returns true is context menu was received during this period.
