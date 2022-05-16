Prerequisites
===================================

Working with clinical data in a hospital requires a broad understanding of the basic IT concepts. The regulatory aspects (human research act, federal act on data protection, e.g.), the conformance to IT security standards and the efficient handling of various data/file types all depend on the understanding of these basic concepts.

Basic IT Concepts
------------------------

**Server**

A server is a piece of hardware with an own operating system that can be used for various purposes. The server can be physicial or virtual (also "Virtual Machine").

A server can be more powerful and reliable than standard personal computers, and especially in high performance compute (HPC) environment can be clustered to scale-up the compute power.

Typical servers are database servers, file servers, mail servers, print servers, web servers and application servers.

**Network**

A network consists of two or more computers that are linked in order to share resources, exchange files, or allow electronic communications. Typically a network is structured into different zones with different security measures. Obviously communicating from one network zone to another zone requires additional security measures to avoid unwanted/malicious incoming traffic in a network zone.

* **Internet Zone**
    * This zone is normally insecure and not trusted.
* **Demilitarized Zone** 
    * Publicly accessible servers are placed in this zone. Servers placed in this zone are called bastion hosts.
* **Intranet Zone** 
    * This zone consists of internal networks.
* **Internal Highly-Secure Zone** 
    * Business critical information and services are placed in this zone. The acess is restricted to allow only administrators. 

**Firewall**

A firewall is a network security device that monitors incoming and outgoing network traffic and decides whether to allow or block specific traffic based on a defined set of security rules.
Firewalls establish a barrier between secured and controlled internal networks that can be trusted and untrusted outside networks, such as the Internet. 
A firewall can be hardware, software, or both.

**Proxy**

A proxy server acts as a gateway between the user and the internet. It separates end users from the websites they browse. Proxy servers provide varying levels of functionality, security, and privacy depending on the use case, needs, or company policy.

When a proxy server is configured, internet traffic flows through the proxy server on its way to the address the user requested. The request then comes back through that same proxy server and the proxy server forwards the data received from the website to the user.

**Storage System**

Storage is a mechanism that enables a computer to retain data, either temporarily or permanently. 

There are two major types:

* **Volatile Storage (Memory)**
    * Requires a continuous supply of electricity to store/retain data. It acts as a computer's primary storage for temporarily storing data and handling application workloads. A good example is the random access memory (RAM). Obviously if the supply of electricity stops, the data is gone.
  
* **Non-Volatile Storage** 
    * A type of storage mechanism that retains digital data even if the supply of electricity stops. This is often referred to as a secondary storage mechanism, and is used for permanent data storage requiring I/O (input/output) operations. Examples of volatile storage include a hard disk, USB storage and optical media (CD/DVD/etc.).

Glossary
------------

