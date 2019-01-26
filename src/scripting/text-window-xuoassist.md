# Text Window

**TextWindow is a static reference just like `Client` so you can always get it.**

***

### Command Format

**NameSpace**.**name**(_**requiredParameters**_, [_optionalParameters=defaultValue_]);


***
- void TextWindow.Open();

Open the text box.

***

- void TextWindow.Close();

Close the text box.

***

- void TextWindow.Clear();

Clear the text box.

***

- void TextWindow.Print('text');

Type the text in the text box.

***

- void TextWindow.SetPos(x, y);

Move text windows to x and y screen coordinates.

***

- void TextWindow.SetSize(width, height);

Sets text windows size by given width and height.

***

- void TextWindow.SaveToFile('filePath');

Write contents of text windows into a file at filePath.