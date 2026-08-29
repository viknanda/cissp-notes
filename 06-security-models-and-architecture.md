# Security Models and Architecture

A security model is a statement that outlines the requirements necessary to properly support and implement a certain security policy.

Computer architecture encompasses all the parts of a computer system necessary for it to function, including the operating system, memory chips, circuits, hard drive, security components, buses and networking components.

The central processing unit (CPU) is a microprocessor that contains a control unit, an arithmetic logic unit (ALU) and registers, which are holding places for data and instructions.

The control unit manages and synchronizes the system while different applications' code and operating system instructions are being executed. It determines what application instructions get processed and in what priority and time slice.

The ALU can be thought of as the brain of the CPU and the CPU as the brain of the computer.

Buffer overflows: if the software instructions do not properly set the boundaries for how much data can come in as a block, extra data can slip in and be executed.

Random access memory (RAM) is a type of memory storage facility where data can be held and altered. It is used for read/write activities by the operating system and appications. It is described as volatile because if the computer's power supply is terminated, then all information within this type of memory is lost.

Static RAM is so-called because when it stores data, it stayes there without the need of being continually refreshed.

Dynamic RAM requires that the data held within it be periodically refreshed because the data can dissipate and decay.

Read-only memory (ROM) is a nonvolatile storage facilitiy, meaning that when a computer's power is turned off, the data is still held within the memory chips. The software that is stored within ROM is called firmware.

Erasable and programmable read-only memory (EPROM) can be modified, deleted or upgraded. EPROM holds data that can be electrically erased or written to.

Cache memory is a type of memory that is used for high-speed writing and reading activities. It holds instructions and data from primary storage and is accessed when application instructions and data are being executed.

Data being received from cache can be accessed much more quickly than if it was stored in real memory.

The CPU is one of the most trusted components within a system and therefore it can access memory directly. It uses physical addresses instead of pointers to memory segments.

Software does not use physical addresses; instead, it uses virtual or logical memory. Accessing memory indirectly provides an access control layer between the software and the memory, which is done for protection and efficiency.

Mammped memory enables different programs to access the data and perform their own separate functions on it in a more economical and resourceful manner.

Secondary storage is considered to be nonvolatile storage media, which can be the computer's hard drive, floppy disks or CD-ROM.

When RAM and secondary storage are combined, the result is virtual storage. The system uses hard drive space to extend RAM memory space capability. The hard drive space that is used to extend the RAM memory capabilities is incremented in pages.

Paging refers to the process when data is brought from the hard drive pages back into memory.

Protection rings provide strict boundaries and definitions for what the processes that work within the each ring can access and what operations they can successfully execute.

The processes that operate within the inner rings have more privileges than the processes operating in the outer rings.

Processes that execute within the inner rings are usually referred to as existing in a privileged or supervisor mode. The processes working in the outer rings are said to execute in a user mode.

The actual ring architecture that is being used by a system is dictated by the processor and the operating system. The hardware chip is constructed to work with a certain number of rings and the operating system must be developed to also work in this ring structure.

Ring 0 – operating system kernel Ring 1 – remaining parts of the operating system Ring 2 – I/O drivers and utilities Ring 3 – applications and programs These protection rings provide an intermediate layer between subjects and objects and are used for access control when a subject tries to access an object. The lower the ring number, the greater the amoung of privilege that is given to the process that runs within that ring. Entities can only access objects within their own ring and outer rings.

When an application needs access to components in rings that it is not allowed to directly access, it makes a request of the operating system toperform the necessary tasks.

A process is a program in execution that works in its own address space and can only communicate with other processes in a controlled manner.

A thread represents a piece of code that is executed within a process.

Operating system modes: privileged or user Process operating states:

- Stopped – the process is not running

- Waiting – the process is waiting for an interrupt to be able to interact with the CPU

- Running – the process and its instructions are being executed by the CPU

- Ready – the process is available to be used and waiting for an instruction The operating system creates a virtual environment (virtual machine) for the application to work in and allots it a segment of virtual memory.

Multiprogramming instead of multitasking is not a good approach because a process could commit a resource and no other processes could use the resource until it was properly released by the first process.

