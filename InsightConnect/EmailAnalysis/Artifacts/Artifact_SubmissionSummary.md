## {{["Attached Emails Loop"].[$item].[subject]}}
> **From:** {{["Attached Emails Loop"].[$item].[sender]}}
> **To:** {{["Attached Emails Loop"].[$item].[recipients]}}
> **Date** {{["loop-header_analysis"].[Received]}}
> **Has Attachments:** {{["Attached Emails Loop"].[$item].[has_attachments]}}

### Extracted Variables
> **SenderIP:** {{["loop-header_analysis"].[Sender-IP]}}
> **Network-Message-IP:** {{["loop-header_analysis"].[Network-Message-ID]}}
> **Header Domains:** {{["uniq-header_domains"].[element_count]}}
> **Body URLs:** {{["uniq-body_urls"].[element_count]}}
