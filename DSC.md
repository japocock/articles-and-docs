# DSC

Useful links and documents

#### DSC

[Idempotency For Dummies](https://medium.com/@ahmadfarag/idempotency-764f7bb6e4e2)

[Credentials Options in Configuration Data](https://docs.microsoft.com/en-us/powershell/dsc/configurations/configdatacredentials)

Get resource syntax

```sh
Get-DscResource -Name <resourcename> -Syntax

PS C:\Users\administrator.BlueBuffalo> Get-DscResource | Select Name

<resourcename>                   
----                     
File                     
Archive                  
Environment              
Group                    
GroupSet                 
Log                      
Package                  
ProcessSet               
Registry                 
Script                   
Service                  
ServiceSet               
User                     
WaitForAll               
WaitForAny               
WaitForSome              
WindowsFeature           
WindowsFeatureSet        
WindowsOptionalFeature   
WindowsOptionalFeatureSet
WindowsProcess           
```