Proper input/output management is a core component of operating systems. When a request for a resource is made, certain data structures are built and processes are dedicated for this action to take place. One the action takes place, the program or operating system needs to tear down these built structures and release the resources back into a pool to be available for other programs and processes. If this does not happen properly, a deadlock situation ca n occur.

Another common deadlock situation is when process A commits resource 1 and needs to use resource 2 to properly complete its task. But process B has commited resource 2 and needs resource 1 to finish its job.

Hence, both processes are "hung" because they do not have the resources they need to finish the function they are to carry out.

If protection is implemented at the hardware layer, the protection mechanisms will be more simplistic and provide broad and general protection. As we ascend up the layers, more complxity is added and functionality becomes more specific and granular. The top layer holds the most complexity because it is directed toward providing the user with a vast amoung of functionality and options.

As functionality increases, complexity increases and the assurance of security decreases.

The trusted computing base (TCB) is defined as the total combination of protection mechanisms within a computer system. The TCB includes hardware, software and firmware. These are a part of the TCB because the system is sure that these components will enforce the security policy and not violate it.

TCB originated from the Orange Book and does not address the level of security a system provides, but the level of trust, albeit from a security sense.

The Orange Book defines a trusted system as hardware and software that utilizes measures to protect the integrity of unclassified or classified data for a range of users without violating access rights and the security policy.

A security perimeter is a boundary that divides the trusted from the untrusted.

The reference monitor is an abstract machine, which mediates all access subjects have to objects to ensure that subjects have the necessary access rights and to protect the objects from unauthorized access and destructive modification.

The security kernel is made up of mechanisms that fall within the TCB and implements and enforces the reference monitor concept. There are four main requirements of the security kernel:

- It must provide isolation for the processes carrying out the reference monitor concept and they must be tamperproof.

- The reference monitor must be invoked for every access attempt and must be impossible to circumvent.

Thus, the reference monitor must be implemented in a complete and foolproof way.

- The reference monitor must be verifiable as being correct. This means that all decisions made by the reference monitor should be written to an audit log and verified as being correct

- It must be small enough to be able to be tested and verified in a complete and comprehensive manner.

A domain is defined as a set of objects that a subject is able to access.

A program that resides in a privileged domain needs to be able to execute its instructions and process its data with the assurance that programs in a different domain cannot negatively affect its environment. This is referred to as an execution domain.

A security domain has a direct correlation to the protection ring that a subject or object is assigned to.

The lower the protection ring number, the higher the privilege and the larger the security domain.

Hardware segmentation of memory – memory is separated physically instead of just logically. This adds another layer of protection to ensure that a lower-privileged process does not access and modify a higher-level process' memory space.

A security policy is a set of rules and practices dictating how sensitive information is managed, protected and distributed. A security policy expresses exactly what the security level should be by setting the goals of what the security mechanisms are to accomplish.

Security policies that prevent information from flowing from a high security level to a lower security level are called multilevel security policies.

Least privilege means that a process has no more privileges than necessary to be able to fulfill its functions.

Layering further separates processed and resources and adds modularity to the system. The layers can communicate, but only through detailed interfaces that uphold the security integrity of the system.

When it is required that processes in different layers do not communicate and they are not supplied with interfaces to interact with each other, this is referred to as data hiding.

When a class of objects is assigned specific perimissions and acceptable activities are defined, it is called abstraction. This makes management of different objects easier because classes can be dealt with instead of each and every individual object.

When a class is defined, all the objects within that class are assigned an abstract data type, which is a precise definition of the format the object will accept data and the format it will present its processed data to other objects and subjects.

The security policy provides the abstract goals and the security model provides the dos and don'ts necessary to fulfill these goals.

State machine models use states to track and verify the security of a system. A system that has employed a state machine model will be in a secure state in each and every instance of its existence.

A system that employs the Bell-LaPadula model is called a multilevel security system because users with different clearances use the systems and the systems process data with different classifications. The Bell-LaPadula model is a state machine model enforcing the confidentiality asect of access control.

The level at which information is classified determines the handling procedures that should be used.

A lattice is an upper bound and lower bound of authorized access. Mandatory access control is based on a lattice of security labels.

Bell-LaPadula model is also an information flow security model, which means that information does not flow in an insecure model.

Bell-LaPadula model is a subject-to-object model.

