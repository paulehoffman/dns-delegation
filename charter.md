# Background and Problem Space

The DNS protocol has traditionally had limited ability to signal recursive resolvers about the capabilities of authoritative servers they communicate with.
In part, this stems comes from the inability of parents (often registries) to specify additional information about child delegations (often registrants) beyond NS, DS, and glue records.
Further complicating matters is the inability of a registrant to signal that the operation of a delegation point is being outsourced to a different operator, leaving a challenge when operators need to update parental information that is only in the control of the child.
A significant issue in today's deployed DNS that results from these issues is that data is often woefully out of synchronization between parents and children.

The Internet's dependence on the DNS as a critical starting point for most communication has resulted in the development of a complex ecosystem that consists of many different parties, business relationships, and software packages.
Software deployments exist in environments that range from small CPE devices and software packages to entire clusters of world-wide distributed server platforms.

# Objective

To address these challenges, the DELEG working group will first research the requirements for adding a new signaling mechanism for parents to pass to resolvers at delegation points about the children.
To be successful in development requirements that ensure wide spread deployment of a solution for this space is possible, it is critical that viewpoints from the entire DNS ecosystem are collected.

Also to be researched is what types of information need to be provided over a designed signaling mechanism.  Given today's deployed DNS infrastructure, what additional information could a resolver use when a parent provides delegation information about a child?

# Scope

The working group is expected to first study the problem space carefully with an eye toward solutions that maximize deployment and interoperability.

A solution to the problem space can then be developed that is modular in form so as to be extensible when future extensions and attributes are needed, avoiding the ossification that we have with today's DNS delegation records.

# Deliverables

- A document listing the consensus derived requirements for a new signaling mechanism between a parent and a resolver about parameters for communicating with a delegated child.
This need not be published as an RFC and may remain as an internet-draft.

- A document listing, and ideally prioritizing, new delegation attributes to be distributed from parents that would benefit resolver and child communications.
This need not be published as an RFC and may remain as an internet-draft.

- A specification defining the new delegation attribute signaling mechanism.

- A minimal set of initial specifications of attributes to be used within the new attribute signaling mechanism.

