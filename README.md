# az104-10-vm0
Creating a Virtual Machine (VM) in Azure can be useful for a variety of scenarios including development, testing, hosting applications, and running workloads in the cloud.

Welcome to Azure Site Recovery
You can replicate your virtual machines to another Azure region for business continuity and disaster recovery needs.

Enable virtual machine replication
In the Azure portal, search for and select Recovery Services vaults and, on the Recovery Services vaults blade, click + Create
On the Create Recovery Services vault blade, specify the following settings:
Settings
Value
Subscription
the name of your Azure subscription
Resource group
az104-rg-region2 (If necessary, select Create new)
Vault Name
az104-rsv-region2
Region
West US

Note: Make sure that you specify a different region than the virtual machine.
Click Review + Create, ensure that the validation passes and then click Create.
Note: Wait for the deployment to complete. The deployment should take a couple of minutes.
Search for and select the az104-10-vm0 virtual machine.
In the Backup + Disaster recovery blade, select Disaster recovery.
Select Enable replication.
On the Basics tab, notice the Target region.
Move to the Advanced settings tab. Resource selections have been made for you. It is important to review them.
Verify your subscription, vm resource group, virtual network, and availability (take the default) settings.
In Storage settings select Show details.
Setting
Value
Churn for the vm
Normal churn
Cache storage account
(new) xxx

Note: It is important that both of these settings be populated, or the validation will fail. If values are not present, try refreshing the page. If that doesn’t work, create an empty storage account and then return to this page.
In Replication settings select Show details. Notice your recovery resources vault in region 2 was automatically selected.
Select Review + Start replication and then Enable replication
Note: Enabling replication will take a 10-15 minutes. Watch the notification messages in the upper right of the portal. While you wait, consider reviewing the self-paced training links at the end of this page.
Once the replication is complete, search for and locate your Recovery Services Vault, az104-rsv-region2. You may need to Refresh the page.
In the Protected items section, select Replicated items.
Check that the virtual machine is showing as healthy for the replication health. Note that the status will show the synchronization (starting at 0%) status and ultimately show Protected after the initial synchronization completes.

Select the virtual machine to view more details.
Did you know? It is a good practice to test the failover of a protected VM.
