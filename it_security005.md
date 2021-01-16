
## Sytems Hardening 

### defense in Depth

The concept of having multiple .overlaping systems of defense to protect IT systems

#### Disabling unecessary componets 

Attack ventors:

    a method/mechanism in which an attacker or malware gains access to a system or network

    email attachments, user inputs, net protocols/services/interfaces

attack surfaces:

    sum of all the different attack vectors in a given system

disable unscessary components to resduce attack surfaces.

Reduce software deployments (have a unified solutions)

Deploy many security walls


#### Host-based firewalls

Protect individual hosts from being compromised when they're used in untrusted ,  potentially malicious environments

also protect inside trusted network compromise

only allows traffic to specific roles and tasks

Bastion Host/Networks:

    Deployed on the internet to reduce system compromise

    have limted network connectivity

VPNs can also be used to protect againest remote attackers in a network

AD in windows can be used to monitor and log for firewalls compromise by system admins 



#### Logging and Auditing:

Have logging servers on large companies and log systems fro small companies

SIEM(Security Information and Event Management):

    Centralized log server

    has anlysis feature

formalization

    process of taking log data in different format and converting it to standardized formart with log structure

log data to and from clients and timestamp to be sure when  the event occured

pay attention to patterns and traffic moving in your systems during analysis 

logging servers:

    rsylog (open source)
    Splunk Enterprise Security
    IBM Security Qradar
    RSA security analytics


#### loging and auditing suplimentary reading

[rsylog open sourced](https://github.com/rsyslog/rsyslog)

[Splunk Enterprise Security](https://www.splunk.com/)

[IBM Security Qradar](https://www.ibm.com/security/security-intelligence/qradar)

[RSA Security analytics](https://community.rsa.com/docs/DOC-41639)



#### Antimalware protection

Antivirus to protect on systems

    operates on known signatures for new files or downloads and blocks the malware from harming the system

Not trustable because its vendor invent and sign which could be too late for attacks

binary white listing software

    only permits s/w in the list to run alone

    for only executable binary files

uses crytographic hash binaries -> identify unique binary

software signing certificate: -> sign binary distrubuted by private vendors

#### Antimalware protection reading

[compromising unprotected systems](https://isc.sans.edu/survivaltime.html)

[Antivirus in question by securty engineers](http://robert.ocallahan.org/2017/01/disable-your-antivirus-software-except.html)

[Sophos Antivirus system attack](http://lock.cmpxchg8b.com/Sophail.pdf)

[Hackers bypassing whitelisting attacks](http://www.crn.com/news/security/240148192/bit9-admits-systems-breach-stolen-code-signing-certificates.htm)


#### Disk Encryption

FDE:(Full Disk Encryption):
    
    converting data on hardware into a form that cannot be understood by anyone without the key to undo conversion

Bootloader and Kernel: -> helps boot and FDE Disk

secure boot:

    uses public Key cryptography to secure booting process from attackers

first-party encryption solution:

    Bit Locker -microsoft
    FileVault2 - apple

third-party

    dm-encrypt package (linux)
    PGP
    TrueCrypt
    VeraCrypt

key Escrow:

    securely storing encryption keys by third party for later retreival when needed


#### Disk Encryption reading

[Bitlocker by Microsoft](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-overview)

[FileVault by Apple](https://support.apple.com/en-us/HT204837)

[Linux dm-encrypt](https://wiki.archlinux.org/index.php/dm-crypt)

[PGP](https://www.symantec.com/products/encryption)

[TrueCrypt](http://truecrypt.sourceforge.net/)

[VeraCrypt](https://www.veracrypt.fr/en/Home.html)



#### Software Patch Management

Softwae should always be uptodate 

the sending and receiving ends must have eqaul checksum for communication

Open SSL was compromised in 2014 with different heartbeats memory

have a system to check vulnarabilities on a system before installing software

used managment tools to verify:

    Microsoft SCCM
    Puppet Labs

#### Application policies

have policy on s/w to be used and secure the system by educating the team

have the latest software working only

makes sure we have the latest security features in place

Extension on web must be well monitored as it could send user inputs to a remote server for credentials
