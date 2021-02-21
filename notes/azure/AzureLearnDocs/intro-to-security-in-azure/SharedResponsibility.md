# Microsoft Learn Notes: Intro to Security [Unit 2 Shared Responsibility](https://docs.microsoft.com/en-us/learn/modules/intro-to-security-in-azure/2-shared-responsibility)  

## Last Edited `01/24/2020`  

---  

## Notes' Author List  

1. [Trevor Henderson](https://github.com/trevor-henderson)  

---  

## Notable Definitions (Legend)  

| Key | Description | Link |  
|-------------|-------------|-------------|  
| `Tenant` | Entity utilizing the cloud services | N/A |
| `Service Provider` | Entity producing and maintaining cloud services | N/A |  
| `IaaS` | Infrastructure as a Service | [Microsoft Azure Definition](https://azure.microsoft.com/en-us/overview/what-is-iaas/) |
| `PaaS` | Platform as a Service | [Microsoft Azure Definition](https://azure.microsoft.com/en-us/overview/what-is-paas/) |
| `SaaS` | Software as a Service | [Microsoft Azure Definition](https://azure.microsoft.com/en-us/overview/what-is-saas/) |  
| `RBAC` | Role Based Access Control | [Microsoft Azure Definition](https://docs.microsoft.com/en-us/azure/role-based-access-control/overview)  
| `Resource` | Microsoft Azure Resource | [Azure Resource Groups Definition](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/overview#resource-groups)
| `DDoS` | Distributed Denial of Service | [Wikipedia Definition](https://en.wikipedia.org/wiki/Denial-of-service_attack)
---  

## Cloud Security

- As cloud tech becomes more prevalent the responsibility of security is shifted towards a shared responsibility between `tenant` and `Service Provider`  
  - In this shared responsibility, there are many "out-of-the-box" solutions that the `Service Provider` supports to mitigate risks and ensure proper security  
  - Cloud intelligence can improve detection and response time  
  - Cloud Security allows `Tenant`s to choose from a wide variety of Services to improve security  

---  

## Security Is a Shared Responsibility  

- At the `IaaS` level  
  - Still `Tenant`'s responsibility to patch and secure OS & software  
  - Still `Tenant`'s responsibility to configure the network  
  - `Tenant` gains the advantage of having outsourced concern over protecting the physical network  

- At the `PaaS` level  
  - Azure takes care of OS & most foundational software patches  
  - Services can be integrated with Azure Active Directory for access control  
  - No Need to create subnets or build entire infrastructure; Just point and click in the portal for pre-secured systems  
- At the `SaaS` Level  
  - Outsource most concerns  
- All could deplyment types  
  - `Tenant` retains responsibility for:  
    - Data  
    - Endpoints  
    - Accounts  
    - Access management  

---  

## A layered Security Approach  

- _Defense in depth_:  
  - Uses subsequent layers to prevent further exposure if the previous layer was breached  
  - Visualized as a set of concentric rings with the data at the center  
  - Each ring adds an additional layer of security  
  - ultimately, it is an attempt to prevent information being accessed or stolen by individuals that are not authorized to obtain it  
- _Desired Data for Bad Actors_:  
  - Data in the database  
  - Data on disk in a VM  
  - Data in cloud storage  
- Quote:  

``` text  
    It's the responsibility of those storing and controlling access to data to ensure that it's properly secured. Often, there are regulatory requirements that dictate the controls and processes that must be in place to ensure the confidentiality, integrity, and availability of the data.
```  

---
## Layers  

- Application:  
  - Ensure applications are secure and free of vulnerabilites  
  - Store sensitive application secrets in a secure storage meduium  
  - Make security a design requirement fo all app development  
- Quote:  

``` text  
Integrating security into the application development life cycle will help reduce the number of vulnerabilities introduced in code. We encourage all development teams to ensure their applications are secure by default, and that they're making security requirements non-negotiable.
```  

- Compute:  
  - Secure access to VMs  
  - Implement endpoint protection  
  - keep systems patched and up-to-date  
- Quote:  

``` text  
Malware, unpatched systems, and improperly secured systems open your environment to attacks. The focus in this layer is on making sure your compute resources are secure, and that you have the proper controls in place to minimize security issues.  

```  

- Networking:  
  - Limit communication between `resources`  
  - Deny by default  
  - Restrict inbound traffic and limit outbound  
  - Implement secure connectivity  

- Quote:  

``` text  
At this layer, the focus is on limiting the network connectivity across all your resources to allow only what is required. By limiting this communication, you reduce the risk of lateral movement throughout your network.
```  

- Perimeter:  
  - Use `DDoS` protection to filter large scale attacks before the can succeed  
  - Use firewalls to identify & alert on malicious events  
- Quote:  

``` text  
At the network perimeter, it's about protecting from network-based attacks against your resources. Identifying these attacks, eliminating their impact, and alerting you when they happen are important ways to keep your network secure.
```  

- Identity and Access:  
  - Control access to infrastructure and change control  
  - Use single sign-on & multi-factor authentication  
  - Audit events and changes  
- Quote:  

``` text
The identity and access layer is all about ensuring identities are secure, access granted is only what is needed, and changes are logged.
```  

- Physical Server:  
  - Where the hardware is stored and is Protected by the `Service Provider`  

- Quote:  

``` text
With physical security, the intent is to provide physical safeguards against access to assets. These safeguards ensure that other layers can't be bypassed, and loss or theft is handled appropriately.
```  

---  

## General Notes  

- The more control the `Tenant` desires the more responsibility the Tenant takes on  
- `RBAC` allows tenant to assign Role's to given Resources  
