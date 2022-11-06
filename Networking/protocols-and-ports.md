# Protocols and Ports

## Voice and video
- RTP - Realtime Transport Protocol
- VoIP - Voice over the Internet. VoIP logs contain timestamps, phonenumbers, extensions, missed calls, etc.
- SRTP - Secure RTP
- SIP - Session initialization Protocol. Uses request and repsonse messages. SIP logs include timestamps, addresses, etc.

## File Transfer
- FTP -21(C)20(D)- File transfer protocol. By default is in cleartext. Used to download files from an FTP server
- TFTP -UDP 69- Trivial FTP (smaller files)

## Encryption protocols for data in transit
- SSH-22-Secure Shell - encryption of data in transit
- SCP-22- Secure Copy, based on SSH. Used to copy encrypted files through network
- SSL - Secure Socket Layer - HTTP -> HTTPS. Also encrypts SMTP. Is compromised.
- TLS -443- Transport Layer Security - replacement for SSL
- IPSec - encrypts IP traffic. Native to IPv6. Internet key exchange through port 500 to create security association with VPN
- SFTP -22- SSH in FTP. 
- FTPS -989,990- extension to FTP uses TLS. Also can encrypt FTP 20,21

## EMAIL and WEB
- SMTP -25/587_with_TLS- Simple Mail Transfer Protocol
- (S)POP3 -101- Post office protocol. SPOP -995- encrypted
- (S)IMAP4 -143/993_encrypted- Internet Messaging Access Protocol. Allows to store emails on server, organaize them in folders.
- HTTP - 80 - Hyper Text Transfer Protocol
- HTTPS - 443 - HTTP using TLS
- LDAP(S) - 389/636_encrypted -Light weight directory access protocol

## Remote Access
- RDP -tcp/udp 3389- Remote Desktop protocol. Microsoft proprietary protocol
- OpenSSH -22- suite of tools - supports SCP and SFTP.

## Time Synchronization
- NTP -123- Network Time Protocol
- SNTP -udp123- Simple Network Time Protocol

