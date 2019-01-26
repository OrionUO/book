# Non Categorized

### Command Format

**NameSpace**.**name**(_**requiredParameters**_, [_optionalParameters=defaultValue_]);

***

- void Client.SaveConfig();

Save configuration.

***

- void Client.SetLight(state, [value=currentLight]);

Set the light level.

state - state turn on/turn off.

value - light level value from 0 to 31.

***

- void Client.SetWeather(state, [index=currentWeather], [effectsCount=currentCount], [temperature=currentTemperature]);

Set weather conditions.

state - state turn on/turn off.

index - ordinal number of the weather effect.

effectsCount - number of effects on screen.

temperature - not used.

***

- void Client.SetSeason(state, [index=currentIndex], [musicIndex=currentMusic]);

Set season with number.

state - state turn on/turn off.

index - ordinal number of season.

musicIndex - music number for playback.

***

- void Client.Track([state=false], [x=-1, y=-1]);

Hide/show quest arrow to the indicated coordinates. -1 in coordinates indicates current location in the world.

state - state show/hide.

x - coordinate X in the world, where the arrow points

y - coordinate Y в мире, where the arrow points

***

- bool Client.SaveHotkeys('fileName');

Save current hotkey set with file name 'filename' (to the Hotkeys folder at the root of the assistant).

Result: true on successful file save.

***

- bool Client.LoadHotkeys('fileName');

Load hotkey set with file name 'fileName' (from the Hotkeys folder at the root of the assistant).

Result: true on successful file load.

***

- void Client.Cast(spellIndex/'spellName', ['targetSerial']);

Cast a spell 'spellName' (You can also refer to the order number in the spellbook).

If targetSerial is specified - automatically use the target on this object, otherwise - only sends a cast request to the server.

***

- void Client.UseSkill(skillIndex/'skillName', ['targetSerial']);

Use skill 'skillName' (You can also refer to the order number).

If targetSerial is specified - automatically use the target on this object, otherwise - only sends a request to use skill to the server.

***

- int Client.SkillValue(skillIndex/'skillName', ['type'=real]);

Get skill value 'skillName' (You can also refer to the order number).

type - value type: real, base, cap, lock.

Result: Integer value of the skill (e.g: 3.0 will be 30, 10.3 - 103, 50.8 - 508, 100.0 - 1000).

***

- void Client.CloseUO();

Close game client.

***

- void Client.WarMode([state=switch]);

Switch war mode.

state - turn on/turn off war mode. If not specified - switches the current state.

***

- void Client.Morph(['graphic'=0]);

Change character body graphic.

Without parameters or 0 - returns body to its original state.

***

- void Client.Resend();

Synchronisation with the server. Can be used every few seconds.

***

- void Client.Sound(index);

Play sound index.

***

- void Client.EmoteAction('actionName');

Request to emotion reproducing  actionName.

***

- void Client.Print(['color'], 'text');

Display in system chat

If displayed only 1 argument - string color will be standard.

color - message color.

text - text.

***

- void Client.CharPrint('serial', 'color', 'text');

Display message above the character

serial - serial of the character, above who you want to display the message

color - message color

text - text.

***

- void Client.Say('text');

Say in the chat 'text'

***

- void Client.BuffExists('name');

Checking for buffs by name or graphic.

Result: true if buff is active.

***

- void Client.SetFontColor(state, ['color'=0x02B2]);

Change text color for player character and state of this option.

state - true/false.

color - text color.

***

- bool Client.GetFontColor();

Retrieve status of text replacement option for player character.

Returns true if option is enabled.

***

- String Client.GetFontColorValue();

Retrieve text replacement color for player character.

Returns: text color.

***

- void Client.SetCharactersFontColor(state, ['color'=0x02B2]);

Change text color used by characters for output and state of this option.

state - true/false.

color - text color.

***

- bool Client.GetCharactersFontColor();

Retrieve status of text replacement option for characters.

Returns true if option is enabled.

***

- String Client.GetCharactersFontColorValue();

Retrieve text replacement color for all characters.

Returns: text color.

***

- void Client.UseAbility('abilityName');

Use request for an ability 'abilityName'.

'abilityName' can also be 'Primary', 'Secondary', or its real name in(can also be found in script editor context menu) or it can be ability index starting from '0' and '30' as last index.

***

- void Client.UseWrestlingDisarm();

Wrestling Disarm ability use request.

***

- void Client.UseWrestlingStun();

Wrestling Stun ability use request..

***

- void Client.InvokeVirture('name');

...

***

- void Client.PlayWav('filePath');

Play a *.WAV file from filePath.

***

- void Client.Screenshot();

Create a screenshot.

***

- void Client.LogOut();

Client log out ( client will remain running, at login screen ).

***

-  MacroObject Client.CreateClientMacro(['action'], ['subAction']);

Create a macro in client options.

Returns MacroObject or null reference.
***

- void Client.OpenPaperdoll('serial');

Open paperdoll by serial.

***

- void Client.ClosePaperdoll('serial');

Close paperdoll by serial.

***

- void Client.MovePaperdoll('serial', x, y);

Move paperdoll by serial to chosen x and y coordinates on screen.

***

- void Client.ClientViewRange(range);

Set clients view range ( 5 is minimal, 25 is maximal ).

***

- int Client.ClientViewRange();

Get current client view range.

Returns clients view range in tiles.

***

- void Client.LoadProfile('name');

Load OA profile by name.