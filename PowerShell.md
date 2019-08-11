# PowerShell
Useful links and documents

#### PowerShell Search
```sh
Get-ChildItem -recurse | Select-String -pattern "foo" | where-object {$_.path -like '*.txt*'} | group path | select name
```

#### PowerShell Articles

[Understanding the Six PowerShell Profiles](https://devblogs.microsoft.com/scripting/understanding-the-six-powershell-profiles/)

[Richard Siddaway's Blog](https://richardspowershellblog.wordpress.com/)

#### AWS PowerShell Commands

Get S3 objects from a given bucket with a given storage class.

```sh
Get-S3Object -BucketName <bucketname> -ProfileName <ProfileName> -Region <Region>  | Where-Object {$_.StorageClass -eq "GLACIER"}
```

#### PowerShell Converters

[Registry to PowerShell converter](https://reg2ps.azurewebsites.net/)

#### AD PowerShell Commands

[Test-ComputerSecureChannel -Repair -Verbose](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/test-computersecurechannel?view=powershell-5.1)

```sh
$objSID = New-Object System.Security.Principal.SecurityIdentifier ("xxxxxxxxx")
$objUser = $objSID.Translate( [System.Security.Principal.NTAccount])
$objUser.Value 
```

#### Windows Feature PowerShell Commands

Install .NET

```sh
Install-WindowsFeature Net-Framework-Core -source "C:\SomeSource"
```

Export Features and roles to XML

```sh
Get-WindowsFeature | Where-Object {$_.name -Like "*Web*"} | Where Installed | Export-Clixml C:\TEMP\InstalledRoles.xml
```
