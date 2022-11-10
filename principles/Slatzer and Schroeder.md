# Information taken from CyBok Introduction v 1.0 
# Saltzer and Schroeder Principles *1975*
Initially developed in a context of engeneering a secure multi-user operation systems for use in Government and Military organisations

## Principles:
- *Economy of Mechanism*. The design of security system should remain small, since it is easier to reason and argue correctness. Also simpler systems are easier to audit or verify for high assurance. Introduces a notion of TCB - Trusted Component Base - list of trusted Hardware and software, wich needs to remain small in order to maintain security purposes
- *Fail-safe defaults*. Security controls need to define and enable operations that can positively be identified as being in accordance with a security policy, and reject all others. Need to identify a known good behaviour, rather than base controls on exclusion of detected violation.
- *Complete Mediation*. All operations on all objects in a system should be checked to ensure that they are in accordance with the security policy. Often done bu ensuring authorisation of all objects, presuming a strict authentrication mechanism.
- *Open Desing*. Security of the system should not rely on secrecy, bot on the set of the specified secrets, such as passwords. This principle enables Cyber Security to be a field of study, lets other professionals to examine systems.
- *Separation of Privilege*. Security controls that rely on multiple subjects to authorise an operation, provide higher assurance than those relying on a single subject.
- *Least Privilege*. Operations should be performed by users with least possible privileges
- *Least Common Mechanism*. It is preferable to minimise sharing of resources and system mechanisms between different parties.
- *Psychological Acceptability* - Security controls need to be naturally usable so that users may 'manually and routinely' apply protection

## Principles regarding security controls
- *Work Factor*. Security control should require more resources to circumvent than those available to adversary
- *Compromise Recording*. It is sometimes suggested that reliable records or logs, that allow detection of a compromise, may be used instead of controls that prevent a compromise. Most systems do log security events, and security operations heavily rely on such reliable logs to detect intrusions. The relative merits — and costs — of the two approaches are highly context-dependent.