The simple security rule states that a subject at a given security level cannot read data that resides at a higher security level. [no read up] The *-property rule states that a subject in a given security level cannot write information to a lower security level. [no write down] The strong star property rule states that a subject that has read and write capabilities can only perform those functions at the same security level, nothing higher and nothing lower.

The definition of the Basic Security Theorem is that if a system initializes in a secure state and all state transitions are secure, then every subsequent state will be secure no matter what inputs occur.

Criticisms of Bell-LaPadula model:

- It deals only with confidentiality and does not address integrity.

- It does not address management of access control because there is no mechanism to modify access rights.

- The model does not prevent or address covert channels.

- The model does not address file sharing used in more modern systems.

The Biba model uses a state machine model and is very similar to the Bell-LaPadula model. Biba addresses the integrity of data being threatened when subjects at lower integrity levels are able to write to objects at higher integrity levels and when subjects can read data at lower levels.

No write up rule states that a subject cannot write data to an object at a higher intergrity level.

No read down rule states that a subject cannot read data from an object at a lower integrity level.

The Bell-LaPadula model is used to provide confidentiality. The Biba model is used to provide integrity.

The Bell-LaPadula and Biba models are informational flow models becausethey are most concerned about data flowing from one level to another.

Bell-LaPadula uses security levels and Biba uses integrity levels.

In the Clark-Wilson model, users cannot access and manipulate objects directly, but must access the object through a program.

Ensuring that subjects can only access objects through the use of an application is referred to as an access triple. A subject has to go through an application to access an object.

The Clark-Wilson model also enforces separation of duties, which divides an operation into different parts and requires different users or rules to perform each part.

Goals of Integrity:

- Prevent unauthorized users from making modifications

- Prevent authorized users from making improper modifications

- Maintain internal and external consistency Clark-Wilson model addresses each of these goals in its model. Biba only addresses the first goal.

Noninterference is implemented to ensure that any actions that take place at a higher security level do not affect or interfere with actions that take place at a lower level.

The Brewer and Nash model, also called the Chinese Wall model, was created to provide access controls that can change dynamically depending upon a user's previous actions. The main goal of this model is to protect against users accessing data that could be seen as a conflict of interest.

Graham-Denning model is a model that creates rights for subjects, which correlate to the operations that can be executed on objects.

Harrison-Ruzzo-Ullman model is a model that allows for access rights to bechanged and specifies how subject and objects should be created and deleted.

A system is operating in a dedicated security mode if all users have the clearance and formal need-to-know to all data processed within the system. All users have been given formal access approval for all information on the system and have signed nondisclosure agreements pertaining to this information. The system can handle a single classification level of information.

A system is operating in system-high security mode when all users have a security clearance or authorization to access the information but not necessarily a need-to-know for all the information processed on the system. This mode also requires all users to have the highest level of clearance required by any and all data on the system.

A system is operating in compartmented security mode when all users have the clearance to access all the information processed by the system, but might not have the need-to-know or formal access approval. In this mode, users can access a segment or compartment of data only.

A system is operating in multilevel security mode when it perimts two or more classification levels to be processed at the same time when all the users do not have the clearance or formal approval to access all the information being processed by the system.

A trusted system means that all protection mechanisms work together to process sensitive data for many types of uses but till keeps the same secure detail. Assurance looks at the same issues but with more depth and detail. Systems that provide higherlevels of assurance means that their designs were thoroughly inspected, the development stages were reviewed, the technical specifications and test plans were evaluated and the system was tested extensively.

A security evaluation examines the security-relevant parts of a system, meaning the TCB, access control mechanisms, reference monitor, kernel and protection mechanisms.

Trusted Computer System Evaluation Criteria (TCSEC) is used to evaluate operating systems, applications and different products. Also known as the Orange Book.

TCSEC provides a graded classification of systems that is divided into hierarchical divisions of security levels:

- A    Verified protection

- B    Mandatory protection

- C    Discretionary protection

- D    Minimal security Each division above can have one or more numbered classes; the classes with higher numbers indicate a greater degree of trust and assurance.

TCSEC criteria can be broken down into seven different areas:

- Security policy – the policy must be explicit and well defined and enforced by the mechanisms within the system

- Identification – individual subjects must be uniquely identified

- Labels – access control labels must be associated properly with objects

- Documentation – this includes the test, design, specification documents, user guides and manuals

