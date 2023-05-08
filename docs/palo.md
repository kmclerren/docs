# Palo Alto Firewalls

BGP related CLI commands

    less mp-log routed.log
    tail follow yes mp-log routed.log

Group mapping related CLI commands

    show user group list
    show user group name "cn=it_operations,cn=users,dc=al,dc=com"
    debug user-id refresh group-mapping all (force cache refresh)
    show user user-attributes user all
    show user ip-user-mapping all
    

GlobalProtect Cookie and Config file locations (dat files - see: https://thewayeye.net/posts/globalprotect-remove-cookies/)

Windows

    %AppData%\..\Local\Palo Alto Networks\GlobalProtect

Windows log files

    C:\Program Files\Palo Alto Networks\GlobalProtect

MacOS

    /Users/$USER/Library/Application Support/PaloAltoNetworks/GlobalProtect/
    /Library/Application Support/PaloAltoNetworks/GlobalProtect/


ECMP

Symmetric return in ECMP

* Select Symmetric Return to cause return packets to egress out the same interface on which the associated ingress packets arrived. That is, the firewall will use the ingress interface on which to send return packets, rather than use the ECMP interface, so the Symmetric Return setting overrides load balancing. This behavior occurs only for traffic flows from the server to the client.

* "Strict source path" means no ECMP. It applies to firewall originated IKE/IPsec traffic. Traffic will be sent out over the tunnel based on which tunnel the source address belong to. It has nothing to do with real "source routing". It does not affect transit traffic. Similar to "symetric return" it is an exception of ECMP hashing.


Related links

* https://thewayeye.net/posts/globalprotect-remove-cookies/
* https://docs.paloaltonetworks.com/pan-os/9-1/pan-os-admin/user-id/map-users-to-groups
* https://knowledgebase.paloaltonetworks.com/kcSArticleDetail?id=kA10g0000008U8e

