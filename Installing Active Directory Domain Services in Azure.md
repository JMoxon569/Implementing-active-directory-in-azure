**Installing Active Directory Domain Services in Azure**

**Introduction**

This section will guide you through the installation of Active Directory Domain Services (AD DS) on your Azure-hosted virtual machine. You'll convert one of your virtual machines into a domain controller, a critical component in managing network resources and services.

**Step 1: Prepare the Virtual Machine**

- **Access the VM:** Connect to your virtual machine using Remote Desktop Protocol (RDP). Use the credentials defined during the VM setup process.
- **Check System Requirements:** Ensure the VM meets the necessary requirements for installing AD DS. This typically involves having adequate system resources (CPU, Memory, and Disk Space) and network settings.

**Step 2: Install Active Directory Domain Services Role**

- **Open Server Manager:** Once logged in, open the Server Manager dashboard. This tool is essential for managing roles and features on your server.
- **Add Roles and Features:** Click on 'Add roles and features' to launch the wizard.
- **Role Selection:**
  - Choose 'Role-based or feature-based installation' and click 'Next'.
  - Select the current server from the server pool and click 'Next'.
  - From the list of available roles, check 'Active Directory Domain Services'. When prompted, also add the features that are required for Active Directory Domain Services.
- **Feature Installation:** Continue clicking 'Next' without adding additional features unless specifically required for your setup.
- **Confirmation and Installation:** Review your selections on the confirmation page, then click 'Install'. This process might take several minutes, depending on the VM's performance specs.

**Step 3: Promote the Server to a Domain Controller**

- **Promote the Server:** Once the AD DS role is installed, click on the notification flag in Server Manager, then click 'Promote this server to a domain controller'.
- **Deployment Configuration:**
  - Select 'Add a new forest' and enter the Root domain name (e.g., yourdomain.local).
- **Domain Controller Options:**
  - Set the Forest and Domain functional levels according to your environment needs (typically the highest level supported by all domain controllers in the network).
  - Specify the Directory Services Restore Mode (DSRM) password. This password is used when restoring the AD DS.
- **DNS Options:** If no DNS server is detected, the wizard will automatically select the option to install DNS server on this domain controller.
- **Additional Options:** Specify the location for the AD DS database, log files, and SYSVOL folder. The default locations are usually sufficient unless specific storage strategies are implemented.
- **Review Options:** Verify all your selections are correct.
- **Prerequisites Check:** Allow the wizard to check if the configuration meets all necessary prerequisites. If any issues are reported, address them before proceeding.
- **Install:** Click 'Install'. The server will automatically restart after the installation if necessary.

**Step 4: Verify the Installation**

- **Reconnect to the VM:** After the server restarts, reconnect using RDP.
- **Check Active Directory Tools:** Open Server Manager and ensure the 'AD DS' and 'DNS' roles are listed and running. You can further validate the installation by opening 'Active Directory Users and Computers' and 'DNS Manager' to see the new domain setup.

**Conclusion**

You have now successfully installed and configured Active Directory Domain Services on your Azure virtual machine, transforming it into a domain controller. This setup forms the backbone of your network's security and resource management in Azure.

