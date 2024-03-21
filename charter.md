# Background and Problem Space

The DNS protocol has traditionally had limited ability to signal to recursive resolvers about the capabilities of authoritative servers they communicate with.
In part, this stems from the inability of parents (often registries) to specify additional information about child delegations (often registrants) beyond NS, DS, and glue records.
Further complicating matters is the inability of a registrant to signal that the operation of a delegation point is being outsourced to a different operator, leaving a challenge when operators need to update parental information that is only in the control of the child.
A significant issue in today's deployed DNS that derives from these issues is data often being out of synchronization between parents and children. Said another way, children often have more up-to-date information about the nameservers and DNSSEC keying information than their parents due to slowness, or complete lack, of automated child-to-parent updates.

# Objective and Scope

To address these challenges, the working group will first develop the requirements for adding a new signaling mechanism that allows parents to return additional DNS delegation information about their children.

The working group will also list the other types of information not available today that might be provided over a designed signaling mechanism.

The potential first use cases for the working group will be new DNS authoritative signaling mechanisms for alternative DNS transports,
and delegation aliasing (where the parent returns a pointer to the service provider that will then return the needed delegation information).
The working group should also consider the how well different solutions can be deployed, and should study possible negative consequences of deploying alternative delegation mechanisms.

The working group will then define the semantics of a new signaling mechanism, taking future extensibility into account.

The working group will specify extensions to the DNS, EPP, and other protocols that relate to delegation.
The working group will coordinate with other working groups as appropriate.

# Deliverables

- A document listing the requirements for a new signaling mechanism allowing parents to return additional information when communicating about a delegated child.  This is expected to be published as an Informational RFC.

- A specification defining the new delegation information distribution mechanism.  This document should include operational and deployment considerations.
This is expected to documented within a standards-track RFC.

- A specification for how to use the new delegation information to perform aliasing of delegation information.
This is expected to documented within a standards-track RFC.

- A specification for facilitating the use of additional transports for DNS.
This is expected to documented within a standards-track RFC.

