# Setup Visual Studio with PerlTidy

Turns out adding Perltidy to Visual Studio was fairly painless.

Open the Tools | External Tools menu item

Add the following against the various parameters.

Title: Perltidy
Command: C:\Perl64\site\bin\perltidy.bat
Arguments: -b -bext='/' $(ItemPath)
Initial directory: <blank>
Check "Use Output window"
Leave others unchecked ("Treat output as Unicode", "Prompt for arguments")

NB: $(ItemPath) is a variable pointing to the full path and filename for the current code (i.e. perl script).
    Ref: https://msdn.microsoft.com/en-us/library/76712d27.aspx#Arguments for external tools

And done!
