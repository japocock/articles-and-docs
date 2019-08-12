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

```sh
#Test/repair a computers secure channel with AD
Test-ComputerSecureChannel -Repair -Verbose
```

```sh
#SID > GroupName
$objSID = New-Object System.Security.Principal.SecurityIdentifier ("xxxxxxxxx")
$objUser = $objSID.Translate( [System.Security.Principal.NTAccount])
$objUser.Value 
```
```sh
#Get Members of AD Groups (possible filter examples)

get-adgroup -Properties *  -Filter "name -like 'Acme*' -and GroupCategory -eq 'Security' -and Managedby -eq 'CN=Simpson\, HOMER,OU=SPRINGFIELD,DC=EARTH,DC=net'" -SearchBase "DC=EARTH,DC=net" -PipelineVariable group  | 
Get-AdgroupMember -PipelineVariable member | ForEach-Object {
    New-Object psobject -Property @{
        Group = $group.Name
        "Group DN" = $group.Distinguishedname
        "Group SamAccountName" = $group.SamAccountName
        "Member DN" = $member.DistinguishedName
        "Member Name" = $member.Name
        "Member SamAccountName" = $member.SamAccountName
    }
} | Export-CSV C:\TEMP\Acme_Groups_Groups_Managed_By_Homer_Simpson.csv -Append -NoTypeInformation -ErrorAction Inquire
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
