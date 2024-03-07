
---

# Policy for low quality mailing lists and sendings.

- **Version:** 1.0 
- **Date:** 2023-01-04 
- **Policy Owner:** CTO Marketing Line, SOC Manager 

- **Reviewed by:** Jesper Sörtoft, Deliverability Specialist (2024-03-06), Markus Palokangas, Development Manager (2023-05-04), Felix Denbratt, CTO Marketing Line (2023-05-04), Patrick Lidberg, Sales Enablement Manager (2023-02-04),  



### Version history
| Version     | Editor          | Description   | Date       |
|-------------|-----------------|---------------|------------|
| V.1.0.0     | Arkadiusz Zabicki, SOC team lead | First version | 2023-01-04 |
| V.1.0.1     | Arkadiusz Zabicki, SOC team lead | Minor adjustement to escalation policies added | 2023-02-07 |
| V.1.0.2     | Fredrik Wremerth, Operational Process Development Manager | Adding dispatch rules, List Hygiene session details | 2024-02-29 |
| V.1.0.3     | Arkadiusz Zabicki, SOC team lead | Fixing typos and updating support email address | 2024-03-06 |

---

## Introduction
This document defines a process for customers with low quality mailing lists/sendings: how customers are identified and how the communication and escalation process looks like when actions are needed to ensure bad sendings will stop. 

### Scope
This policy applies to Delivery team members who owns the process of identifying customers with low quality lists/sendigns and the communication process.

### Goals
Establish a clear communication and escalation process that can be easily followed by any delivery team member to ensure harmful sendings will get stopped. 

### Definitions

#### Bad sending
Sending is labeled as bad if it has high bounce rate (usually 10% bounces) or it is sent to bad domains that should have very few or no real subscribers. All sendings labeled as 'bad' are a result of the investigation of our delivery team.

## Policy

Whenever delivery team will discover bad sending, they will open a communication between APSIS and customer to help customer correct abusive behavior. For that reason an incident in Efficy U will be created by delivery team and email to the customer will be sent with the reason why the communication was initiated and what needs to be done in order to mitigate the issue.  We've divided bad sendings into 3 categories. For each of them initial communication will be different.

#### Sendings to old and outdated mailing lists 

This results in bounces which can lead to temporary blacklisting, but it's also an indication of subscibers without valid opt in which leads to spam complaints or permanent blacklisting in case they have been turned into spamtraps - even though they might at one point have been opt in. This is a fairly common problem with new customers, they rarely have any understanding of or training in email hygiene and the dangers of importing outdated lists.


##### Message template

**Title**: Important notice about outdated mailing list.

**Content**
```
Dear Customer,  

During our routine monitoring, we noticed an unusually high bounce rate for the email you sent on XXXX-XX-XX. Among your subscribers are many email accounts or domains that do not exist, which indicates that you are using an outdated list. 

All recipients must have a valid opt-in, which is confirmed opt-in within the last 6 months, or a recent history of email opens. Sending emails to recipients who do not exist, or did not provide explicit consent, will damage not only your own sender reputation, but also the IP reputation of our mail servers, which can affect deliverability for all APSIS and Efficy customers.  

Since good email deliverability has high importance to both you and us, we expect this issue to be resolved before your next sending. We are of course happy to help, and if you have any questions please reach out to our support: customerservice.apsis@efficy.com

What can you do? 

We recommend that you review your list of subscribers and remove the contacts that did not provide you with email consent or have been inactive for 6 months or more. If you have any questions about this, please reach out to us by replying directly to this email or contacting customerservice.apsis@efficy.com
```

#### Sendings to mailing lists that contains spambot signups 

This is possibly less of a problem in Apsis One since many/most are using signup forms with decent bot protection, but it does happen and when it does it's likely that there are spamtraps among the fake subscribers.

##### Message template

**Title**: Important notice about sending to mailing lists that contains spambot signups

