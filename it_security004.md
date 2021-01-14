
## Securing Your Network

#### Network Hardening Best practices

The process of securing your network by reducing its potential vulnerabilities through configuration changes and taking specific steps

#### Implicit deny

    A network security concept where anything not explicitly permitted or allowed should be denied

Monitoring networks:

    Make sure you understand your traffic

Analyse logs:

    The practice of collecting logs from different network & clients devices on your network and then doing analysis on them

    logs: (authentication logs, server logs & application logs)

    log analysis-> configured with user-defined rules to match interesting entries

Corelation analysis:-> The process of taking log data from different systems and matching events across the system

post fail analysis->Investigating hoe a compromise happened after a breach is detected

Splunk:

    Log analysis system popular used

Flood guards:

    Provide protection againest Dos (Denial of Service Attacks)

failed to ban:

    flood guard open sourced for small org

[Cisco IOS firewall rules](https://www.cisco.com/en/US/docs/routers/access/800/850/software/configuration/guide/firewall.html)

[Juniper Firewall rules](https://www.juniper.net/documentation/en_US/junos/topics/usage-guidelines/services-configuring-stateful-firewall-rules.html)

[Iptables firewall rules](https://www.digitalocean.com/community/tutorials/iptables-essentials-common-firewall-rules-and-commands)

[UFW firewall rules](https://www.digitalocean.com/community/tutorials/ufw-essentials-common-firewall-rules-and-commands)

[Configuring MaCOS firewall](https://support.apple.com/en-us/HT201642)

[Microsoft firewall rules](https://technet.microsoft.com/en-us/library/cc754274(v=ws.11).aspx)


#### Network HardwareHardening

#### Network HardwareHardening

DHCP:

    Protocol where devices on a network are assigned critical configuration information for communication over a network

rougue DHCP server attck:

    hackers controling DHCP server for attacks

DHCP snooping:

    Monitor DHCP traffic being sent over a network and track IP assingment and maps them to address being sent over a network

    Can also be used to prevent againest IP Snoofing and ARP attacks

Dynamic ARP inspection

    Allows the nature of the men-in-the-middle attack:

a gratuitous ARP Response:

    answers query that no one made. prevent data manipulation and ip forwading of data

Dynamic ARP inspection(DAI):

    prevent DHCP attacks and DHCP snoofing

    Detects forged ARP and drops them

    precents ARP scanning by having limited set of IP addresses per transfer

IP Source Guard (IPSG)
    
    prevents ip spoofing attacks

802.1X

    locking down a network

    IEEE standards for encapsulating EAP - Extensible Authentication Protocol Traffic

    EAP over LAN

Parties involved when Authenticating 802.1X

    Supplicant-->The client device

    Linux wpa_supplicant (client communication which acts as gate keeper)

EAP-TLS

    Authenticaiton type supportted by EAP that uses TLS to authenticate both client and Authentication server

TPMS and FDE

    provide more security to the systwm

#### IEEE 802.1X

[More on IEE 802.X1](https://en.wikipedia.org/wiki/IEEE_802.1X)


### Network software Hardening:

covers

    Firewalls
    VPS
    Proxies

Host-based Firewall:

    Provide security for mobile Devices and other devices from being corrupted over a network

Network-based Firewalls;

    VPNs to provide secure remote access to link to networks seccurely

Procies:

    usesful to protect clients device and their traffic and remote access without using a VPN
    Can be used to block maliciour content from accessing company's data
    Reverse proxy allows secure remote Access

Proxy solutions:

    HAProxy
    Nginix
    Apache web server

#### Reading on Proxy

[HAProxy Main Documentation](http://www.haproxy.org/#docs)

[HAProxy Reverse documentation](http://cbonte.github.io/haproxy-dconv/1.8/intro.html#3.3.1)

[Nginx documentation](http://nginx.org/en/docs/)

[Nginx Reverse Documentation](http://nginx.org/en/docs/beginners_guide.html#proxy)

[Apache HTTP server main Documentation](http://httpd.apache.org/docs/)

[Apache HTTP reverse proxy documentation](https://httpd.apache.org/docs/2.4/howto/reverse_proxy.html)


## Wireless Security

#### WEP Encryption

#### Wifi Seccurity Network:

WEP(Wired Equivalent Privacy):

    Wireless infomation protection againest evesdropping

    It uses the RC4 symmetric stream cipher for encryption

IV --> generate random data to be used in the systems without repeating same code

Modes for WEP:

    Open System Authentication - No client requirement to encrypt

    Shared Key Authentication - Four stepn challenge to allow encryption

WEP tools cracker Passwords:

    Aircrack
    AirSnort

[WEP Encryption](https://doi.org/10.1007/3-540-45537-X_1)



### WPA/WPA2

Wifi Protected Access (WPA):

TKIP-(Temprol Key Integrity Protocol)
    
    secure derivation method (IV->Per packet encryption)
    Sequence Counter -> reject repeated packets
    64-bit MIC (Message Integrity Check) to prevent packets corruption

PBKDF2(Password-Based Key Derivation Function 2)

HMAC-SHA1 -> genearate encryption 4096 times 

SSID-> prevent rainbow attacks

4096->increase computational power to prevent brute force attack

WPA2:

    improved WPA by introducing CCMP (Counter Mode CBC-MAC Protocol)

    mode of operation for BLock ciphers

    Authenticate + Encrypt mechanism

Four-way handshake (Client-AP Exchange)

    PMK - used for encryption and decryption key(PTK- Pairwise Transient Key)
        Generating using:
        PMK
        AP nonce
        Client nonce
        AP MAC address
        Client MAC address
    PTk keys:
        2-keys->Encryption and Confirmation EAPol Packects
        2-keys--> sending and receiving message Integrity codes
        temprol key->used to encrypt data
    AP:
        Transmit  GTK(Group Transcient Key)
        Encyrpt multicast and broadcast traffic

Non 802.1X Configurations are called either WPA2-Personal or WPA2-PSK since they use preshared key to auth clinets

Wifi protected setup:

    makes it wasier for clients to join a WPA2 protected network

WPS:
    helps client to join a network without entring a preshared Key

    usses SSID to authenticate

    supports:
        PIN entry
        NFC/ USB out of banned exchange
        push-button authentication
    PIN Modes:
        Client generates Pin entered into AP
        AP has a pin hard-corded into the client

[Wifi Protected Set up WPS Brute Force Vulnurability Attack](https://www.kb.cert.org/vuls/id/723755)

#### Wireless Hardening

use WPA2 with AES/CCMP 

Raise Computational bars

Disable WPS and allow only clients to use it and not server/office 

AP manangment console should be upto date

## Network Monitoring

#### Sniffing Network

Packet Sniffing:
    
    The process of intercepting network packets in their entirety for analysis

Promiscious Mode:

    Computer networking Operational Mode in which all network data packets can be accessed and viewed by all network adaptors operating in this mode

Make sure to have root access and right previlages to access the packets and traffic you want to capture

port mirroring:

    Allows the switch to take all packets from a specified port, port range / entire VLAN and mirror the 
    packets to a specific switch port

    you can also use Hub on the traffic you want ot monitor


Monitor Mode:

    Allows us to scan across channels to see all wireless traffic being sentby APs and Clients

Capture and Monitoring utilities:

    Aircrack-ng
    Kismet


#### Wireshack and tcpdump

Tcpdump:

    light-weight command-line based utility you can use to capture and analyze packets.

    provide brief packet analysis

    -x flag--> view raw data

wireshark:

    powerful packet anylsis and sniffer

    uses libpcap library 

    has a UI for operation

    if a passphrase os known it can dedcode WPA/WEP

    also checks for bluetooth traffic and USB Traffic

    Can unencrypt voices  VOIP traffic

#### Promiscous Mode:
