## What TNC architecture provide
 - The aim of the TNC architecture is to provide a framework for the development of standards to support multi-vendor
   solutions
     * Endpoint compliance
     * Control of access to resources
     * Policy enforcement
     * Security automation
     * Threat detection and response

## Benefits of TNC
  - TNC standards have a proven track record(There are many open-source implementations) 
  - TNC standards are widely deployed in real production scenarios(Government, Healthcare, Finance, Retail and
    Education)
  - TNC standards are vendor-neutral
  - TNC standards are flexible
     * supporting a broad range of assessment options(identity, health, behavior, and location; hardware-based &
       software-based security; and pre-admission & post-admission evaluation and monitoring)
     * accommodating rapid change and evolving security landscape
  - TNC standards can and do easily integrate with other standards(ISO 19770-2)

## Capabilities
  - Compliance capability
  - Orchestration capability
  - Access control capability
  - Combining capability
  - Composing the TNC capability

## TNC Elements
  - Function : unitary operation of the TNC arch(logically)
  - Component : implementing one or more functions(usually a piece of software)
  - Interface : a standardized method of communication between components
  - Role : an actor who utilize a particular set of functions with a specific purpose
  - Entity : a device performing one or more roles

## Roles
  - Endpoint : provides posture information to Policy Server and accesses a protected resource
  - PEP(Policy Enforcement Point) : enforces the decisions of the PDP regarding resource access
  - Poicy Server
     * PDP(Policy Decision Point) : performs the decision-making regarding the Endpoint's resource access request
       The PDP compares the Endpoint's credentials(e.g. user certificate, password, etc.) and information about
       its posture against configured network access policies
     * CEP(Compliance Evaluation Point) : collects and evaluates endpoint posture information, and to send
       the information to a CMDB for storage
  - CMDB(Configuration Management Database) : stores endpoint posture information and make it available to consumers
    of such information
  - CMDBC(CMDB Client) : shares and consumes endpoint posture information
  - MAP(Metadata Access Point) : stores and provides state information about end points, resource, and the environment
    This information may include, but is not limited to, device bindings, user bindings, registered address bindings,
    authentication status, endpoint compliance status, endpoint behavior, and authorization status
  - MAPC(MAP Client) : publishes to, or consume from, the state information in the MAP

## Functions (usually implementing as software components running on the Endpoint)
  - Endpoint Functions
     * IMCs(Integrity Measurement Collectors) : measures specific aspects of the Endpoint's posture
       Example measurements could include the anti-virus parameters on the Endpoint, personal firewall status, software
       and operating system versions, patch levels, configuration, and other provisioning and security aspects of the
       Endpoint.
     * TNCC(TNC Client) : receives requests and instructions from a TNC Server, sends them to the appropriate IMCs
       combines posture measurements from IMCs into batches and communicates them to a TNCS
     * TPTC(TNC Posture Transport Client) : facilitates network communication to a TNC Posture Transport Server
     * NAR(Network Access Requestor) : establishes network access by negotiating an Endpoint's connection to a network
       Examples are aupplicant in 802.1X or the VPN client in IPsec
  - CEP Functions
     * IMVs(Integrity Measurement Verifiers) : compares a particular aspect of the Endpoint's posture against policy
       based on measurements received from IMCs or other data, and returns an IMV Action Recommendation.
     * TNCS(TNC Server) : collects requests and instructions from IMVs, communicates them to a TNCC,
       receives batches of measurements from the TNCC, distributes the measurements to the appropriate IMVs,
       gathers IMV Action Recommendations from IMVs
     * TPTS(TNC Posture Transport Server) : faciliates network communication to a TPTC
     * One primary distinction between a CEP and a PDP is that the PDP has a Network Access Authority and performs
       enforcement functions
  - CMDB and CMDB Client Functions
     * No TNC-spec functions are currently defined for theses roles
  - PEP Functions
     * NAE(Network Access Enforcer) : controls access to a protected network
       The NAE consults an NAA to determine whether this access should be granted
  - PEP Functions
     * IMVs, TNCS, TPTS
     * NAA(Network Access Authority) decides whether an Endpoint should be granted access
       The NAA consults a TNC Server to determine whether the Endpoint's posture complies with the PDP's
       security policy
  - MAP Functions
     * MAPS(Metadata Access Point Server) : allows elements which do not have a direct relationship to endpoints, users,
       capabilities, roles, device activities, and postures as well as other run time data

## See also
  - https://trustedcomputinggroup.org/wp-content/uploads/TCG-TNC-Architecture-for-Interoperability-Version-2.0-Revision-13-.pdf
  - https://trustedcomputinggroup.org/work-groups/trusted-network-communications/open-standards-tnc/



