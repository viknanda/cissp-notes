# Applications Security

A database management system (DBMS) is usually a suite of programs used to manage large sets of structured data with ad hoc query capabilities for many types of users. These can also controls the security parameters of the database.

A database is a collection of data stored in a meaningful way that enables multiple users and applications to access, view and modify data as needed.

Record – collection of related data items File – collection of records of the same type Database – cross-referenced collection of files DBMS – manages and controls the database Base relation – a table stored in a database Tuple – a row in a two-dimensional database Attribute – a column in a two-dimensional database Primary key – columns that make each row unique (A table must include a primary key for ever row) View – virtual relation defined by the database to keep subjects from viewing certain data Foreign key – attribute of one table that is the primary key of another table Cell – intersection of a row and column Schema – holds data that describes a database Data dictionary – central repository of data elements and their relationships The database model defines the relationships between different data elements, dictates how data can be accessed and defines acceptable operations, the type of integrity offered and how data is organized.

A relational data model uses attributes and tuples to contain and organize information. Relational databases hold data in table structures.

Hierarchical databases use a tree structure and a parent/child relationship.

A distributed data model has data stored in more than one database, but is logically connected.

An object-oriented database is designed to handle a variety of data. The objects within the database contain information that is used to access the objects actually containing these different data types and defines their properties.

An object-oriented database is more dynamic in nature when compared with a relational database because objects can be created when needed, and the data and procedure go with the object when it is requested.

In a relational database, an application uses its procedures to obtain data from the database. The database does not actually provide procedures as object-oriented databases do. The object-oriented database has classes to define the attributes and procedures of its objects.

Database Interface Languages:

- Open Database Connectivity (ODBC) – an application programming interface (API) that allows an application to communicate with a database either locally or remotely. The application sends requests to the ODBC, which in turn translates them into database commands. ODBC tracks down the necessary database driver for the application.

- Object Linking and Embedding Database (OLE DB) – separates data into components that run as middleware on a client or server. It provides a low-level interface to link information across different databases and provides access to data no matter where it is located or how it is formatted.

- ActiveX Data Objects (ADO) – an API that allows applications to access back-end database systems. It is a set of ODBC interfaces that expose the functionality of a database through accessible objects. The ADO uses the OLE DB interface to connect with the database and can be developed with many different scripting languages.

- Java Database Connectivity (JDBC) – an API that allows a Java application to communicate with a database. The application can connect through ODBC or directly to the database.

- EXtensible Markup Languag (XML) – a standard for structuring data so that it can be easily shared by application using Web technologies. It is a markup language that is self-defining and provides a lot of flexibility in how information within the database is presented.

Data definition language (DDL) – defines the structure and schema of the database. The structure could mean the table size, key placement, views and data element relationship.

Data manipulation language (DML) – exmaines and manipulates the data within the database. It contains all the commands that enable a user to view, manipulate, and use the database.

Data control language (DCL) – defines the internal organization of the database.

Query language (QL) – this is for users to make queries and access the data within the database.

A data dictionary is a central repository of data elements and their relationships. It stores critical information about data usage, data relationships, data sources and data formats.

If an attribute in one table has a value matching the primary key in another table, this attribute is considered a foreign key.

Concurrency has to do with making sure that different subjects receive the most up-to-date information and ensures that the database can properly handle various requests at the same time.

Locking ensures that two processes do not access the same table at the same time.

A semantic integrity mechanism makes sure that structural and semantic rules are enforced. These rules pertain to data types, logical values, uniqueness constraints and operations that could adversely affect the structure of the database.

A database has referential integrity if all foreign keys reference existing primary keys. There should be a mechanism in place that ensures no foreign key would contain a reference to a primary key of a nonexisting record, or a null value.

Entity integrity guarantees that the tuples are uniquely identified by primary key values.

The rollback is a statement that ends a current transaction and cancels all other changes to the database.

The commit statement terminates a transaction and executes all changes that were just made by the user.

Savepoints are used to make sure that if a system failure occurs, or if an error is detected, the database can attempt to return to a point before the system crashed or hiccupped.

“Checkpoints” are very similar to savepoints. When the database software fills up a certain amount of memory, a checkpoint is initiated, which saves the data from the memory segment to a temporary file. If a glitch is experienced, the software will tryand use this information to restore the user's working environment to its previous state.

Aggregation happens when a user does not have the clearance or permission to access the components of this information.

Aggregation is the act of combining information from separate sources. The combination of the information forms new information, which the subject does not have the necessary rights to access. The combined information has a sensitivity that is greater than the individual parts.