**Content**
```
Dear Customer,  

During our routine monitoring, we noticed an unusually high number of recipients who are very unlikely to have signed up for the email you sent on XXXX-XX-XX. Many of these email addresses have been abused by spambots for decades, and most of them are on old US ISPs that have few active email users—and generally none in Europe. Some examples of abused addresses are: 

xxxxxx@bellsouth.net 

xxxxxx@earthlink.net 

xxxxxx@att.net 

xxxxxx@comcast.net 

Email addresses like these are most likely used by spambots on unsecured signup forms. All recipients must have a valid opt-in, which is confirmed opt-in within the last 6 months, or a recent history of email opens. Sending emails to recipients who do not exist, or did not provide explicit consent, will damage not only your own sender reputation, but also the IP reputation of our mail servers, which can affect deliverability for all APSIS and Efficy customers.   

Since good email deliverability has high importance to both you and us, we expect this issue to be resolved before your next sending. We are of course happy to help, and if you have any questions please reach out to our support: customerservice.apsis@efficy.com
 
What can you do?  

We recommend that you look through your list of subscribers to remove the contacts that did not provide you with email consent or have been inactive for 6 months or more. Most importantly, start securing your signup forms by enabling double opt-in. 

If you have any questions about this, please reach out to us by replying directly to this email or contacting customerservice.apsis@efficy.com

To learn more about spam traps and ISP please refer to our delivery help center: https://help.apsis.one/en/collections/3414375-resource-library#email-deliverability
```

#### Sendings with technical issues, such as DMARC with p=reject and no DKIM-signing with Apsis

This happens often, but it's the customers own fault (for implementing DMARC without understanding how it works or monitoring it) and it generally only affects the customers specific sending - not reputation.

In this scenario delivery team/soc will inform customer about the need for DKIM and guide them to our Customer Care at customerservice.apsis@efficy.com - Customer Care will take care of DKIM order - standard order will have to be sent to delivery team via Efficy U.

### 2nd level of escalation 

In case customer contacted in regard of bad sending won't act accordingly for our initial communication, a reminder will be send to them by delivery team with information that we expect correction of abusive behavior within the next 5 business days. If customer will reply to this email and ask for help in cleaning their list, ticket will be moved to Customer Service using the dispatching process: [efficy Dispatching Rules & Process for all product lines](https://efficy-my.sharepoint.com/:w:/p/fwr/EQcnqbmK0uZPpPNA6j94rTgByEo6naPjbJWw8pw1gdBtow?e=QG5raI). If customer will need professional assistance with cleaning up their email lists, our Professional Services department can assist them - if customer will request this service ticket will be moved to the Professional Services team according to the dispatch rules: [efficy Dispatching Rules & Process for all product lines](https://efficy-my.sharepoint.com/:w:/p/fwr/EQcnqbmK0uZPpPNA6j94rTgByEo6naPjbJWw8pw1gdBtow?e=QG5raI). The Professional Services team will handle the ticket and conduct a pre-sales consultation with the customer as well as perform the consulting work if the customer approves the consultancy.

Exception: if situation was caused by APSIS in result of insufficient onboarding, errors in migration, others - customer should not be charged for that.

If customer will not reply to this email, delivery team will send the last reminder with information that lack of proper action will result in locking the account after 2 business days.

### 3rd level of escalation

In case customer won't correct their behavior within 2 business days after 2nd escalation, all sendings from customer's account shall be disabled - account will be locked in backoffice via 'Lock account' button.

An email will be sent to customer via Efficy U with a notification that account has been locked and no new sendings can be scheduled.  

##### Message template

**Title**: Your account has been suspended due to violation of APSIS deliverability policy.

**Content**
```
Dear Customer,

Due to violation of APSIS deliverability policy your account is now suspended - access to the account for all users has been blocked by APSIS team.

In order to lift the suspension you need to fix the issues with your Audience communicated to you by our delivery department. For that reason we will add one user to your account that need perform necessary mitiagtion actions. Please send an email address of a person you wish to be added to the account to customerservice.apsis@efficy.com.

After applying all apropriate measures please send a message via our extranet about what was done to fix the issue and, if possible, what lead to this scenario in the first place. Your account will be checked by our delivery specialists and, if everything will be fine, it will become active again.

Best regards,

APSIS Delivery Team
```