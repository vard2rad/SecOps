# Description
This workflow runs a query that pulls remote public IP addresses and checks them against AbuseIPDB and the total number of login attempts. Based on these results, the workflow then automatically adds the IP address as an indicator in Microsoft Defender for Endpoint.

# Key Features
* Runs automatically to scan for new login attempts based on frequency set
* Uses workflow parameters to establish a threshold for automatically adding IPs found as an indicator
* If the above parameters aren't met, then the workflow will trigger a Human decision allowing user(s) to manually initiate the indicator addition

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
### Abuse Confidence Threshold
This sets the minimum required "Confidence of Abuse" value for InsightConnect to automatically flag the indicator as malicious. If the returned confidence value is greater than this parameter, the workflow will follow the automated approach to blacklisting/blocking this indicator.

## Usage

## Technical Details

## Troubleshooting

# Version History

# Links
* [GitHub InsightConnect/RemoteIPLoginAttempts](https://github.com/vard2rad/SecOps/tree/main/InsightConnect/RemoteIPLoginAttempts)
* [AbuseIPDB FAQ](https://www.abuseipdb.com/faq.html)

## References