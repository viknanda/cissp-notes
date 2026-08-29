# Access Controls

Access control is the collection of mechanisms that permits managers of a system to exercise a directing or restraining influence over the behavior, use and content of a system. It permits management to specify what users can do, which resources they can access and what operations they can perform on a system.

Access is the flow of information between a subject and an object.

A subject is an active entity that requests access to an object or the data within an object.

An object is a passive entity that contains information.

Availability ensures that information, systems and resources are available to users in a timely manner so as to not affect productivity.

Integrity ensures that information is accurate, complete and protected from unauthorized or unexpected modification.

Confidentiality is the assurance that information is not disclosed to unauthorized individuals, programs, or processes.

Identification --> Authentication --> Authorization Identification describes a method of ensuring that a subject (user, program, or process) is the entity it claims to be.

The subject needs to be held accountable for the actions taken within a syste m or domain.

Something a person knows: password, pin, mother's maiden name, combination to a lock (usuallyleast expensive) Something a person has: key, swipe card, access card, badge Something a person is: biometrics Strong authentication contains two out of three methods: something a person knows, has, or is. (Biometrics by itself does not constitute strong authentication.) Biometrics verifies an individual's identity by a unique personal attribute, which is one of the most effective and accurate methods of verifying identification.

Biometrics is a very sophisticated technology; thus, it is much more expensive and complex than the other types of identity verification processes.

Type I error: when a biometric system rejects an authorized individual.

Type II error: when the system accepts impostors who should be rejected.

Crossover error rate (CER) is a metric used to compare different biometric systems. It is stated in a percentage and represents the point at which the false rejection rate equals the false acceptance rate. CER of 3 is more accurate than CER of 4.

Fingerprints: made up of ridge endings and bifurcations exhibited by the friction ridges and other detailed characteristics that are called minutiae. Distinctiveness of these minutiae that gives each individual a unique fingerprint.

Palm scan: the palm has creases, ridges and grooves throughout it that are unique to a specific person. The palm scan also includes the fingerprints of each finger.

Hand geometry: shape of a person's hand (the length and width of the hand and fingers).

Retina scan: examines the blood-vessel pattern of the retina on the backside of the eyeball.

Iris scan: examines the colored portion of the eye that surrounds the pupil. The iris has unique patterns, rifts, colors, rings, coronas and furrows.

When using an iris pattern biometric system, the optical unit must be positioned so that the sun does not shine into the aperture.

Signature dynamics: examines the electrical signals produced by the physical motions performed when someone signs a document.

Keyboard dynamics: capture electrical signals when a person types a certain phrase.

Voice print: examines subtle distinguishing differences in people's speech sounds and patterns.

Facial scan: takes many attributes and characteristics into account such as, bone structures, nose ridges, eye widths, forehead sizes and chin shapes.

Hand topology: side-view picture of the hand is captured. Hand topology looks at the different peaks and valleys of the hand, along with its overall shape and curvature.

A password is a protected string of characters that is used to authenticate an individual.

Clipping level: a threshold set by an administrator to, e.g., lock a user out after a certain number of failed logon attempts.

Password checkers: tools used to detect weak passwords by performing a dictionary attack.

Password checkers are tools used by security professionals to test the strength of a password.

Password crackers are tools used by hackers.

Password aging involves setting an expiration date for passwords, forcing users to change them.

Cognitive passwords are fact-or opinion-based information used to verify an individual's identity. (Think help desk services.) One-time password is also called a dynamic password. It is used when a user needs to authenticate himself.

Synchronous token device synchronizes with the authentication service by using time or an event as the core piece of the authentication process.

Time-based: token device and authentication service must hold the exact same time within their internal clocks. Time value is encrypted with a secret key and displayed to the user.

Event-based: user may need to initiate the logon sequence on the computer and push a button on the token device. Again, authentication value is encrypted and displayed to the user.

[Note that token device and authentication service must share the same secret key for encryption and decryption.] Asynchronous token device uses a challenge/response scheme to authenticate the user.

Passwords are the weakest form of authentication and can be easily sniffed as they travel over a network.

A digital signature is a technology that uses a private key to encrypt a hash value (message digest).

A passphrase is another form of authentication and is transformed to a virtual password by an application when it is used for authentication.

A memory card holds information, but does not process information.

A smart card has the necessary hardware and logic to actually process information.

Access control mechanisms:

