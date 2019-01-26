# Interactions With Other Scripts

### Command Format

**NameSpace**.**name**(_**requiredParameters**_, [_optionalParameters=defaultValue_]);

***

- void Client.Wait('delay');

Wait delay (milliseconds).

In addition, the value can take in the parameter string constants: moveitemdelay, waittargetdelay, useitemdelay, keepcorpsedelay.

***

- int Client.Now();

Result: the current time in milliseconds.

***

- void Client.LoadScript('filePath');

Load the script file.

***

- void Client.Exec('functionName', [oneScriptRunning=false], [argumentsList]);

Start the function.

- - functionName - The name of the function to start.

- - oneScriptRunning - Check for a running instance of the function with the same name and prevent re-execution.

- - argumentsList - List of function parameters.

***

- void Client.Terminate('functionName', ['functionsSave']);

Terminate the script. The function name register is important !!!

- - functionName - The name of the function to be terminated. Ends all functions with that name. If 'all' is specified - exits all functions except those that were specified in functionsSave.

- - functionsSave - Functions that do not need to be terminated are indicated by '|' ; For example, Client.Terminate ('all', 'Heal | Loot | CheckMana') - terminates all working functions except Heal, Loot, CheckMana.

***

- bool Client.ScriptRunning('functionName');

Check if the script is already running.

Result: true if the script is running.

***

- void Client.Launch('filePath', [arguments]);

Launching of external program from 'filePath' with optional 'arguments'.

***

- bool Client.Contains(text, pattern, [ignoreCase=false]);

This function will check for a text pattern or a collection of patters ('patternOne|patternTwo|patternThree') within 'text' string.
Uses same logic as text searching in UO journal.

- - text - String with text to search within.

- - pattern - String with pattern(s) to search for.

- - ignoreCase - true - Ignore case is true by default.

Returns true if there's a match.

***

- StringList Client.Split(text, [separator=' '], [skipEmptyWord=true]);

This function will split 'text' string into a list of strings by separator character. Default is space character.

- - text - string of text to split.

- - separator - character used as a separator for text string.

- - skipEmptyWord - true - skips empty words by default.

Returns a list of strings.

***

- String Client.OAVersion();

Returns: Current version number of OA, for example "2.0.8.0".

***

- bool Client.Connected();

Returns: true if client is connected to a server and character is already in the world.

***

- String Client.Time(['format'=hh:mm:ss.zzz]);

Returns: current time, example "13:27:41.508".

***

- String Client.Date(['format'=dd.MM.yyyy]);

Returns: current date, example "26.05.2017".

***

- int Client.Random([value=2147483647]);

Returns: random value starting from 0 and up to value-1.

***

- int Client.Random(minValue, maxValue);

Returns: random value starting from minValue and up to maxValue-1.

***

- void Client.ActivateClient();

Activates client window.

***

- void Client.ShutdownWindows(['mode']);

Shuts down your PC :) can add flags as 'mode'.

***

- bool Client.OnOffHotkeys();

Get current state of hotkeys ( enabled/disabled )

Returns true if hotkeys are enabled, false if disabled.

***

- void Client.OnOffHotkeys(state);

Sets hotkeys state.