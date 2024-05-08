# Active Directory On-Premises in Azure

## Introduction

This tutorial provides a comprehensive guide on setting up an on-premises Active Directory environment using Microsoft Azure. This project is designed to help users simulate a realistic Active Directory setup in a cloud environment, demonstrating the setup of multiple virtual machines, connectivity configurations, AD Domain Services installation, and automation with PowerShell scripts.

## Requirements

- **Microsoft Azure Subscription**: You will need an active subscription to Microsoft Azure. If you don't have one, you can sign up for a free trial.
- **Knowledge of Azure Virtual Machines and Networking**: Basic understanding of how to create and manage virtual machines and virtual networks in Azure.
- **Active Directory Knowledge**: Familiarity with Active Directory concepts and management tasks.
- **PowerShell Proficiency**: Ability to write and understand PowerShell scripts, as this will be necessary for automating tasks in Active Directory.

## Tutorial Sections

1. **Setting Up Virtual Machines**
   - This section covers the creation of virtual machines within Azure. It guides you through setting up the required virtual network and VMs that will host the Active Directory.
   - [Setup Virtual Machines](1_Setup_Virtual_Machines.md)

2. **Installing Active Directory Domain Services**
   - Here, you will learn how to install and configure Active Directory Domain Services on your virtual machines. This includes promoting one of your VMs to a domain controller.
   - [Install AD Domain Services](2_Install_AD_Domain_Services.md)

3. **Automating User Creation with PowerShell**
   - This part of the tutorial will show you how to write and execute a PowerShell script to automate the creation of thousands of users in your Active Directory.
   - [Automate User Creation](3_Automate_User_Creation.md)

## Additional Resources

- [Microsoft Azure Documentation](https://docs.microsoft.com/en-us/azure/)
- [Active Directory Documentation](https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/)
- [Learn PowerShell](https://docs.microsoft.com/en-us/powershell/)
