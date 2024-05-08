**Setting Up Virtual Machines in Azure**

**Introduction**

This section of the tutorial covers the creation and configuration of virtual machines (VMs) within Microsoft Azure. You will learn how to set up the required virtual network and VMs that will host the Active Directory Domain Services.

**Step 1: Create a Virtual Network**

- **Log into Azure Portal:** Begin by signing into your Azure Portal at [https://portal.azure.com](https://portal.azure.com/).
- **Navigate to Virtual Networks:** Go to the 'Virtual networks' section from the sidebar or use the search bar to find it.
- **Create Virtual Network:** Click on 'Create' and then 'Virtual network'. Fill in the necessary details:
  - **Name:** Provide a descriptive name for your virtual network.
  - **Region:** Select the region that matches your compliance and latency requirements.
  - **Address space:** Define the IP address range in CIDR notation. Ensure that it is large enough to accommodate all VMs and services you plan to deploy.
- **Subnet Creation:** Within the virtual network, create a subnet that will be used by your VMs.
- **Review and Create:** After reviewing your settings, click 'Create' to deploy the virtual network.

**Step 2: Create Virtual Machines**

- **Open Virtual Machine Creation:** From the Azure home dashboard, click on 'Create a resource', then choose 'Virtual machines'.
- **Basic Configuration:**
  - **Subscription and Resource Group:** Select your Azure subscription and either choose an existing resource group or create a new one.
  - **Virtual Machine Name:** Give your VM a name that helps you identify its role (e.g., AD-Domain-Controller).
  - **Region:** Choose the same region as your virtual network.
  - **Availability Options:** Configure availability options if necessary, to ensure higher availability.
- **Administrator Account Setup:**
  - **Authentication type:** Choose whether to use SSH keys or a username and password. For Windows VMs, you will generally use a username and password.
  - **Username and Password:** Enter a username and a strong password that will be used to access the VM.
- **Operating System:**
  - **Image:** Select an appropriate OS image, such as Windows Server 2019.
- **Size:** Choose a size for your VM. Ensure it meets the minimum requirements for running Active Directory.
- **Networking Settings:**
  - **Virtual Network and Subnet:** Ensure the VM is connected to the previously created virtual network and subnet.
  - **Public IP:** Assign a public IP if remote access is required from outside the network.
- **Management Tools:**
  - **Monitoring and Diagnostics:** Configure monitoring and diagnostics settings according to your needs.
- **Review and Create:** Review all settings, then click 'Create' to start the deployment of your VM.

**Step 3: Verify VM Connectivity**

- **Check VM Status:** Once your VMs are deployed, go to the 'Virtual machines' section to check their status. Ensure they are running and have no issues.
- **Connect to VM:** Test the connectivity by remotely connecting to your VM:
  - For Windows VMs, use Remote Desktop Protocol (RDP) to connect using the public IP address and the credentials you set up.
- **Verify Network Connectivity:** Ensure that the VMs can communicate with each other over the virtual network. This is crucial for setting up Active Directory services in the next steps.

**Conclusion**

You have now successfully set up and configured the necessary virtual machines in Microsoft Azure. These VMs are connected and ready for the installation of Active Directory Domain Services, which will be covered in the following sections of this tutorial.

