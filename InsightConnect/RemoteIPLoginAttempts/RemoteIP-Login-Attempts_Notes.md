# Description
This workflow runs a query that pulls remote public IP addresses and checks them against AbuseIPDB and the total number of login attempts. Based on these results, the workflow then automatically adds the IP address as an indicator in Microsoft Defender for Endpoint.

# Key Features
* Runs automatically to scan for new login attempts based on frequency set
* Uses workflow parameters to establish a threshold for automatically adding IPs found as an indicator
* If the above parameters aren't met, then the workflow will trigger a Human decision allowing user(s) to manually initiate the indicator addition

# Requirements
* Microsoft Office 365 Email
* Microsoft Windows Defender ATP
* AbuseIPDB API
* Global Artifact ("Blocked IP Addresses")
* Microsoft Defender Hunting



# Documentation

## Setup

### Parameter Details

## Usage

## Technical Details

## Troubleshooting

# Version History

# Links
[GitHub InsightConnect/RemoteIPLoginAttempts](https://github.com/vard2rad/SecOps/tree/main/InsightConnect/RemoteIPLoginAttempts)

## References