Roles Groups Physical or logical isolation Time of day or temporal isolation Transaction types Need-to-know is similar to the least-privilege principle.

Management: determine the security requirements of individuals and how access is authorized.

Administrator and IT staff: configure the access control.

Security officer: configures security mechanisms to fulfill these requirements.

Bottomline is that the owner determines security requirements of users.

Single sign-on allows a user to enter credentials one time and be able to access allresources in primary and secondary network domains. It also allows users to access, through the one set of credentials, all other resrouces that they have access to, including legacy and other application systems.

Kerberos is an example of a single sign-on system for distributed environments, and is a de-facto standard for heterogeneous networks. Kerberos uses symmetric key cryptography and provides end-to-end security.

Key Distribution Center (KDC) is the most important component within a Kerberos environment.

KDC holds all users' and services' cryptographic keys. It provides authentication services, as well as key distribution functionality. Clients and services trust the integrity of the KDC and this trust is the foundation of Kerberos security.

KDC provides security services to entities referred to as principals. The KDC and each principal share a secret key.

A ticket is generated by the KDC and given to a principal when that principal needs to authenticate to another principal.

KDC provides security services for a set of principals. This set is called a realm in Kerberos.

AS – authentication service is the part of the KDC that authenticates a principal.

TGS – ticket granting service is the part of the KDC that makes the tickets and hands them out to principals.

Kerberos implemented as an authenticator: identification and time stamp encrypted with session key. Time stamp is used to protect against replay attacks.

Weaknesses of Kerberos:

KDC is single point of failure Secret keys are temporarily stored on users' computers Session keys are decrypted and reside on users' computers SESAME – Secure European System for Applications in a Multi-vendor Environment SESAME is based on symmetric and assymetric cyrptography. Kerberos is strictly symmetric key-based technology.

Kerberos:Tickets as SESAME:Privileged Access Certificates KDC is roughly equivalent to the Priviledged Attribute Server A network service is a mechanism that identifies resources ona network and provides a way to makethem available to users and programs.

A network directory service contains information about these different resources and provides a naming scheme (LDAP, Novell's NDS and Microsoft's Active Directory).

An access control model is a framework that dictates how subjects access objects.

A system that uses discretionary access control (DAC) enables the owner of the resource to specify which subjects can access specific resources. Most common implementation of DAC is through ACLs.

Mandatory access control (MAC) model is based on a security label system; users are given a security clearance and data is classified by sensitivity labels.

A role-based access contrrol (RBAC) model (also called nondiscretionary access control) uses a centrally administered set of controls to determine how subjects and objectes interact. Best system for companies that have high employee turnover.

Group – generally a collection of users Role – generally a collection of access rights RBAC model can use role-based access, task-based access or, a lattive-based access.

Lattice-based access control provides an upper bound and lower bound of access capabilities for every subject and object reationship.

Rule-based access control is based on specific rules that indicate what can and cannot happen to an object.

An access contrl matrix is a table of subjects and objects indicating what actions individual subjects can take upon individual objects. Usually an attribute of DAC models. The access rights can be assigned directly to the subjects (capabilities) or to the objects (ACLs).

A capability table specifies the access rights a certain subject possesses pertaining to specific objects. A capability table is different from an ACL because the subject is bound to the capability table whereas the object is bound to the ACL.

In the Kerberos environment, the user is given a ticket, which is his capability table. The ticket is bound to the user and dictates what objects that user can access and to what extent.

Access contorl lists (ACLs) are lists of subjects that are autorized to access a specific object and they define what level of authorization is granted. Authorization can be specific to an individual, role, or group.

Content-based access refers to access decisioning based on the sensitivity of the data, not solely on subject identity.

Centralized access control administration refers to the fact that one entity is responsible for granting all users access to resources.

RADIUS – Remote Authentication Dial-In User Services (Dial-in user --> Modem pool --> Access server --> RADIUS server) TACACS – Terminal Access Controller Access Control System; combines its authentication and authorization processes XTACACS – separates authentication, authorization, and accounting processes TACACS+ – XTACACS with extended two-factor user authentication. TACACS+ and RADIUS provide the same functionality but RADIUS is an actual Internet standard whereas TACACS+ is a Cisco proprietary protocol.

Diameter is an authentication protocol that has the capability of authenticating many types of devices over different types of connections.

A decentralized access control administration method gives control of access to the people closer to the resources.

