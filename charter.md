# Background and Problem Space

The DNS protocol has traditionally had limited ability to signal to recursive resolvers about the capabilities of authoritative servers they communicate with.
In part, this stems from the inability of parents (often registries) to specify additional information about child delegations (often registrants) beyond NS, DS, and glue records.
Further complicating matters is the inability of a registrant to signal that the operation of a delegation point is being outsourced to a different operator, leaving a challenge when operators need to update parental information that is only in the control of the child.
A significant issue in today's deployed DNS that derives from these issues is data often being out of synchronization between parents and children. Said another way, children often have more up-to-date information about the nameservers and DNSSEC keying information than their parents due to slowness, or complete lack, of automated child-to-parent updates.

The Internet's dependence on the DNS as a critical starting point for most communication has resulted in the development of a complex ecosystem that consists of many different parties, business relationships, and software packages.
Software deployments exist in environments that range from small CPE devices and software packages to entire clusters of world-wide distributed server platforms.

# Objective and Scope

To address these challenges, the working group will first develop the requirements for adding a new signaling mechanism that allows parents to return DNS delegation information to resolvers.

The working group will also list the other types of information not available today that might be provided over a designed signaling mechanism.

The working group will then define the semantics of a new signaling mechanism, taking future extensibility into account.

The first use case for this DNS delegation signaling mechanism is expected to be delegation aliasing, where the parent returns a pointer to the service provider that will then return the needed delegation information.
This use case has been discussed for many years in the DNSOP and other working groups.

The working group will only specify extensions to the DNS protocol that relate to delegation.

# Deliverables

- A document listing the consensus-derived requirements for a new signaling mechanism between a parent and a resolver about communication parameters available for communicating with a delegated child.
This need not be published as an RFC and may remain as an Internet-draft.

- A document listing, and ideally prioritizing, new delegation attributes to be distributed from parents that would benefit resolver and child communications.
This need not be published as an RFC and may remain as an Internet-draft.

- A specification defining the new delegation attribute signaling mechanism.
This is expected to become a standards-track RFC.

- A specification for how to use the new delegation attribute signaling mechanism to perform aliasing for delegation.
This is expected to become a standards-track RFC.

