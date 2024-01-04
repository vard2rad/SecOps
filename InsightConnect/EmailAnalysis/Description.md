# Description

# Key Features
* 
* 
* 

# Requirements
* Microsoft Office 365 Email
* VirusTotal
* WHOIS
* AbuseIPDB
* Cisco ThreatGrid
* Global Artifacts
  * Allowed Domains
  * Allowed URLs

# Documentation

## Setup

## Parameter Definitions
**VirusTotal Domain Threshold:** This threshold governs the risk measurement of VirusTotal reputations. This number NEEDS to be negative, since malicious reputations are indicated with a value less than 0. If the reputation is lower than this parameter, the domain is found to be malicious. If the reputation is higher, then the domain will be low risk (or harmless if it is greater than 0). Example is below.
> Let R = VirusTotal Reputation
> Let P = Parameter
> > If R > 0, domain has no risk
> > If 0 > R > P, domain is low risk
> > If 0 > P > R, domain is high risk

## Usage

## Process Details
### Object Extractions
- Domains are extracted from headers
- URLs are extracted from headers
- URLs are extracted from email body
- Attachments are pulled directly
### Header Domains
1. Domains are checked against the Allowed Domains global object to see if it is excluded. If found, the domain will be skipped.
2. Domain is checked against WHOIS - if successful AND creation_date is defined, then domain is considered valid.
3. Domain age is calculated. If age is less than 30 days, domain is immediately flagged as malicious. Loop stops.
4. If domain age is greater than 30, the domain is then checked against VirusTotal for reputation as the domain report was pulled successfully.

## Troubleshooting

# Version History

# Links

## References