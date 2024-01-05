# Description
This workflow runs a query that pulls remote public IP addresses and checks them against AbuseIPDB and the total number of login attempts. Based on these results, the workflow then automatically adds the IP address as an indicator in Microsoft Defender for Endpoint. \
The workflow will send an email to recipients indicated in workflow parameters if the indicator is **new**. If the indicator is a repeat, only an artifact will be created.
> Please note that throughout this workflow the terms "ip address" and "indicator" may be used interchangeably. This is only to make the workflow adaptable in the event further indicators are added.

# Key Features
* Runs automatically to scan for new login attempts based on frequency set
* Uses workflow parameters to establish a threshold for automatically adding IPs found as an indicator
* If the above parameters aren't met, then the workflow will trigger a Human decision allowing user(s) to manually  initiate the indicator addition
* If a new indicator is created, an email is sent. If it is a repeat indicator, an artifact is created.

# Setup
## Required Plugins
* Microsoft Office 365 Email
* Microsoft Windows Defender ATP
* AbuseIPDB API
* Global Artifacts (match names **exactly**):
  * Blocked IP Addresses
  * Allowed IP Addresses
* Microsoft Defender Hunting

## Parameter Details
### Email Sender
This is a valid email address that InsightConnect would be able to send from. Will be used as the "from" address when sending the email.

### Email Recipient
Recipient email address(es) of user(s) who should receive the email informing of a new indicator being added to Microsoft Defender.

### Abuse Confidence Threshold
This sets the minimum required "Confidence of Abuse" value for InsightConnect to automatically flag the indicator as malicious. If the returned confidence value is greater than this parameter, the workflow will follow the automated approach to blacklisting/blocking this indicator.

### Login Attempt Threshold
If the number of login attempts from a single IP address, over the time between workflow runs, is greater than the login attempt threshold value indicated then the indicator is added automatically without human interaction.

# Technical Details

## Version History
v1.0 - Original Version

# Links
* [GitHub InsightConnect/RemoteIPLoginAttempts](https://github.com/vard2rad/SecOps/tree/main/InsightConnect/RemoteIPLoginAttempts)
* [AbuseIPDB FAQ](https://www.abuseipdb.com/faq.html)

## References
* Created by [vard2rad](https://discuss.rapid7.com/u/vard2rad)