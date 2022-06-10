# This is the second phase of the Active Directory Lab

# INSTALL DOMAIN CONTROLLER

1. Rename Windows Server 2022

2. Add static IP and DNS addresses

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