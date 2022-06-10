# This is the second phase of the Active Directory Lab

# INSTALL DOMAIN CONTROLLER

1. Rename Windows Server 2022

Use SConfig.exe

OR

Use:
```
Rename-Computer -NewName "XYZ-DC1" -Restart
```

2. Add static IP and DNS addresses

Use SConfig.exe

OR

Use:
```
Set-NetIPAddress -InterfaceIndex 1 -IPAddress 192.168.147.155 -PrefixLength 24
```

```
Set-DnsClientServerAddress -InterfaceIndex 1 -ServerAddresses ("192.168.147.155")
```

3. Install AD Domain Services

```
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
```

4. Install AD Forest

```
Import-Module ADDSDeployment
```

```
Install-ADDSForest
```