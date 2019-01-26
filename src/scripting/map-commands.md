# Map

### Command Format

NameSpace.name(requiredParameters, [optionalParameters=defaultValue]);

***

- void Client.OpenMap([x, y]);

Opens Client map.

If x and y were defined, moves map window to given screen coordinates.

***

- void Client.MoveMap(x, y);

Moves map to given screen coordinates.

***

- void Client.CloseMap();

Close Client map.

***

- void Client.OpenEnhancedMap(['filePath']);

Opens Enchanced Map at 'filePath' (for example "D:\Games\UO\EnhancedMap.exe").

If 'filePath' wasn't defined, tries to open from a default location <UORoot>/Map/EnhancedMap.exe'
