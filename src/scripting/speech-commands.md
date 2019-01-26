# Speech

### Command Format

NameSpace.name(requiredParameters, [optionalParameters=defaultValue]);

***

- void Client.Print(['color'], 'text');

Prints 'text' string into system chat.

If only 'text' string was passed, default color [no color] will be used.

color - message color.

text - message text.

***

- void Client.CharPrint('serial', 'color', 'text');

Print a message above character with given serial.

serial - given character serial.

color - message color.

text - message text.

***

- void Client.Say('text');

Display 'text' speech in client.

***

- void Client.SetFontColor(state, ['color'=0x02B2]);

Changes font color of YOUR character to given color argument ( if given ) and disables/enables this feature by state argument.

state - can be either true or false.

color - message color.

***

- bool Client.GetFontColor();

Returns state of Client.SetFontColor() option.

***

- String Client.GetFontColorValue();

Returns color value of Client.SetFontColor() option.

***

- void Client.SetCharactersFontColor(state, ['color'=0x02B2]);

Changes font color of all characters to a given color argument ( if given ) and disables/enables this feature by state argument.

state - can be either true or false.

color - message color.

***

- bool Client.GetCharactersFontColor();

Returns state of Client.SetCharactersFontColor() option.

***

- String Client.GetCharactersFontColorValue();

Returns color value of Client.SetCharactersFontColor() option.

***

- void Client.SayYell('some text');

Do 'yelling' speech.

***

- void Client.SayWhisper('some text');

Do 'whisper' speech.

***

- void Client.SayEmote('some text');

Do 'emote' speech.

***

- void Client.SayBroadcast('some text');

Do 'broadcast' speech.

***

- void Client.SayParty('some text');

Send 'text' to party chat.

***

- void Client.SayGuild('some text');

Send 'text' to guild chat.

***

- void Client.SayAlliance('some text');

Send 'text' to alliance chat.
