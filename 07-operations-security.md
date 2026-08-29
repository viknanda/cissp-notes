# Operations Security

Rotation of duties definition – Interrupt opportunity to create collusion to subvert operation for fraudulent purposes.

Operational assurance concentrates on the architecture of the product, embedded features and functionality that enable a customer to continually obtain the necessary level of protection when using the product.

Lifecycle assurance pertains to how the product was developed and maintained. Eac hstage of the product's lifecycle has standards and expectations it must fulfill before it can be deemed a highly trustd product.

A clipping level refers to a baseline for violation activities that may be normal for a user to commit before alarms are raised.

Security controls and mechanims that are in place should have a degree of transparency. This enables the user to perform tasks and duties without having to go through extra steps because of the presence of the security controls. Transparency also does not let the user know too much about the controls, which helps prevent him from figuring out how to circumvent them.

Change control is the management of security features and a level of assurance provided through the control of the changes made to the system's hardware, software and firmware configurations through the development and operational lifecycle.

Change Control Policy features:

- Request for a change to take place

- Approval of the change

- Documentation of the change

- Tested and presented

- Implementation

- Report changes to management Backup tapes should be labelled with the following information:

- Date of creation

- Individual who created the backup

- Retention period

- Classification

- Volume name and version When media is cleared of its contents, it is said to be sanitized.

A device that performs degaussing generates a coercive magnetic force that reduces the magnetic flux density of the storage media to zero. This magnetic force is what properly erases data from media.

Data remanence is the residual physical representation of information that was saved and then erased in some fashion. This remanence may be enough to enable the data to be reconstructed and restored back into readable form.

An operating system's response to a type of failure can be classified as one of the following:

- System reboot – takes place after shutting down the system in a controlled manner in response to a TCB failure. If the system finds inconsistent object data structures or if there is not enough space in some critical tables, a system reboot may take place. This releases resources and returns the systems to a more stable and safe state.

- Emergency system restart – takes place after a system failure happens in an uncontrolled manner. This can be a TCB or media failure that could be caused by lower-privileged userprocesses attempting to access memory segments that are restricted. The system goes into a maintenance mode and recovers from the actions taken. The system is brought back up in a consistent and stable state.

- System cold start – takes place when an unexpected TCB or media failure happens and the regular recovery procedure cannot recover the system to a more consistent state. The system, TCB and user objects may remain in an inconsistent state while the system attempts to recover itself and intervention may be required by the user or administrator to restore the system.

It is important that the system does not enter an insecure state when it is affected by any of these types of problems and that it shuts down and recovers properly to a secure and stable state.

Simple Mail Transfer Protocol (SMTP) works as a message transfer agent.

Post Office Protocol (POP) is an Internet mail server protocol that supports incoming and outgoing messages. The mail server using POP stores and forwards email messages and works with SMTP to move messages between mail servers. This system is useful because the messages will be held on the mail server until users are ready to download their messages.

Internet Messaga Access Protocol (IMAP) is also an Internet protocol that enables users to access mail on a mail server. IMAP as more capabilities and functionality than POP. IMAP is a store-and -forward mail server protocol that is considered POP's successor. IMAP also gives administrators more capabilities when it comes to administering and maintaining the user's messages.

Mail servers use a relay agent to send a message from one mail server to another. This needs to be properly configured so that a company's mail server is not used by another for spamming activity.

A fax encryptor, a bulk data link encryption mechanism, encrypts any and all fax data that hits the network cable or telephone wire.

Operating system fingerprinting refers to interpreting two slightly different responses from hosts in order to determine the type of operating system that an attacker is communicating with.

Port scanning identifies open ports on a computer.

TCP wrappers monitor incoming network traffic and control what can and cannot access the services mapped to specific ports.

Countermeasures to Port Scanning and Network Mapping:

- Disable unnecessary ports and services

- Block access at the perimeter network using firewalls, routers and proxy servers

- Use an IDS to identify this type of activity

- Use TCP Wrappers on vulnerable services that have to be available

- Remove as many banners as possible within operating systems and applications

- Upgrade or update to more secure operating systems, applications and protocols A superzapping program is a utility used in IBM mainframe centers that has the capability to bypass access controls within the mainframe's operating system.

The only way to detect improper use of a superzapping utility is by comparing the sizes of the files to the original or parent files.

Today, a superzapper refers to any tool that can make modifications that are not auditable or logged.

A network sniffer is a tool that monitors traffic as it passes by. These tools work with network interface cards in promiscuous mode i.e. They see all traffic that is going past them on the network wire.

Switched environments are less prone to exploits based on network sniffers because they separate network segments by broadcast and collision domains.

Secure RPC (S-RPC) uses Diffie-Hellman public key cryptography to determine the shared secret key for encryption with the DES algorithm.

If session hijacking is a concern on a network, the administrator can implement a protocol that requires mutual authentication between users or systems like IPSec or Kerberos.

A dictionary attack is when a large list of words is fed into a password hacking tool. This tool runs a one-way hash on the captured password and on each word in the list. The tool compares the hashing results to see if they match.

In a brute force attack, a tool will try many different variations of characters, run a hash value on each variation and compare it to the hash value of the captured password.

WinNuk – type of DoS attack that sends out-of-band packets to port 139.

Slamming – when a user's telephone service provider has been changed without the user's consent.

Cramming – adding on charges that are bogus in nature that the user did not request.

Penetration testing is a set of procedures designed to test and possibly bypass security controls of a system.

Its goal is to measure an organization's resistance to an attack and to uncover any weaknesses within the environment.

Initial Program Load (IPL) is a mainfram term for loading the operating system's kernel into the computer's main memory.
