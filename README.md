# Role Name:
- ansible-role-compliance-windows-system-policy-2019

# Description:
This System Policy Role was based off the CIS specs for 2019 servers.   This
role covers the "System" CIS section only. The checks and remediation commands
are for local settings only. Group Policy settings may override these settings.
When the "remediate" variable is set to "YES", the role will try to remediate
the server's setting(s) accoridng to the CIS standards.  The defaults/main.yml
file can be used to disable specific CIS items (i.e. "execute_<cis task #>")
from executing. The default value in the defaults/main.yml for these CIS item
variables (i.e. "execute_<cis task #>") is set to "YES". The value "YES" means
that the CIS item will execute at run time. Set the value to "NO" if you want
to skip this CIS item in question from executing.

# Windows Ansible related pre-requisites:
Powershell 3.0 and higher for windows
Powershell remote management

# Defaults file for ansible-role-compliance-windows-system-policy-2019:
# Variables

Parameter | Choices/Defaults|Comments
----------|-----------------|--------
__remediate__ |"NO"| varaible to determine whether or not to remediate non-compliant settings.
__ProcessCreationIncludeCmdLine_Enabled_cis__ |"1"| CIS value.
__DriverLoadPolicy_cis__ |["1","3","8"]| CIS value.
__NoBackgroundPolicy_cis__ |"0"| CIS value.
__NoGPOListChanges_cis__ |"0"| CIS value.
__EnableCdp_cis__ |"0"| CIS value.
__DisableBkGndGroupPolicy_cis__ |"0"| CIS value.
__NoUseStoreOpenWith_cis__ |"1"| CIS value.
__DisableWebPnPDownload_cis__ |"1"| CIS value.
__PreventHandwritingDataSharing_cis__ |"1"| CIS value.
__PreventHandwritingErrorReports_cis__ |"1"| CIS value.
__ExitOnMSICW_cis__ |"1"| CIS value.
__NoWebServices_cis__ |"1"| CIS value.
__DisableHTTPPrinting_cis__ |"1"| CIS value.
__NoRegistration_cis__ |"1"| CIS value.
__DisableContentFileUpdates_cis__ |"1"| CIS value.
__NoOnlinePrintsWizard_cis__ |"1"| CIS value.
__NoPublishingWizard_cis__ |"1"| CIS value.
__CEIP_cis__|"2"| CIS value.
__CEIPEnable_cis__ |"0"| CIS value.
__Disabled_cis__ |"1"| CIS value.
__DevicePKInitBehavior_cis__ |"1"| CIS value.
__DevicePKInitEnabled_cis__ |"1"| CIS value.
__BlockUserInputMethodsForSignIn_cis__ |"1"| CIS value.
__BlockUserFromShowingAccountDetailsOnSignin_cis__ |"1"| CIS value.
__DontDisplayNetworkSelectionUI_cis__ |"1"| CIS value.
__DontEnumerateConnectedUsers_cis__ |"1"| CIS value.
__EnumerateLocalUsers_cis__ |"0"| CIS value.
__DisableLockScreenAppNotifications_cis__ |"1"| CIS value.
__AllowDomainPINLogon_cis__ |"0"| CIS value.
__MitigationOptions_FontBocking_cis__ |"1000000000000"| CIS value.
__DCSettingIndex_cis__ |"1"| CIS value.
__ACSettingIndex_cis__ |"1"| CIS value.
__DCSettingIndex2_cis__ |"1"| CIS value.
__ACSettingIndex2_cis__ |"1"| CIS value.
__fAllowUnsolicited_cis__ |"0"| CIS value.
__fAllowToGetHelp_cis__ |"0"| CIS value.
__EnableAuthEpResolution_cis__ |"1"| CIS value.
__RestrictRemoteClients_cis__ |"1"| CIS value.
__DisableQueryRemoteServer_cis__ |"0"| CIS value.
__ScenarioExecutionEnabled_cis__ |"0"| CIS value.
__DisabledByGroupPolicy_cis__ |"1"| CIS value.
__Enabled_cis__ |"1"| CIS value.
__Enabled2_cis__ |"0"| CIS value.
__NoImplicitFeedback_cis__ |"1"| CIS value.

# Example Playbook:
---
 - hosts: [win]
   roles:
   - ansible-role-compliance-windows-system-policy-2019


# Author Information:
Richard M. Williams (williamsitv@yahoo.com)
