# Timers

### Command Format

NameSpace.name(requiredParameters, [optionalParameters=defaultValue]);

***

- bool Client.TimerExists('name');

Check if timer with given name exists.

Returns true if such timer exists.
***

- void Client.SetTimer('name', [delay=0]);

Create/Change timer with 'delay' as initial value. Default is 0.

***

- int Client.Timer('name');

Get current value of timer by name.

Returns -1 if such timer doesn't exist .

Returns time passed from timer initiation in ms.

***

- void Client.RemoveTimer('name');

Removes timer with a given name.

***

- void Client.ClearTimers();

Removes all existing timers.
