
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
