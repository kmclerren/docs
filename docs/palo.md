# Palo Alto Firewalls

BGP related CLI commands

    less mp-log routed.log
    tail follow yes mp-log routed.log

Group mapping related CLI commands

    show user group list
    show user group name "cn=it_operations,cn=users,dc=al,dc=com"

GlobalProtect Cookie and Config file locations (dat files - see: https://thewayeye.net/posts/globalprotect-remove-cookies/)

Windows

    %AppData%\..\Local\Palo Alto Networks\GlobalProtect

Windows log files

    C:\Program Files\Palo Alto Networks\GlobalProtect

MacOS

    /Users/$USER/Library/Application Support/PaloAltoNetworks/GlobalProtect/
    /Library/Application Support/PaloAltoNetworks/GlobalProtect/


Related links

* https://thewayeye.net/posts/globalprotect-remove-cookies/
* https://docs.paloaltonetworks.com/pan-os/9-1/pan-os-admin/user-id/map-users-to-groups
* https://knowledgebase.paloaltonetworks.com/kcSArticleDetail?id=kA10g0000008U8e

