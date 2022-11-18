## Basics

> New-Item -Path 'X:\Guru99' -ItemType Directory <br>
> remove-item -path 'path'

> Write-Host "Hello, Guru99!"

> Set-executionpolicy unrestricted



## Data types:

![types](https://www.guru99.com/images/tensorflow/082918_1415_PowershellT8.jpg)


## Special Variables
- $Error 	An array of error objects which display the most recent errors
- $Host 	Display the name of the current hosting application
- $Profile 	Stores entire path of a user profile for the default shell
- $PID 	Stores the process identifier
- $PSUICulture 	It holds the name of the current UI culture.
- $NULL 	Contains empty or NULL value.
- $False 	Contains FALSE value
- $True 	Contains TRUE value

## PowerShell Concepts

- Cmdlets 	Cmdlet are build-command written in .net languages like VB or C#. It allows developers to extend the set of cmdlets by loading and write PowerShell snap-ins.
- Functions 	Functions are commands which is written in the PowerShell language. It can be developed without using other IDE like Visual Studio and devs.
- Scripts :	Scripts are text files on disk with a .ps1 extension
- Applications : 	Applications are existing windows programs.
- What if :	Tells the cmdlet not to execute, but to tell you what would happen if the cmdlet were to run.
- Confirm  :	Instruct the cmdlet to prompt before executing the command.
- Verbose :	Gives a higher level of detail.
- Debug :	Instructs the cmdlet to provide debugging information.
- ErrorAction :	Instructs the cmdlet to perform a specific action when an error occurs. Allowed actions continue, stop, silently- continue and inquire.
- ErrorVariable :	It specifies the variable which holds error information.
- OutVariable :	Tells the cmdlet to use a specific variable to hold the output information
- OutBuffer :	Instructs the cmdlet to hold the specific number of objects before calling the next cmdlet in the pipeline.
