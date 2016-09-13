This is my DefaultParameter module. I created it primarily to let me store default parameter values like `Out-File:Encoding` and my `Publish-Module:NuGetApiKey` ...

You can install it from the PowerShell gallery:

```posh
Install-Module DefaultParameters
```

Then you can do something like this:

```posh
Set-DefaultParameter Out-File Encoding utf-8
Export-DefaultParameter
```

If you Export-DefaultParameter, your _whole_ `$PSDefaultParameterValues` hashtable is exported, and by default it goes in your profile folder. Whenever the DefaultParameter module is imported, the file in that default location file is imported, but you can manually specify the path if you like.

## Disable-DefaultParameter

The `Disable-DefaultParameter` command actually disables all the default parameter values, and this setting is part of the import/export...