A hybrid access contol administration method is a combination of the centralized and decentralized access control administration methods. E.g. Administrator controls access to database, printer, intellectual information, host computer and fax. Data owners control access to their files and resources.

Acces s Control Layers:

Administrative Policy and Procedures Personnel controls Supervisory structure Security awareness training Testing Physical Controls Network segregation Perimeter security Computer controls Work area separation Data backups Cabling Technical Controls System access Network architecture Network access Encryption and protocols Auditing A security policy is a high-level plan stating management's intent pertaining to how security should be practiced within an organization, what actions are acceptable, and what level of risk the company is willing to accept.

Personnel controls indicate how employees are expected to interact with security mechanisms and noncompliance issues pertaining to these expectations.

Separation of duties should be enforced so no one individual can carry out a critical task alone that coule prove to be detrimental to the company.

Collusion means that more than one person would need to commit fraud and this effort would need to happen in a concerted effort. This drastically reduces the probability of security breaches and fraud.

Rotation of duties means that people know how to fulfill the obligations of more than one position.

Technical controls, also called logical controls, are the software tools used to restrict subjects' access to objects.

A control zone is a combination of technical and physical controls. It is a specific area that surrounds and protects network devices that emit electrical signals. It ensures that confidential information is contained and hinders intruders from accessing information through airwaves.

Access Control Types Preventive – Administrative Policies and procedures Effective hiring practices Pre-employment background checks Controlled termination procedures Data classification and labeling Security awareness Preventive – Physical Badges, swipe cards Guards, dog, motion detectors, CCTVs Fences, locks, mantraps, alarms Preventive – Technical Passwords, biometrics, smart cards Encryption, protocols, call-back systems, database views, constrained user interfaces Antivirus software, ACLs, firewalls, routers, clipping levels Locks are usually considered delay mechanisms because they will only delay a determined intruder.

Preventive – controls used to deter and avoid undesirable events from taking place Detective – controls used to identify undesirable events that have occurred Corrective – controls used to correct undesirable events that have occurred Deterrent – controls used to discourage security violations Recovery – controls used to restore resources and capabilities Compensation – controls used to provide alternatives to other controls An audit reduction tool reduces the amount of information within an audit log.

A variance detection tool can monitor computer and resource usage trends and detect variations.

Keystroke monitoring is a type of auditing that can review and record keystrokes entered by a user during an active session.

Tempest is the study and control of spurious electrical signals that are emitted by electrical equipment.

Tempest refers to standardized technology that suppresses signal emanations with shielding material and it is an actual standard.

A Faraday cage is a type of metal and materials with the necessary depth to ensure that only a certain amount of radiation is released.

Emanation security – electronic devices emit electrical radiation and this radiation can hold important information White noise is a uniform spectrum of random electrical signals. It is distributed over the full spectrum so that the bandwidth is constand and an intruder is not able to decipher real information from random noise or random information.

Knowledge-or Signature-based Intrusion Detection Each identified attack has a signature, which is used to detect an attack in progress or determine if one has occurred within the network.

Behavior-Based or Statistical Intrusion Detection Observes and detects deviation from expected behavior of users and systems.

A honeypot is a computer set up as a sacrificial lamb on the network; the system is not locked down and has open ports and services enabled.

Important to differentiate between enticement and entrapment. Entrapment is where the intruder is induced to commit a crime that they weren't originallycontemplating. Entrapment is illegal and cannot b used when charging an individual with hacking or unauthorized activity.

Dictionary attack – a program is fed lists (dictionaries) of commonly-used words or combinations of characters and the program compares these values to capture passwords. The program will hash the dictionary words and compare the resulting message digest with the system password file that also stores its passwords in one-way hashed format.

Brute force attack – an attack that continually tries different inputs to achieve a predefined goal.

Wardialing – a long list of phone numbers are inserted into a wardialing program in hopes of finding a modem that can be exploited to gain unauthorized access.

The goal of penetration testing is to identify vulnerabilities, estimate the true protection the security mechanisms within the environment are providing and see how suspicious activity is reported.

Discovery – footprinting and gathering information about the target Enumeration – performing port scans and resource identification methods Vulnerability mapping – identifying vulnerabilities is identified systems and resources Exploitation – attempting to gain unauthorized access by exploiting vulnerabilities Report to management – documentation of findings of test goes to management along with suggested countermeasures
