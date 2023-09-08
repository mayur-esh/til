# til
Today I learned

### PowerShell.exe enables SeDebugPrivilege by default, while CMD.exe does not.
This is enabled by .NET when PowerShell uses the System.Diagnostics.Process class in .NET. One example is the Get-Process cmdlet. Another example is the method it invokes to get the current process PID for the $pid variable. Any .NET application that uses the System.Diagnostics.Process class also enables this privilege. 

Sources:
https://www.leeholmes.com/why-is-sedebugprivilege-enabled-in-powershell/
https://github.com/dotnet/corefx/blob/master/src/System.Diagnostics.Process/src/System/Diagnostics/ProcessManager.Windows.cs#L129

### PowerShell snippet for RTLO 
``Rename-Item -Path GetSymbol.exe -NewName ("DSC-Image" + ( [char]0x202E) + "gepj.exe")``
