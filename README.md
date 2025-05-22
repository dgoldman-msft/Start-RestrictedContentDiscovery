# Start-RestrictedContentDiscovery
Implement Restricted Content Discovery for SharePoint Sites

## DESCRIPTION

This will set a flag to determine if the SharePoint site is detected in organizational wide searches. Module can use PowerShell 5 and 7 to connect.


## EXAMPLE 1
    C:\PS> Start-RestrictedContentDiscovery -TenantDomain contoso -SiteUrl "https://tenantname.sharepoint.com/sites/Test" -SetRCD

    This will set the flag which controls whether org-wide content search is enabled for the site specified.

## EXAMPLE 2
    C:\PS> Start-RestrictedContentDiscovery -TenantDomain contoso -SiteUrl "https://tenantname.sharepoint.com/sites/Test" -RemoveRCD

    This will remove the flag which controls whether org-wide content search is enabled for the site specified.

## EXAMPLE 3
    C:\PS> rcd -TenantDomain contoso -SiteUrl "https://tenantname.sharepoint.com/sites/Test" -SetRCD

    Call this function with the alias and set the flag which controls whether org-wide content search is enabled for the site specified.

## EXAMPLE 4
    C:\PS> rcd -TenantDomain contoso -SiteUrl "https://tenantname.sharepoint.com/sites/Test" -RemoveRCD

    Call this function with the alias and remove the flag which controls whether org-wide content search is enabled for the site specified.

## EXAMPLE 5
    C:\PS> rcd -TenantDomain contoso -GenerateRCDReport

    Will generate a SharePoint Online Restricted Content Discoverability Report.

## Notes:
    The testing is only at the Org-wide search and in Copilot search without referencing the file.

    1. You must have not accessed any content on that site at least in the last 28 days. RCD is to prevent accidental discovery. "Although RCD is applied at a site basis,
    2. SharePoint indexing happens at the file level, so a fan-out process must find and reindex every file in a site 'before RCD becomes effective for that site'.

    The time required to update the index for a site is highly dependent on the number of items in the site.