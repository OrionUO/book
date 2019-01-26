# Character Movement

### Command Format

**NameSpace**.**name**(_**requiredParameters**_, [_optionalParameters=defaultValue_]);

***

- void Client.BlockMoving(state);

Blocks character movement.

***

- bool Client.CanWalk(direction, x, y, z);

Check for the ability to take a step.

Result: true if you can step from the current coordinates (the turn is considered as a step).

***

- bool Client.Step(direction, [run=false]);

Request to move a character with the ability to run.

Result: true if the step was successfully made (the turn is considered as a step).

***

- bool Client.WalkTo(x, y, z, [distance=1]);

Path search to the specified coordinates until the specified distance is reached. Can be used within one screen.

Result: true if the destination or specified distance is reached.

***

- void Client.StopWalking();

Cancel the path search.

***

- bool Client.IsWalking();

Check: whether the character is currently moving (automatic movement).

Result: true if auto-movement is on.