Inference is the ability to derive information that is not explicitly available.

Database security looks at the contents of a file when it makes an access control decision, which is referred to as content-dependent access control.

Cell suppression is a technique used to hide or not show specific cells that contain information that could be used in inference attacks.

Partitioning a database involves dividing the database into different parts, which makes it much harder for an unauthorized individual to find connecting pieces of data that can be brought together and other information that can be deduced or uncovered.

Noise and perturbation is a technique of inserting bogus information in the hopes of misdirecting an attacker or confusing the matter enough that the actual attack will not be fruitful.

Polyinstantiation enables a relation to contain multiple tuples with the same primary keys, with each instance distinguished by a security level.

Polyinstantiation is a process of interactively producing more detailed version of objects by populating variables with different values or other variables. It is often used to prevent inference attacks.

Online transaction processing (OLTP) is usually used when databases are clustered to provide fault tolerance and higher performance. OLTP provides mechanisms that watch for problems and deal with them appropriately when they do occur.

ACID test:

- Atomicity – divides transactions into units of work and ensures that all modifications take effect or none takes effect. The changes are either committed or the database is rolled back.

- Consistency – a transaction must follow the integrity policy developed for that particular database and ensure that all data is consistent in the different databases.

- Isolation – transactions execute in isolation until completed, without interacting with other transactions.

The results of the modification are not available until the transaction is completed.

- Durability – once the transaction is verified as accurate on all systems, it is committed and the databases cannot be rolled back.

Data warehousing combines data from multiple databases or data sources into a large database with the purpose of a fuller extent of information retrieval and data analysis.

Data mining is the process of analyzing a database using tools that look for trends, correlations, relationships and anomalies without having the knowledge of the meaning of the data.

Data mining is also known as Knowledge Discovery in Database (KDD) and is a combination of techniques to identify valid and useful patterns. Following three approaches are used:

- Classification – data is grouped together according to shared similarities

- Probabilistic – data interdependencies are identified and probabilities are applied to their relationships

- Statistical – identifies relationships between data elements and uses rule discovery Metadata is the result of storing data within a database and mining the data with tools.

System Development Lifecycle:

- Project initiation

- Conception of project definition

- Proposal and initial study

- Initial risk analysis

- Functional design analysis and planning

- Requirements uncovered and defined

- System environment specifications determined

- Formal design created

- System design specifications

- Functional design review

- Functionality broken down

- Detailed planning put into placement

- Code design

- Software development

- Developing and programming software

- Installation/implementation

- Product installation and implementation

- Testing and auditing

- Operational/maintenance

- Product changes, fixes and minor modifications

- Disposal

- Replace product with new product Verification determines if the product accurately represents and meets the specifications. A product can be developed that does not match the original specifications. This step ensures that the specs are properly met.

Validation determines if the product provides the necessary solution for the intended real-world problem.

In large projects, it is easy to lose sight of the overall goal. This exercise ensures that the main goal of the project is met.

Trapdoors or maintenance hooks are lines of code that allow developers to bypass any security and access controls so that they can quickly access the application's code by means of a few keystrokes.

Trapdoors and maintenance hooks should be removed before the code goes into production.

Software Development Methods:

- Waterfall – a classical method that uses discrete phases of development that require formal reviews and documentation before moving into the next phase of the project

- Spiral Model – a method that builds upon the waterfall method with an emphasis on risk analysis, prototypes and simulations at different phases of the development cycle

- Joint Analysis Development (JAD) – uses a team approach in application development in a workshop- oriented environment

- Rapid Application Development (RAD) – a method of determining user requirements and developing systems quickly to satisfy immediate needs

- Cleanroom – an approach that attempts to prevent errors or mistakes by following strcutured and formal methods of developing and testing. This approach is used for high-quality and critical applications that will be put through a strict certification process Change control is a process to manage and approve of any type of change within the environment.

Changes must be authorized, tested and recorded. Changed systems may require recertification and reaccreditation.

Configuration management is the procedures that are used to carry out changes that affect the network, individual systems or software.

Identifying, controlling, accounting for and auditing changes made to the baseline TCB, which includes changes to hardware, software and firmware.

A system that will control changes and test documentation through the operational life cycle of a system.

Change Control Process:

- Make a formal request for a change

- Analyze the request

- Develop the implementation strategy

- Calculate the costs of this implementation

- Review any security implications

- Record the change request

- Submit the change request for approval

- Develop the change

- Recode segments of the product and add or subtract functionality

- Link these changes in the code to the formal change control request

- Submit software for testing and quality approval

