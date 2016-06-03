# Add-AzureRmVm.ps1

This is a PowerShell script to add an Azure Resource Manager Virtual Machine to an existing environment. You can use the script to add a IaaSv2 virtual machine to an existing resource group, virtual network, and storage account. Simply provide the name of the resource group and storage account as parameters and your new VM will get added to the existing environment.

Here's an example of how you might run the script. This assumes that you've already authenticated to the AzureRM PowerShell module and have selected your subscription.

```
$params = @{
    VMName = 'Web2'
    ResourceGroupName = 'WebServers'
    StorageAccountName = 'webservers6722'
    Credential = (Get-Credential)
}

.\Add-AzureRmVm.ps1 @params

```

The script also creates a public IP address and attaches it to the servers network interface.
