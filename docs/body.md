# Body

**Topic**: The "Solarwinds" attack and farm-to-table methods in the development process - Mitigating disasters through supply-chain security

## The SolarWinds Attack

On 13 December 2020, FireEye, a US-based cybersecurity company, detected a large supply chain attack directed at customers of SolarWinds using their Orion monitoring and management solution. The actors of the attack, which are now presumed to be of Russian origin, were able to gain access to data of sever high-profile private and public institutions. While the attack was made apparent by late 2020, it has been running since at least Spring 2020, resulting in widespread lateral movement and data theft.

The backdoor was built into a digitally signed component of the Orion platform (`SolarWinds.Orion.Core.BusinessLayer.dll`) which communicates with external servers using HTTP. After an initial dormant period, the Trojan is able to receive and execute commands such as transferring and executing files, profiling a system, disabling services and issuing reboots from command and control infrastructure; traffic is obfuscated as by masquerading as telemetry communications similar in structure to the Orion Improvement Program. In addition to these obfuscation methods, it is sandbox-aware to evade detection by anti-malware tools and increase the threshold required to do forensics.

In order to deliver the malware to users of SolarWinds Orion, the supply chain was attacked. The attackers were able to compromise SolarWinds' private keys and digitally sign a trojanized version of a Windows Installer Patch file, which was distributed using the existing update infrastructure and, after the update process, was loaded by the host process. Signature checks did not fail due to the private key compromise. Attacks were than able to connect from the malware to command and control infrastructure by resolving a subdomain's CNAME record and designing their API to be similar to the legitimate SolarWinds API.