- Repeat until quantity is adequate

- Make version changes

- Report results to management The Capability Maturity Model (CMM) describes procedures, principles and practices that underlie software development process maturity. Maturity levels used:

- Initial – development process is ad hoc or even chaotic. The company does not use effective management procedures and plans. There is no assurance of consistency and quality is unpredictable.

- Repeatable – a formal management strcuture, change control and quality assurance is in place. The company can properly repeat processes throughout each project. The company does not have formal process models defined.

- Defined – formal procedures are in place that outline and define processes that are carried out in each project. The organization has a way to allow for quantitative process improvement.

- Managed – the company has formal processes in place to collect and analyze qualitative data and metrics are defined and fed into the process improvement program.

- Optimizing – the company has budgeted and integrated plans for continuous process improvement.

Software escrow means that there is a third party involved and this third party will keep a copy of the source code and possibly other materials, which will only be released to the customer if specific circumstances arise (e.g. if the software company went out of business).

Machine language is in a form that the processor can understand and work with directly. Assembly and high-level languages cannot be understood directly by the processor and must be translated, which results in machine language.

Interpreters translate one command at a time during execution.

Compilers translate large sections of code at a time.

Assemblers translate assembly language into machine language.

In object-oriented programming (OOP), objects are unique instances of a data structure defined by the template provided by their corresponding classes.

A method is the functionality or procedure that an object can carry out.

Data hiding is provided by encapsulation, which protects an object's private data from outside access. No object should be allowed to or have the need to access another object's internal data or processes.

Abstraction is the capability to suppress unnecessary details so that the important, inherent properties can be examined and reviewed. It enables the separation of conceptual aspects of a system.

Object-oriented design (OOD) is a design method where a system is modeled as a collection of cooperating objects. Each individual object is treated as an instance of a class within a class hierarchy.

Polymorphism is when different objects respond to the same command, input, or message in different ways.

Object-oriented analysis (OOA) is the process of classifying objects that will be appropriate for a solution.

Data modeling considers data independently of the way that the data is processed and of the components that process the data. A data model will follow an input value from the beginning to end and verify that the output is correct.

A data structure is a representation of the logical relationship between elements of data. It dictates the degree of association between elements, methods of access, processing alternatives nd the organization of data elements.

Examples of data structures include scalars, hierarchical trees and linked lists.

A cohesive module can perform a single task with little or no help from other modules.

Coupling is a measure of interconnection among modules in an application. The level of coupling involved between modules depends on the interface's complexity, the data being passed between the modules and the point of entry or reference made to the module itself. The lower the coupling, the better the software design because it promotes module independence.

Modules should be self-contained and perform a single logical function, which is high cohesion.

Modules should not drastically affect each other, which is low coupling.

Object Management Architecture (OMA) provides standards to accomplish a complete distributed environment.

Object request brokers (ORBs), which are system-oriented components, manage all communication between components and enable them to interact in a heterogeneous and distributed environment. ORB works independently of the platform where the objects reside, which provides greater interoperability.

Common Object Request Broker Architecture (CORBA) provides interoperability among the vast array of software, platforms and hardware in environments today. CORBA enables applications to communicate with one another no matter where the application is located or who developed it.

Clients request services from objects. ORB is the middleware that establishes the client/server relationship between objects.

Computer-aided software engineering (CASE) tools refer to tools used by programmers, developers, project managers and analysts to help them make program applications more quickly and with fewer errors in an automated fashion and run the project in a controlled and organized manner.

When automation covers the complete life cycle of a product, the tools are referred to as integrated computer-aided software engineering (I-CASE).

Component Object Model (COM) defines how components interact and provides an architecture for simple interprocess communication (IPC). Distributed Component Object Model (DCOM) supports the same model for component interaction, but supports distributed IPC.

COM enables applications to use components on the same systems.

DCOM enables applications to access objects that reside in different parts of a network.

DCOM works as middleware that enables distributed processing and provides developers with services that support process-to-process communication across networks.

DCOM provides ORB services, data connectivity services, distributed messaging services, and distributed transaction services layered over its RPC mechanism using the same interface as COM.

ODBC is a de facto standard that provides a standard SQL dialect that can be used to access many types of relational databases. ODBC is the middleman between applications and databases.

Object linking and embedding (OLE) provides a way for objects to be shared on a local personal computer and to use COM as their foundation. OLE enables objects to be embedded into documents, like graphics, pictures and spreadsheets.

The capability for one program to call another program is linking.

The capability to place a piece of data inside a foreign program or document is embedding.

