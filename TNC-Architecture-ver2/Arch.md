## TNC 
 - providing orchestration of network and security system and interoperatibility
 - providing End point visibility helping network managers(knowing who and what is on their network)
 - providing network-based access control enforcement(access based on authentication granting or blocking)
 - providing security automation(NAC and interoperabililty in multi-vendor environments)
 - TNC mechanisms enable expression of that trust to a third party or back-end verifier, increasing confidence both in
   endpoint evaluation and in resulting actions such as access control decisions

## International standardization efforts
 - GlobalPlatform : general scheme of root of trust, TEE(Trusted Execution Environment) and collaboration with TCG
 - TCG(Trusted Computing Group) : TPM for IoT
 - OneM2M and GSMA for remote management of secure module by applying GlobalPlatfrom scheme etc

## TCG TNC and TCG TPM
 - The Trusted Computing Gruop(TCG), an international not-for-profit organization that develops, defines, and promotes
   open, vendor-neutral specifications for interoperable trusted computing platform 


## TNC and IETF
 - IETF NEA working gruop published several RFCs based on TNC client-server protocols
   * https://datatracker.ietf.org/doc/rfc5792/
   * https://datatracker.ietf.org/doc/rfc5793/
   * https://datatracker.ietf.org/doc/rfc5209/

## Four important concepts for securing mobile devices
 - Mobile Root of Trust(RoT)
   * performing one or moer security specific functions, such as measurement, storage, reporting, verification, update
 - Secure Boot
   * Process in which every software image is validated before execution
 - Measured BOOT
   * What TPM securely stroes and protects the measurements
 - Protected environment
   * Functional Element that has execution and memory resources that are isolated from other components
   in order to host sensitive application that require security and privacy properties 

## Three distinct security areas
 - Compliance
   * evaluating an endpoint's adherence to network policy both at the time of connection and on an ongoing basis while
   it is connected to network
 - Orchestration
   * providing a dynamic repository and notification service for real-time state and events
 - Access Control
   * managing the use of protected resource and network based on endpoint posture and other factors

## use case
 - Device health reporting in mobile networks
   * When a mobile device connects to a cellular base station, the base station establishes a device-specific Security
   Context for that mobile device. The Security Context identifies and tracks security characteristics of mobile device
   that is connected to mobile network. This Security Context is transferred to a new base station every time there
   is a handoff
    Currently, the information in the Security Context is limited to descriptions of the mobile platform of the device,
   with no useful health reporting. as such, this Security Context is of little use for determining whether the device
   is compromised or at risk of compromise. The ability to support more detailed health assessment of mobile devices,
   similar to what is common today on traditional workstations, would be a powerful tool for tracking and managing
   unhealthy mobile device

## IF-MAP
 - providing open spec including the Interface to a Metadata Access Point(IF-MAP) for enterprise security
   * IF-MAP provides a standard way for information security products to share and respond to information about a
     security-realated topics and events

