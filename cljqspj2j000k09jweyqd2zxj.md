---
title: "Azure Administration"
seoTitle: "Mastering Azure AZ-104: A Comprehensive Guide to Azure Administrator"
seoDescription: "Unlock the power of Microsoft Azure with our in-depth guide on Azure AZ-104 certification. Learn the essential skills and knowledge needed to become a profi"
datePublished: Mon Jan 09 2023 06:56:01 GMT+0000 (Coordinated Universal Time)
cuid: cljqspj2j000k09jweyqd2zxj
slug: azure-administration
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1688585717767/9de2dfc5-b977-4676-bbee-5595dd166cb5.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1688626449758/6386dfd5-07a0-47e3-b2e5-cd1c3036ceba.png
tags: microsoft-azure-certification, azureprojects, azure-day-to-day

---

1. ### **What is Microsoft Azure?**
    

[Azure is a cloud computing platform](https://www.simplilearn.com/azure-cloud-services-and-its-importance-article?source=frs_author_page) and an online portal that allows you to access and manage cloud services and resources provided by Microsoft.

### **1.1 What are the Various Azure Services and How Does Azure Work?**

Azure provides more than 200 services, which are divided into 18 categories. These categories include computing, networking, storage, [IoT](https://www.simplilearn.com/what-is-iot-how-and-why-it-matters-article), migration, mobile, analytics, containers, [artificial intelligence](https://www.simplilearn.com/tutorials/artificial-intelligence-tutorial/what-is-artificial-intelligence), and other machine learning, integration, management tools, developer tools, security, databases, [DevOps,](https://www.simplilearn.com/tutorials/devops-tutorial/what-is-devops) media identity, and web services.

### **1.2 Compute Services**

* #### **Virtual Machine**
    
    This service enables you to create a virtual machine in Windows, Linux or any other configuration in seconds.
    
* #### **Cloud Service**
    
    This service lets you create scalable applications within the cloud. Once the application is deployed, everything, including provisioning, load balancing, and health monitoring, is taken care of by Azure.
    
* #### **Service Fabric**
    
    With service fabric, the process of developing a microservice is immensely simplified. Microservice is an application that contains other bundled smaller applications.
    
* #### **Functions**
    
    With functions, you can create applications in any programming language. The best part about this service is that you need not worry about hardware requirements while developing applications because Azure takes care of that. All you need to do is provide the code.
    
* ### **1.3 Networking**
    
    * #### **Azure CDN**
        
        Azure CDN (Content Delivery Network) is for delivering content to users. It uses a high bandwidth, and content can be transferred to any person around the globe. The [CDN service](https://www.simplilearn.com/content-delivery-network-article) uses a network of servers placed strategically around the globe so that the users can access the data as soon as possible.
        
    * #### **Express Route**
        
        This service lets you connect your on-premise network to the Microsoft cloud or any other services that you want, through a private connection. So, the only communications that will happen here will be between the enterprise network and the service that you want.
        
    * #### **Virtual network**
        
        The [virtual network](https://www.simplilearn.com/tutorials/azure-tutorial/azure-virtual-network-vnet) allows you to have any of the Azure services communicate with one another privately and securely.
        
    * #### **Azure DNS**
        
        This service allows you to host your DNS domains or system domains on Azure.
        
    
    ### **1.4 Storage**
    
    * #### **Disk Storage**
        
        This service allows you to choose from either HDD (Hard Disk Drive) or SSD (Solid State Drive) as your storage option along with your virtual machine.
        
    * #### **Blob Storage**
        
        This service is optimized to store a massive amount of unstructured data, including text and even binary data.
        
    * #### **File Storage**
        
        This is a managed file storage service that can be accessed via industry SMB (server message block) protocol.
        
    * #### **Queue Storage**
        
        With queue storage, you can provide stable message queuing for a large workload. This service can be accessed from anywhere in the world.
        
    
    ### **1.5 Azure Key Concepts**
    
    <table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Concept Name</strong></p></td><td colspan="1" rowspan="1"><p><strong>Description</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Regions</strong></p></td><td colspan="1" rowspan="1"><p><br>Azure is a global cloud platform that is available across various regions around the world. When you request a service, application, or VM in Azure, you are first asked to specify a region. The selected region represents the data centre where your application runs.</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Datacenter</strong></p></td><td colspan="1" rowspan="1"><p><br>In Azure, you can deploy your applications into a variety of data centers around the globe. So, it is advisable to select a region which is closer to most of your customers. It helps you to reduce latency in network requests.</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Azure Portal</strong></p></td><td colspan="1" rowspan="1"><p>The Azure portal is a web-based application that can be used to create, manage and remove Azure resources and services. It is located at <a target="_blank" rel="noopener noreferrer nofollow" href="https://portal.azure.com" style="pointer-events: none"><strong>https://portal.azure.com</strong></a>.</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Resource</strong></p></td><td colspan="1" rowspan="1"><p>Resource in Azure is a virtual machine, role, or instance type that can be used for computing, storage, or networking.</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Resource group</strong></p></td><td colspan="1" rowspan="1"><p>A resource group is a container that holds related resources for an Azure solution. The resource group can include all the resources for the solution or only those resources that you want to manage as a group.</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Resource Manager templates</strong></p></td><td colspan="1" rowspan="1"><p>It is a JSON that defines one or more resources to deploy to a resource group. It also establishes dependencies between deployed resources.</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>&nbsp;Automation</strong></p></td><td colspan="1" rowspan="1"><p>Azure allows you to automate the process of creating, managing and deleting resources by using PowerShell or the Azure command-line Interface(CLI).</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Azure PowerShell</strong></p></td><td colspan="1" rowspan="1"><p>PowerShell is a set of modules that offer cmdlets to manage Azure. In most cases, you are allowed to use, the cmdlets command for the same tasks which you are performing in the Azure portal.</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Azure command-line interface(CLI)</strong></p></td><td colspan="1" rowspan="1"><p>The Azure CLI is a tool that you can use to create, manage, and remove Azure resources from the command line.</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>REST APIs</strong></p></td><td colspan="1" rowspan="1"><p>Azure is built on a set of REST APIs that help you perform the same operation that you do in Azure portal Ul. It allows your Azure resources and apps to be manipulated via any third-party software application.</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>&nbsp;</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr></tbody></table>
    
    **Interacting with Azure**
    
    There are 3 ways you can interact with Azure: the Portal, the Azure CLI, and the Azure PowerShell module. A good engineer or architect should be proficient in at least two of these tools, so they can optimize their workflow for any situation.
    
* 1. **Azure Portal**
        
* This is the graphical user interface (GUI) for Azure
    
* You access the portal from [**portal.azure.com**](http://portal.azure.com)
    
* The portal is great for learning about Azure or doing one-time tasks
    
    * Compared to other options, clicking around in the Azure portal can be a little slow
        
    * The portal is also great for visualizing your environment
        
    * Very useful for most day-to-day work
        
* Automation is not supported with the Portal
    
* 2\. **Azure Cloud Shell / Azure CLI**
    
    * The Azure CLI is a command-line program that allows you to do pretty much everything that can be done in the Portal, but through the use of Azure commands
        
    * This can be much quicker than the portal since you do not have to wait for pages to load and click around
        
    * This is also great for users who want to create Bash scripts and put the Azure CLI commands into the script, which is how many tasks are automated
        
    * Azure Cloud Shell is the implementation of Azure CLI that runs in the Azure portal, so you can run Azure CLI commands from a browser-based command line
        
        1. **Azure PowerShell Module**
            
            . It has the same advantages as the Azure CLI, but instead of CLI commands, you will be using PowerShell cmdlets.
            
            . The Azure PowerShell module still is great for repetitive tasks, is generally quicker than the Portal, and can be put into a script (a PowerShell script, of course)
            
    
    ---
    

1. ## Managing MS Azure
    

### Creating Azure Account

Step 1: Visit the Azure Sign-up Page ([**https://azure.microsoft.com/en-us/free/**](https://azure.microsoft.com/en-us/free/)). Step 2: Provide Your Basic Information includes your email address, password, and country/region.

Step 3: Verify Your Identity To ensure the security of your Azure account

Step 4: Set Up Billing Azure provides a range of services, both free and paid, depending on your requirements. To set up billing for your Azure account, you'll need to provide a valid credit card or bank account information. However, Azure also offers a free trial with a generous credit amount to help you explore the platform without incurring charges.

Step 5: Complete the Sign-up Process Once you've provided the necessary information and set up billing, review the terms and conditions, and privacy policy. If you agree to these terms, click on the "Create" or "Sign up" button to finalize the creation of your Azure account.

Step 6: Accessing the Azure Portal Congratulations! You've successfully created your Azure account. You can now access the Azure portal ([**https://portal.azure.com/**](https://portal.azure.com/)) The Azure portal serves as a central hub for managing your Azure resources, deploying virtual machines, configuring services, and much more.

### Types of Administrators:

1. Azure Active Directory (Azure AD) Administrator: This administrator manages user accounts, access policies, and security settings in Azure AD. They can create and manage users, groups, roles, and applications, and control access to Azure resources.
    
2. Subscription Administrator: This administrator has full access to all resources and management operations within an Azure subscription. They can manage resources, assign roles, and perform billing-related tasks.
    
3. Resource Group Administrator: This administrator has permissions to manage and control all resources within a specific resource group. They can create, delete, and modify resources within that resource group.
    
4. Virtual Machine Administrator: This administrator has permissions to manage virtual machines (VMs) in Azure. They can create, configure, start, stop, and delete VMs, as well as manage associated resources like disks, networking, and storage.
    
5. Network Administrator: This administrator is responsible for managing and configuring networking resources in Azure. They can create and manage virtual networks (VNets), subnets, network security groups (NSGs), and other network-related components.
    
6. Storage Administrator: This administrator is responsible for managing and configuring Azure storage accounts and associated services. They can create and manage storage containers, blobs, queues, file shares, and set access permissions.
    
7. Security Administrator: This administrator focuses on securing Azure resources and managing security-related settings. They can configure and manage Azure Security Center, implement security policies, manage encryption keys, and monitor security events.
    
8. Database Administrator: This administrator specializes in managing and administering Azure databases, such as Azure SQL Database, Azure Cosmos DB, or Azure Database for MySQL/PostgreSQL. They can perform tasks like database creation, backup and restore, scaling, and performance optimization.
    
9. App Service Administrator: This administrator manages Azure App Service, a platform for hosting web applications, mobile app backends, and RESTful APIs. They can create, manage, and configure App Service plans, web apps, deployment slots, and associated services like Azure Functions.