- Accountability – audit data must be captured and protected to enforce accountability

- Life cycle assurance – software, hardware and firmware must be able to be tested individually to ensure that each enforces the security policy in an effective manner throughout their lifetimes

- Continuous protection – the security mechanims and the system as a whole must perform predictably and acceptably in different situations continuously Each division and class incorporates the requirements of the ones below it. E.g. B3 has its requirements to fulfill along with those of C1, C2, B1 and B2.

Products are submitted to the National Computer Security Center (NCSC) for evaluation. Theprocess of evaluation is called the Trusted Products Evaluation Program (TPEP). Successfully evaluated products are placed on the Evaluated Products List (EPL).

D – Reserverd for systems that have been evaluated but fail to meet the criteria and requirements of the higher divisions.

C1 – Discretionary security protection. The environment that would require this rating would be where users are processing information at the same sensitivity level; thus, strict access control and auditing measures are not required. It would be a trusted environment with low security concerns.

C2 – Controlled access protection. This class requires a more granular method of providing access control.

The system must enforce strict logon procedures and provide decision-making capabilities when subjects request access to objects. The architecture must provide resource or object isolation so proper protection can be applied to the resource and that actions taken upon it can be properly audited.The object reuse concept must alod be invoked, meaning that any medium holding data must not contain any remnants of information after it is released for another subject to use. The environment that would require systems with a C2 rating would be one that contains users that are trusted but a certain level of accountability is required. C2, overall is regarded to be the most reasonable class for commercial applications, but the level of protection is still relatively weak.

B – in general based on Bell-LaPadula and must show evidence of reference monitor enforcement.

B1 – Labeled security. Each data object must contain a classification label and each subject must have a clearance label. It is intended for environments that require systems to handle classified data.

B2 – Structured protection. This class adds assurance by adding requirements to the design of the system.

The environment that would require B2 systems could process sensitive data that requires a higher degree of security. This environment would require systems that are relatively resistant to penetration and compromise.

B3 – Security domains. More granularity is provided in each protection mechanism. An environment that requires B3 systems is a highly secured environment that processes very sensitive information. It requires systems that are highly resistant to penetration.

A1 – Verified design. Assurance of an A1 system is higher than a B3 system because the formality in the way the system was designed, the way the specifications were developed and the level of detail in the verification techniques. An environment that would require A1 systems is the most secure of secured environments. This environment deals with top-secret information and cannot adequately trust anyone using the systems without strict authentication, restrictions and auditing.

TCSEC addresses confidentiality, but not integrity. Functionality of the security mechanims and the assurance of those mechanisms are not evaluated separately, but combined and rated as a whole.

Criticisms of the Orange Book:

- The Orange Book looks specifically at the operating system and not other issues like networking, databases and so on.

- The Orange Book focuses mainly on confidentiality and not at integrity, availability and authenticity.

- The Orange Book works with government classifications and not the protection classifications that commercial industries use.

- The Orange Book has relatively small number of ratings, which means many different aspects of security are not evaluated and rated independently.

The Trusted Network Interpretation (TNI), also called the Red Book, addresses security evaluation topics for networks and network components. It addresses isolated local area networks and wide area internetwork systems. The Red Book rates confidentiality and integrity of data and operations that happen within a network and the network products.

Communication integrity:

- Authentication – protects against masquerading and playback attacks. Mechanisms include digital signatures, encryption, timestamp and passwords.

- Message integrity – protects protocol header, routing information and the packet payload from being modified. Mechanisms include message authentication and encryption.

- Nonrepudiation – Ensures that a sender cannot deny sending a message. Mechanisms include encryption, digital signatures and notary.

Denial-of-service prevention:

- Continuity of operations – ensures that network is available even if attacked. Mechanisms include fault tolerant and redundant systems and the capability to reconfigure network parameters in case of an emergency.

- Network management – monitors network performance and identifies attacks and failures.

Mechanisms include components that enable network administrators to monito and restrict resource access.

Compromise protection:

- Data confidentiality – protects data from being accessed in an unauthorized method during transmission. Mechanisms include access controls, encryption and physical protection of cables.

- Traffic flow confidentiality – ensures that unauthorized entities are not aware of routing information or frequency of communication via traffic analysis. Mechanisms include padding messages, sending noise or false messages.