ActiveX components are portable components and can be run on any platform supporting DCOM, using the COM model or communicating using DCOM services.

Dynamic Data Exchange (DDE) enables applications to share data by providing IPC. DDE is a communication mechanism that enables direct conversation between two applications.

Distributed computing environment (DCE) is a standard that was developed by the Open Software Foundation (OSF). It is middleware that has the capability to support many types of applications across an enterprise. DCE provides an RPC service, security service, directory service, time service and distributed file support.

DCE and DCOM provide a lot of the same functionality. DCOM was developd by Microsoft and is proprietary in nature.

DCOM uses a globally unique identifier (GUID) and DCE uses a universal unique identifier (UUID). They are both used to identify users, resources and components within an environment.

Enterprise Java Bean (EJB) is a structural design for the development and implementation of distributed applications written in Java. The EJB uses the Internet Inter-ORB Protocol (IIOP), for which the client portion does not have to be a program written in Java but can be any valid CORBA client.

An expert system is a computer program containing a knowledge base and a set of algorithms and rules used to infer new facts from knowledge and incoming data.

Expert systems are also known as knowledge-based systems and use artificial intelligence (AI) to solve problems.

Rule-based programming is a common way of developing expert systems.The rules are based on if-then logic units.

Expert systems use automatic logical processing, inference engine processing and general methods of searching for problem solutions.

An artificial neural network (ANN) is an electronic model based on the neural structure of the brain.

Decisions by neural networks are only as good as the experiences they are given.

Walkthrough of Java applet processing:

- Programmer creates a Java applet and runs it through a compiler

- The Java compiler converts the source code into bytecode (non-processor specific)

- The user downloads the Java applet

- If the user's browser is Java-enabled and has a Java Virtual Machine installed, the broswer knows what to do

- The Java Virtual Machine converts the bytecode into machine-level code (processor specific)

- The applet runs When source code is processed by a compiler, the result is object code, which is written for a specific platform and processor. This object code is the executable form of an application that a user purchases from a vendor.

When the object code runs, it must be converted into binary machine code, which is what the processor actually understands.

Java applets use a security scheme that employs a sandbox to limit the applet's access to certain specific areas within the user's system and protects the system from malicious or poorly written applets.

A trusted Java applet is so called because it provides a digital signature and has access to all system resources; it is not confined to a sandbox. Such an applet is developed by in-house programmers and distributed within an intranet to perform some type of business-oriented functionality.

ActiveX is a Microsoft technology that is used to write controls that Internet users can download to increase their functionality and Internet experience.

Java sets up a sandbox for the code to execute in and this restricts the code's access to resources within the sandbox. ActiveX uses Authenticode technology that relies on digital certificates and trusting certificate authorities.

Malicious code can be detected in the following way:

- File size increase

- Many unexpected disk accesses

- Change in update or modified timestamp

- Sudden decrease of hard drive space

- Unexpected and strange activity by applications A “pseudo-flaw” is code inserted into an application on purpose to trap potential intruders.

A virus is a program that searches out other programs and infects them by embedding a copy of itself.

When the infected program executes, the embedded virus is executed, which propagates the infection.

A macros virus is a virus written in a macro language and is platform independent. Macro viruses infect and replicate in templates and within documents.

Boot sector viruses infect the boot sector of a computer and either move data within the boot sector or overwrite the sector with new information.

Compression viruses append themselves to executables on the system and compress them using t the user's permissions.

A stealth virus hides the modifications that it has made to files or boot records.

A polymorphic virus produces varied but operational copies of itself.

A multipart virus infects both the boot sector of a hard drive and executable files. The virus first becomes resident in memory and then infects the boot sector.

A self-garbling virus attempts to hide from antivirus software by garbling its own code. As the virus spreads, it changes the way its code is formatted. A small portion of the virus decodes the garbled code when activated.

Meme viruses are not actually viruses but types of emails that continually get forwarded around the Internet.

An EICAR test is done with antivirus software by introducing a benign virus to test the detection and reaction activities of the software.

Worms are different than viruses in that they can reproduce on their own without a host application and in that they are self-contained programs. A worm can propagate itself using email, TCP/IP and disk drives.

A logic bomb will execute a program, or string of code, when a certain event happens of a date and time arrives.

A Trojan horse is a program that is disguised as another program and contains hidden code exploiting the authorization process to violate security.

Different interpretations of RFCs by operating systems and vendors lead to slightly different network stacks, which contain their own flaws that can be taken advantageof to produce a denial-of-service (DoS) attack.

