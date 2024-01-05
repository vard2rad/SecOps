## Indicator Updated in Microsoft Defender
An existing indicator in Microsoft Defender for Endpoints was updated. Details of the finding are listed below.
### {{["loop-indicator_response"].[$item]}}
**Indicator Type:** ipaddress \
**domain:** {{["IR-abuseipdb-ip_lookup"].[domain]}} \
**countryName:** {{["IR-abuseipdb-ip_lookup"].[countryName]}} \
**isp:** {{["IR-abuseipdb-ip_lookup"].[isp]}} \ 


### AbuseIPDB Score
**AbuseConfidenceScore:** {{["IR-abuseipdb-ip_lookup"].[abuseConfidenceScore]}} \ 
**lastreportedAt:** {{["IR-abuseipdb-ip_lookup"].[lastReportedAt]}} \

### New Indicator Information
**creationTimeDateTime:** {{["IR-atp-blacklist_indicator"].[indicator_action_response].[creationTimeDateTimeUtc]}} \
**lastUpdateTime:** {{["IR-atp-blacklist_indicator"].[indicator_action_response].[lastUpdateTime]}} \
**expirationTime:** {{["IR-atp-blacklist_indicator"].[indicator_action_response].[expirationTime]}}