- Selective routing – routes messages in a way to avoid specific threats. Mechanisms include network configuration and routing tables.

Red Book Ratings:

- None

- C1 – Minimum

- C2 – Fair

- B2 – Good Information Technology Security Evaluation Criteria (ITSEC) was the first attempt at establishing a single standard for evaluating security attributes of computer systems by many European countries. ITSEC is only used in Europe. There are two main attributes of a system when it is evaluated under ITSEC: functionality and assurance.

F1 to F10 rate the functionality of the system, whereas E0 to E6 rate the assurance of a system.

ITSEC TCSEC E0 = D F1 + E1 = C1 F2 + E2 = C2 F3 + E3 = B1 F4 + E4 = B2 F5 + E5 = B3 F5 + E6 = A1 F6 = systems that provide high integrity F7 = systems that provide high availability F8 = systems that provide data integrity during communication F9 = systems that provide high confidentiality (like cryptographic devices) F10 = networks with high demands on confidentiality and integrity Common Criteria – coming together of evaluation criteria. An evaluation is carried out on a product and is assigned an evaluation assurance level (EAL). The thoroughness and stringent testing increases in detail-oriented tasks as the levels increase.

EAL 1 Functionally tested EAL 2 Structurally tested EAL 3 Methodically tested and checked EAL 4 Methodically designed, tested and reviewed EAL 5 Semiformally designed and tested EAL 6 Semiformally verified design and tested EAL 7 Formally verified design and tested The Common Criteria uses protection profiles to evaluate products. The protection profile contains the set of security requirements, their meaning and reasoning, and the corresponding EAL rating that the intended product will require. Protection profile contains the following five sections:

- Descriptive elements

- Rationale

- Functional requirements

- Development assurance requirements

- Evaluation assurance requirements Protection Profile [Request for a specific security solution] Target of Evaluation [The product] Security Target [Vendor's explanation of functionality and assurance components] Security Functionalit y and [Different families of the classes in requirement sets] Security Assurance Requirements Evaluation [Testing and evaluation of product against claimed specifications] Evaluation Assurance Level Assigned Certification is the comprehensive technical evaluation of the security components and their compliance for the purpose of accreditation.

Accreditation is the formal acceptance of the adequacy of a system's overall security and functionality by management.

The British Standard 7799 is a risk-based method for assessing, evaluating and managing risks. It is divided into ten sections:

- Security policy

- Security organization

- Assets classification and control

- Personnel security

- Physical and environmental security

- Computer and network management

- System access control

- System development and maintenance

- Business continuity planning

- Compliance ISO 17799 – referred to as the Code of Practice for Information Security Management Systems that are described as open are built upon standards, protocols and interfaces that have published specifications, which enable third-party vendors to develop add-on components and devices.

Systems that are referred to as closed use an architecture that does not follow industry standards.

Interoperability and standard interfaces are not employed to enable easy communication between different types of systems and add-on features.

A covert channel is a way for an entity to receive information in an unauthorized manner. It is an information flow that is not controlled by a security mechanism or the mechanism has been successfully compromised.

In a covert timing channel, one process relays information to another by modulating its use of system resources. (e.g. If one process writes to the hard disk 30 times in 30 secs, then a second process that is watching for this signal, initiates its malicious intent.) A covert storage channel is when a process writes data to a storage location and another process directly or indirectly reads it. The problem occurs when the processes are at different security levels.

Most common covert channel in usetoday is the Loki attack, which uses the ICMP protocol for communication purposes. A tool called Loki allows an attacker to write data behind the ICMP header.

An overt channel is a channel of communication that was developed specifically for communication purposes.

An asynchronous attack deals with the sequences of steps a system uses to complete a task. Involves a time-of-check versus time-of-use attack (e.g. Replacing autoexec.bat file between when the boot process checks for the autoexec.bat file and when the autoexec.bat file is actually processed).

When two different processes need to carry out their tasks on a resource, they need to follow the correct sequence. If the sequence is not followed, a race condition is encountered.

Buffer overflows happen when programs do not check the length of data that is inputted into a program.

Extra data inputted can launch another program or be a set of code that was devised to perform disruptive behavior in the system. This is sometimes referred to as smashing the stack.

A buffer overflow is usually aimed at systems that let the extra code be executed with privileged rights.
