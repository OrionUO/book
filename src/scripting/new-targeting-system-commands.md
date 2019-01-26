# New Targeting System

Targeting this way works faster because there's no target awaiting time after any action request. The server receives action to do and target for this action with in a single packet.

### Command Format

NameSpace.name(requiredParameters, [optionalParameters=defaultValue]);

***

- void Client.BandageTarget('serial');

Apply bandage to target by serial.

***

- void Client.CastTarget('nameOrIndex', 'serial');

Cast a spell on target by serial.

***

- void Client.UseSkillTarget('nameOrIndex', 'serial');

Use a skill on target by serial.