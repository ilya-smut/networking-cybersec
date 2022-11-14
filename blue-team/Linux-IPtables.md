# Linux IPtables

Linux IPtables is a kind of in-built firewall, where rules may be configured

## A way to configure iptables to respond with TCP RST when a port if filtered
    iptables -I INPUT -p tcp --dport <port> -j REJECT --reject-with tcp-reset
