# Collections

### Command Format

**NameSpace**.**name**(_**requiredParameters**_, [_optionalParameters=defaultValue_]);

***

- void Client.AddType('typeName', ['typeValue'=targetRequest]);

Add type or select type (if typeValue isn't suggested).

***

- void Client.RemoveType('typeName');

Delete type.

***

- void Client.AddObject('objectName', ['objectValue'=targetRequest]);

Add object or select object (if objectValue isn't suggested)

***

- void Client.RemoveObject('objectName');

Delete object.

***

- void Client.AddFindList(['listName'=targetRequest], ['graphic', 'color'], ['comment']);

Add object properties or select to add object properties to Find list.

- - listName - list name. If not suggested - target selection appears to add properties to the currently selected element from the list(on the list tab), without auto-save.
- - graphic - object type.
- - color- object color.
- - comment - a comment, which will be displayed in the list.

***

- void Client.ClearFindList('listName');

Delete search list with all it's content.

- - listName - list name.

***

- void Client.AddIgnoreListObject(['listName'=targetRequest], ['serial'], ['comment']);

Add object to ignore list.

- - listName - list name.
- - serial - serial of the object..
- - comment - a comment, which will be displayed in the list.

***

- void Client.AddIgnoreList(['listName'=targetRequest], ['graphic', 'color'], ['comment']);

Add object properties or target selection appears to add object properties to the ignore list.

- - listName - list name. If not suggested - target selection appears to add properties to the currently selected element from the list(on the list tab), without auto-save
- - graphic - Тип объекта.
- - color- object color.
- - comment - a comment, which will be displayed in the list.

***

- void Client.ClearIgnoreList('listName');

Delete search list with all it's content.

- - listName - list name.

***

- StringList Client.GetFriendList();

Return string list with friends id's.

***

- StringList Client.GetEnemyList();

Return string list with enemies id's.

***

- void Client.AddFriend('friendName', ['serial'=targetRequest]);

Add a friend or select one to add by a target if there's no 'serial' argument.

***

- void Client.RemoveFriend('friendName');

Remove a friend from friends list.

***

- void Client.ClearFriendList();

Clear friends list.
***

- void Client.AddEnemy('enemyName', ['serial'=targetRequest]);

Add an enemy or select one to add by a target if there's no 'serial' argument.

***

- void Client.RemoveEnemy('enemyName');

Remove an enemy from enemies list.

***

- void Client.ClearEnemyList();

Clear enemies list.

***

- void Client.SetGlobal(name, value);

Set a global variable. Value data type is always a string.

***

- String Client.GetGlobal(name);

Retrieve value ( string data type ) of a global variable

Returns value of the variable or an empty string is no variable is found with such name.

***

- void Client.ClearGlobals();

Clear global variables list.