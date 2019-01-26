# Prompt

### Command Format

NameSpace.name(requiredParameters, [optionalParameters=defaultValue]);

***

- void Client.WaitPrompt('text', 'serial'=0, 'type'=all);

Add a prompt hook.

- text - input text

- serial - serial of prompt object. If serial equals 0, serial check will be ignored.

- type - prompt type. all - all types; ascii - only ASCII prompts; unicode - only UNIDCODE prompts;

***

- void Client.CancelWaitPrompt();

Cancel all prompt hooks.

***

- bool Client.PrompsExists();

Returns true if a prompt is active.

***

- String Client.PromptSerial();

Returns prompt serial as string.

***

- String Client.PromptID();

Returns prompt id as string.

***

- void Client.SendPrompt('text');

Send prompt response ( if there's a prompt active ) with text input.