Internet Control Message Protocol (ICMP) is the mini-messenger of Internet Protocol (IP) and is used to find out what systems are up and running.

A sends ICMP ECHO REQUEST to B B responds with ECHO REPLY to A Smurf attack requires three players: the attacker, the victim and the amplifying network.

Attacker spoofs or changes the source IP address in a header to make an ICMP ECHO REQUEST packet seem as though it originated at the victim's system.

This ICMP ECHO REQUEST message is broadcast to the amplifying network, which will reply to the message in full force.

The victim system and victim's network are overwhelmed.

Countermeasures:

- To make sure that a certain network is not used as an amplifying site, direct broadcast functionality can be disabled at the border routers.

- Packets that contain internal source IP addresses should not be accepted by perimeter routers as incoming messages. These packets are spoofed.

- Only the necessary ICMP traffic should be allowed into and out of an environment.

- A network IDS should be employed to watch for suspicious activity.

- Some systems are more sensitive to certain types of DoS, and patches have already been released. The appropriate patches should be applied.

Fraggle is an attack similar to smurf, but instead of using ICMP, it uses User Datagram Protocol (UDP) as its weapon of choice. Countermeasures are similar to those for smurf attacks.

TCP connection:

A sends a SYN to B B responds with a SYN/ACK to A A responds with an ACK to B, establishing a TCP connection SYN Flood involves continually sending a victim SYN messages with spoofed packets. The victim will commit the necessary resources to set up this communication socket and it will send its SYN/ACK message waiting for the ACK message in return. The victim will never receive the ACK message because the packet is spoofed. When this happens repeatedly, the victim system has no more resources to open up another connection (until the existing connections time out).

Countermeasures:

- Decrease the connection-established timeout period.

- Increase the size of the connection queue in the IP stack.

- Proper patches have to be installed to address the different ways that different vendors have to deal with SYN attacks.

- A network IDS can watch for this type of activity

- A firewall can watc for these types of attacks When packets travel through different networks, they may need to be fragmented and recombined depending on the network technology of each specific network. Each network technology has a maximum transmission unit (MTU), which indicates the largest packet size it can process. Some systems make sure that packets are not too large, but do not check to see if a packet is too small. The receiving system, the victim, would receive the fragments and attempt to recombine them but these fragments have been made in such a way that they cannot be properly reassembled. This basically constitutes the teardrop attack.

Countermeasures:

- Install necessary patch or upgrade operating system

- Disallow malformed fragments of packets to enter environment

- Use a router that will combine all fragments into a full packet prior to routing it to the destination systems In a DDoS attack, an attacker uses masters to control zombies to overwhelm the victim with requests.

Countermeasures:

- Perimeter routers restrict unnecessary ICMP and UDP traffic

- A network IDS can be employed to watch for this type of suspicious activity

- Disable unused subsystems and services on computers

- Rename administrator account and implement strict password management so systems cannot be used unknowingly

- Packets that contain internal source IP addresses should not be accepted by perimeter routers as incoming messages. These packets are spoofed.

DNS DoS attacks occur when a DNS record is replaced by inaccurate data and requests are redirected to a bogus website versus the real website.

If the actual DNS records are unattainable to the attacker for him to alter in this fasion, which they should be, the attacker can insert this data into the cache of the server instead of replacing the actual records, which is referred to as cache poisoning.

Countermeasures:

- DNS servers should have public and internal records. The public records serve Internet requests and contain no sensitive information pertaining to the internal network. The internal records should be unreachable from the Internet and are used to resolve queries from internal users.

- DNS servers should also be redundant by using a primary and secondary DNS server per zone.

- Different DNS BIND versions have different vulnerabilities. The BIND version should be updated.

- Employe secure DNS.

When Security DNS (DNSSEL) is implemented, the secondary DNS servers must authenticate the systems that are updating their records. Integrity checks are also performed to ensure that records were not modified or corrupted during transmission. Secure DNS protects DNS servers from having their records updated by unauthorized sources.

Timing Attacks:

- Between the lines entry attack – The attacker taps into and uses an active communication line. The user may not be using the connection at that time, but it is still activem so the attacker jumps in and uses it.

- NAK/ACK attack – A NAK is a negative acknowledgement to tell a system that a certain piece of information was not received or that a certain message or parameter is unacceptable. Some systems do not deal with negative acknowledgements properly, and attackers use this weakness to their advantage.

- Line disconnect attack – An attacker may access and keep a communication session open after the user attempts to terminate it. In this case the user drops off, thinking the connection is closed, but actually the attacker kept the connection active and is now using it.
