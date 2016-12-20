# Information Security Policies <small>`Version 1.0 - December 2016`</small>

The _purpose_ of this document is to _clearly define_ our Information Technology
Security Policies, ensure they are kept _current_ with relevant legislation
and ensure they are available to all relevant stakeholders.

> If you notice a typo/error/ommission or area for improvement/clarification, <br />
please notify us by opening an issue on GitHub.


## Roles and Responsibilities (ISO27001:2013-A.6)

The following roles have been identified in our organization.

### Management/Leadership team

The Management/Leadership team is _ultimately responsible_ for the information
security in the organization; it is not "_outsourced_" to anyone else.


### Data Controller

_Day-to-day responsibility_ for checking that process/procedures for information
security are followed/met belongs to the `The Data Controller` ("**DC**").

DC is the person in the organization who is registered/named
with the **Information Commissioner's Office** (_UK_) and
responsible for ensuring that
[***Data protection principles***](https://ico.org.uk/for-organisations/guide-to-data-protection/data-protection-principles/)
are followed.

### Application Developers

The Application Developer(s) ("**Devs**") are responsible for _implementing_ the code and systems
which have the protection of people's personal data at _heart_.

Additionally **Devs** should make _reasonable_ efforts to keep their
knowledge and skill _current_ and keep track of security reports/advisories
which are relevant to the code which has been included/used in the application.


#### Developer Security Checklist

1. ***Minimise*** the amount of sensitive **P**ersonally **I**dentifiable **I**nformation (PII)
stored by the application/database (_e.g: if you don't need Social Security number don't ask for it!_)
2. Where **PII** is _required_ for the functionality of the App, ***Encrypt*** as much as possible/practical.
3. ***Never*** store **PII** in a session token (JWT) or `localStorage` (where it can be "_stolen_" by an "_XSS_" attack)
4. ***Always*** use **_strong_ passwords** for all systems & services.
5. ***Always*** use **multi-factor authentication** for Gmail, GitHub & AWS to limit the risk of
a malicious user gaining access to these mission-critical systems.

Under _no circumstances_ should a developer merge her/his own change/feature/bugfix.
Segregation of duties should exist wherever _practical_ to ensure accountability.

### Quality Assurance

The Quality Assurance (**QA**) person (_or team_) is responsible for
_checking_/_testing_ features of the application while they are being built
and before they are released to the "live" environment.
QA is the "_gate keeper_" between application developers and end-users.

Wherever possible/practical there should be a _segregation of duties_ between
the people who write the code and those who review it.

QA _should_ not _write_ code unless the team is small and the QA/developer
roles are being _alternated_.

# Technology

## Hardware & Devices

### Server/Infrastructure

_All_ the components of our application are run on the Amazon Web Services (AWS)
"Cloud" Computing Platform-as-a-Service (PaaS).

#### Restricted Access

Access to the "_Production_" AWS account is restricted to the Data Controller (DC).
The DC grants access to the DevOps person as required to perform their tasks
(_e.g: updating the certificate on the server cluster_) and once the task is complete
access is revoked.

A full audit trail of actions performed in the AWS Console is recorded
in case an involuntary (_or malicious_) negative action is performed.

For detail on AWS's compliance with relevant security standards see:
https://aws.amazon.com/compliance/soc-faqs/

### Desktops

No desktop computers are used in the organization.
All devices are portable (laptops, phones & tablets) see below.

### Laptops, Tablets & Mobile Devices

We operate a "Bring Your Own Device" (BYOD) scheme with our employees/contractors.

We require that all devices:
+ use full-drive encryption to protect any browser history data stored on the device.
+ never leave the device unattended in a public space
+ never connect to insecure Wifi networks
+ screen lock is enabled when ever the user is away from the keyboard _in the **office**_
to prevent unauthorized access to critical systems.
+ at the end of the useful life of the device is _must_ be reset to factory settings

#### Theft or Loss

All members of staff and contractors are required to notify the Data Controller
immediately in the event of loss or theft of any device.

In the event of loss or theft the passwords for all accounts should be reset
as a precautionary measure and the incident should be reported to the policy
(_or other relevant authority_).



### Removable Media

Removable media is not permitted in the organisation.
Where files need to be shared they are done through Google Drive
which has good access controls, audit logs and encrypted transmission.

## Access Control

### Password/Passphrase Policy

We have the following password/passphrase policy:
+ Length: 8 characters
+ Complexity:
  + at least one Upper case character
  + at least one lower case character
  + at least one Number
  + at least one special character e.g. punctuation or symbols (!@?)


## Security Awareness Training

_all employees and contractors_ are required to watch the following
security awareness training videos:

+ Malware: https://youtu.be/cKlRc1_f5NY
+ Phishing: https://youtu.be/WpaLmeHTp3I
+ WiFi Safety: https://youtu.be/T5HCy3udooo
+ OWASP Top 10 - Cross-Site-Scripting (XSS) Explained: https://youtu.be/ksM-xXeDUNs
(_the most common vulnerability in web applications_)

## Policy Review

### Annual (_Planned Interval_) Review

The policies and procedures contained within this document will be reviewed annually in the _first_ week of May. A 2 hour block time has been _scheduled_ for the morning of **_May the 4<sup>th</sup>_ 2017** and _calendar invite_ has been sent:

![annual-IT-security-policy-review-meeting](https://cloud.githubusercontent.com/assets/194400/21121467/79538e0a-c0c4-11e6-8859-b627fcedb7d8.png)

Note: Any additional people who are relevant/interested/available will be invited closer to the time.

### Ad-Hoc Review

The policies may be updated in response to a change in systems or service providers.

When a new technology or system is introduced into the company
e.g. a new piece of hardware or 3<sup>rd</sup> party service provider is
being considered we will review the requirements of the policies contained
herein and ensure compliance.

Where an amendment is required it will _first_ be discussed in a Github "_issue_"
- if a _formal_ meeting is required it will be scheduled - and the _outcome_
of the discussion will be recorded/reflected in this policy document.
