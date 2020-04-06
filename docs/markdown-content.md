## Overview

Our customers entrust us with their data, and we take this responsibilty very seriously. Keeping our customers' data protected at all times is our highest priority. Here is an overview of the security best practices we follow. 

Have questions or feedback? Feel free to reach out to us at security@cursive.io(mailto:security@cursive.io)

## Infrastructure

All of our hosted services run in the cloud. Customers may also wish, upon request, to run our services on-premises or in their cloud environments.

We do not host or run our own routers, load balancers, DNS servers, or physical servers.  We use Amazon Web Services (AWS) and have no physical infrastructure or physical access to the servers themselves. Our production databases are on Amazon RDS and S3. AWS provides strong security measures to protect our infrastructure and are compliant with most certifications. You can read more about their practices here (https://aws.amazon.com/security/).

## Network level security monitoring and protection

<!--- __Explanation:__ This section describes the tools in place to monitor and/or protect your network. Isolating networks and restricting accesses to internal services with assigned private IP addresses are security best practices you should follow as soon as possible. --->

Our network security architecture consists of multiple security zones. We monitor and protect our network, to make sure no unauthorized access is performed using:
- A virtual private cloud (VPC), a bastion host or VPN with network access control lists (ACL’s) and no public IP addresses.
- A firewall that monitors and controls incoming and outgoing network traffic.
- An Intrusion Detection and/or Prevention technologies (IDS/IPS) solution that monitors and blocks potential malicious packets.
- IP address filtering

## Data encryption

<!--- __Explanation:__ This part explains the encryption strategy at rest and in transit. There is no good reason not to do data encryption from day one. From data in transit (check your website with [SSLLabs](https://www.ssllabs.com) to encryption at rest ([in a database](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html) or on your machine’s hard drives). To secure your user's passwords, you should either use [one-way encryption on salted passwords](https://blogs.dropbox.com/tech/2016/09/how-dropbox-securely-stores-your-passwords/) or use [bcrypt](https://en.wikipedia.org/wiki/Bcrypt). --->

Encryption in transit: All data sent to or from our infrastructure is encrypted in transit via industry best-practices using Transport Layer Security (TLS). You can see our SSLLabs report here(https://www.ssllabs.com/ssltest/analyze.html?d=cursive.io)

Encryption at rest: All of our user data (and backups) is encrypted using AES-256 key encryption.

## Data retention and removal

Users may request to have their data deleted at any time by writing to support@cursive.io. Please allow 30 days to process your request.

## Business continuity and disaster recovery

We back up all our critical assets and regularly attempt to restore the backup to guarantee a fast recovery in case of disaster. All our backups are encrypted.

## Secure development

We develop following security best practices and frameworks (OWASP Top 10, SANS Top 25). We use the following best practices to ensure the highest level of security in our software:
- We review our code for security vulnerabilities
- We regularly update our dependencies and make sure none of them has known vulnerabilities
- We use Static Application Security Testing (SAST) to detect basic security vulnerabilities in our codebase
- We use Dynamic Application Security Testing (DAST) to scan our applications
- We rely on yearly third-party security experts to perform penetration tests of our applications.

## Responsible disclosure

We encourage everyone that practices responsible disclosure and complies with our policies and terms of service to participate in our bug bounty program.

Please avoid automated testing and only perform security testing with your own data. Please do not disclose any information regarding the vulnerabilities until we fix them. 

You can report vulnerabilities by contacting security@cursive.io(mailto:security@cursive.io). Please include a proof of concept. We will respond as quickly as possible to your submission and won’t take legal actions if you follow the rules.

**Coverage**
- *.cursive.io

**Exclusions**
- status.cursive.io
- support.cursive.io

**Accepted vulnerabilities are the following:**
- Cross-Site Scripting (XSS)
- Open redirect
- Cross-site Request Forgery (CSRF)
- Command/File/URL inclusion
- Authentication issues
- Code execution
- Code or database injections

**This program does NOT include:**
- Logout CSRF
- Account/email enumerations
- Denial of Service (DoS)
- Attacks that could harm the reliability/integrity of our business
- Spam attacks
- Clickjacking on pages without authentication and/or sensitive state changes
- Mixed content warnings
- Lack of DNSSEC
- Content spoofing / text injection
- Timing attacks
- Social engineering
- Phishing
- Insecure cookies for non-sensitive cookies or 3rd party cookies
- Vulnerabilities requiring exceedingly unlikely user interaction
- Exploits that require physical access to a user's machine

## User protection

**2-factor authentication**

We provide a 2-factor authentication mechanism to protect our users from account takeover attacks. Setting up this extra security measure is optional but highly recommended to increase the security of sensitive data.

**Account takeover protection**

We protect our users against data breaches by monitoring and blocking brute force attacks.

**Single sign-on**

Single sign-on (SSO) is offered for our enterprise customers.

**Role-based access control**

Role-based access control (RBAC) is offered on enterprise accounts.

## Compliance

**HIPAA**

We offer HIPAA BAA agreements to enterprise companies that need to comply with HIPAA regulations.

**SOC2**

Our company is engaging with an independent auditor to receive our SOC 2 Type 2(https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/aicpasoc2report.html) certification.  This certification means that an independent auditor has evaluated our product, infrastructure, and policies, and certifies that we meet or exceed specific levels of controls and processes for the security of user data.

In addition, we have purchased third-party software that continuously monitors our infrastructure and ensures we are compliance with our stated policies and procedures.


## Payment information

All payment instrument processing is safely outsourced to Stripe which is certified as a PCI Level 1 Service Provider. We don’t collect any payment information and are therefore not subject to PCI obligations.


## Employee access

All our employees sign a Non-Disclosure and Confidentiality Agreement when joining the company to protect our customers' sensitive information.
