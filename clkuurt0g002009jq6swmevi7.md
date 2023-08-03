---
title: "Upgrading vSphere: A comprehensive Guide from version 5.1 to 6.7 and later."
datePublished: Thu Aug 29 2019 07:45:42 GMT+0000 (Coordinated Universal Time)
cuid: clkuurt0g002009jq6swmevi7
slug: upgrading-vsphere-a-comprehensive-guide-from-version-51-to-67-and-later

---

**Introduction:**

### **What?**

In simple terms, Virtualization is a technology that transforms hardware into software.

Or Technically,

It is the technique of splitting Physical Resources into as many Logical Resources as we want. Eg. CPU Memory.

VMware vSphere is a powerful virtualization platform that enables businesses to consolidate their IT infrastructure, improve resource utilization, and enhance business continuity.

**Benefits of Virtualization**

* Optimized performance
    
* Increased IT productivity
    
* Scalability
    
* Added resilience for reduced downtime
    
* Effortless development and testing
    
* Work from anywhere capabilities
    
* Smaller environmental impact
    
* Simple security
    
* Lower operating costs
    

## **Hypervisor**

### What?

Hypervisor is a piece of software or firmware that creates and runs a Virtual Machine.

The primary function of a hypervisor is to manage and allocate the underlying hardware resources, such as CPU, memory, storage, and network, among the virtual machines. It abstracts these physical resources and presents them to each VM as if they have exclusive access to them, creating the illusion of multiple independent servers operating on a single physical machine.

There are two main types of hypervisors:

1. Type 1 Hypervisor (Bare-metal Hypervisor)
    
2. Type 2 Hypervisor (Hosted Hypervisor)
    

![4. Process and Practises](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ff0.holisticinfosecforwebdevelopers.com%2Fimages%2FHypervisorTypesHighLevel.png&f=1&nofb=1&ipt=fe94a22b7488381acff94197d90d5182294e0901c31e59037b47096a275b1d54&ipo=images align="left")

**Benefits of Hypervisor**

* Server Consolidation
    
* Isolation
    
* Hardware Independence
    
* Snapshot and Cloning
    
* Disaster Recovery and High Availability
    

1. Server Consolidation: By allowing multiple VMs to run on a single physical server, hypervisors enable better resource utilization and reduce hardware costs.
    
2. Isolation: Each virtual machine operates in its isolated environment, ensuring that processes and applications in one VM do not interfere with others. This isolation provides enhanced security and stability.
    
3. Hardware Independence: VMs are decoupled from the underlying hardware, making it easier to move virtual machines between different physical servers without compatibility issues.
    
4. Snapshot and Cloning: Hypervisors often offer features like snapshots and cloning, allowing administrators to capture the state of a VM at a specific point in time or duplicate VMs for testing and deployment purposes.
    
5. Disaster Recovery and High Availability: Hypervisors offer features such as live migration (e.g., vMotion) and replication (e.g., Site Recovery Manager) to ensure business continuity and minimize downtime in case of hardware failures or planned maintenance.
    

**Steps to Upgrade Hypervisor (VMWare vSphere) (Esxi) 5.1 to 6.7**

I. Upgrading from vSphere 5.1 to 5.5:

1. Pre-upgrade Assessment: Before initiating any upgrade process, it is crucial to perform a comprehensive assessment of the existing vSphere environment. This includes checking hardware compatibility, ensuring the compatibility of existing virtual machines with the new version, reviewing storage and networking requirements, and identifying any existing issues.
    
2. Backup and Snapshot: Creating backups and taking snapshots of the current vCenter Server and ESXi hosts is essential. In case of any unexpected issues during the upgrade, these backups will allow you to revert to the previous state safely.
    
3. vCenter Server Upgrade: The upgrade process typically starts with upgrading the vCenter Server. Ensure that you have the necessary upgrade files and follow the provided documentation carefully. During this step, ensure all dependencies like vSphere Web Client, Single Sign-On (SSO), and Inventory Service are also upgraded.
    
4. ESXi Host Upgrade: After upgrading the vCenter Server, proceed with upgrading each ESXi host. This can be done either through the vSphere Update Manager (VUM) or via the ESXi installer. The process involves rebooting each host after the upgrade, so ensure planned downtime for each host accordingly.
    
5. Compatibility and Testing: Post-upgrade, verify the compatibility of all existing virtual machines and ensure they function correctly. Perform thorough testing to confirm the functionality of various services and applications within the upgraded environment.
    

II. Upgrading from vSphere 5.5 to 6.7:

1. Similar Steps as vSphere 5.1 to 5.5 Upgrade: The upgrade process from vSphere 5.5 to 6.7 follows similar steps as the 5.1 to 5.5 upgrade. Begin with upgrading the vCenter Server to the 6.7 version, followed by the ESXi hosts.
    
2. Migration Tools: To ease the upgrade process, VMware offers various migration tools like the vSphere Client Integration Plugin and the vSphere HTML5 Client, making it easier to migrate from the older vSphere Web Client to the new HTML5-based client.
    
3. Compatibility Verification: As with any upgrade, ensure compatibility between the upgraded vCenter Server, ESXi hosts, and existing virtual machines. Testing and verification are crucial to ensure a smooth transition.
    

**(Other Hack) Simply upgrade the hypervisor 5.1 to 6.7**

1. Download ESXI 6.5 offline bundle from [Download VMware vSphere](https://my.vmware.com/web/vmware/details?downloadGroup=ESXI650&productId=614)
    
2. Shut down all VMs running on the ESXI host.
    
3. Cold Migrate all VMs from the Existing host to the backup host (or) another host on the same vCenter Server.
    
4. Now you can upgrade the hypervisor to any version using a flash drive by plugging in to physical server **(or)** uploading esxi offline zip bundle to datastore on ESXI host and upgrading