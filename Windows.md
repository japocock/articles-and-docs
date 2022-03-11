# Windows OS
Useful links and documents

#### Windows OS Articles

[Pushing the Limits of Windows: Virtual Memory](https://blogs.technet.microsoft.com/markrussinovich/2008/11/17/pushing-the-limits-of-windows-virtual-memory/)

[Well-known security identifiers in Windows operating systems](https://support.microsoft.com/en-gb/help/243330/well-known-security-identifiers-in-windows-operating-systems)

[Troubleshoot port exhaustion issues](https://docs.microsoft.com/en-us/windows/client-management/troubleshoot-tcpip-port-exhaust)

```sh
netsh int ipv4 show dynamicport tcp
```

#### AD Computer Commands

Export Features and roles to XML

```sh
Reset-ComputerMachinePassword [-Credential <PSCredential>] [-Server <String>]
```

Allow alias for Windows Machine (2016 onwards)

```sh

///Registry Entries 
New-ItemProperty -Path HKLM:\SYSTEM\CurrentControlSet\Control\Lsa -Name DisableLoopbackCheck -PropertyType DWord -Value 1
New-ItemProperty -Path HKLM:\SYSTEM\CurrentControlSet\Control\Lsa\MSV1_0 -Name BackConnectionHostNames -PropertyType MultiString -Value $altNames
New-ItemProperty -Path HKLM:\SYSTEM\CurrentControlSet\Services\lanmanserver\parameters -Name OptionalNames -PropertyType MultiString -Value $altNames[0]
New-ItemProperty -Path HKLM:\SYSTEM\CurrentControlSet\Services\lanmanserver\parameters -Name DisableStrictNameChecking -PropertyType DWord -Value 1
New-ItemProperty -Path HKLM:\SYSTEM\CurrentControlSet\Services\lanmanserver\parameters -Name DnsOnWire -PropertyType DWord -Value 1

//AD
setspn -A host/alias COMPUTERNAME
```