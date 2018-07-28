---
title: Email Encryption is here!Use STARTTLS everywhere!
layout: page
comments: true
social-share: true
show-avatar: true
---

Historically most email has been unencrypted, and that has a serious flaw: unencrypted email can be read and modified by anyone between the sender and final receiver. Tools to do “end-to-end” encryption of email (to prevent reading and/or modifying it) have been available for decades, but they are often hard to use by “normal” users.

Thankfully, there’s been work to significantly improve email security. In particular, STARTTLS email encryption is now widely supported, and the Electronic Frontier Foundation “STARTTLS Everywhere” initiative is working to get everyone to support STARTTLS in their email systems. 

STARTTLS is not perfect, as discused below. My point is that it’s way more secure than most email without it, because it improves security without requiring end-users to do anything. Below is additional information that I think you’ll find interesting.

First, here’s how STARTTLS works. Email is transmitted by a series of “hops”; if the hop recipient supports STARTTLS, email is automatically encrypted on that hop as it goes through the infrastructure, without requiring email users to do anything special. That ease-of-use is a big deal - users normally do whatever is the default, so if the default is secure, then users will normally do the secure thing.

Lots of organizations now support STARTTLS. Google reports that by 2018-07-24 90% of its incoming email, and 90% of outgoing email, was encrypted using STARTTLS (“Email encryption in transit”). Many email services support STARTTLS, including Gmail, Yahoo.com, Outlook.com, and runbox.com. (This includes the top email services.) Many other organizations support STARTTLS, including Google, Microsoft, Bank of America, The American Red Cross, The Salvation Army, The Software Engineering Institute (SEI), Carnegie Mellon University (CMU), and University of California, Berkeley. I give this list to show that there are many different kinds of organizations that support STARTTLS. The STARTTLS Policy List has an incomplete list of organizations known to be supporting STARTTLS.

There are some historical problems that the STARTTLS Everywhere project is working to fix:

* Some people allow the absurdly old vulnerable protocols SSLv2 and SSLv3 when using STARTTLS, instead of using the newer TLS protocols. TLS version 1.0 came out in January 1999, so there’s been plenty of time to transition away from SSLv2 and SSLv3. The STARTTLS Everywhere project expressly warns about that, and won’t give credit unless you’re using TLS.

* Some sites with STARTTLS use invalid certificates. STARTTLS Everywhere tells you about that, and also explains some solutions so you can use valid certificates instead.

* Historically active attackers can downgrade email encryption by stripping away the STARTTLS request, or can interpose nonsense certificates so that they receive the encrypted email instead. The STARTTLS Everywhere project has created a “STARTTLS Policy List” where supporting organizations can assert that they always use STARTTLS using a valid certificate. Organizations should join that list and check that list before they send email. Once they do, email transmissions cannot be downgraded and certificates cannot replaced, because senders will know to only use STARTTLS with valid certificates for those organizations.

STARTTLS is not an end-to-end encryption system. STARTTLS only encrypts while the email is being sent between systems (“hops”). That’s not all bad. For example, it means that receiving organizations can continue to examine the emails to check for viruses/malware, counter spam, and so on. But of course, there are downsides.

STARTTLS is, in general, not as strong as an end-to-end encryption system (from the point-of-view of providing confidentiality and integrity). For example, receiving organizations (and anyone who subverts their email system) can see and modify the email. Users who do not trust their email service providers should not depend on STARTTLS; they must use end-to-end encryption. In general, end-to-end encryption is stronger, so we should still work to make end-to-end email encryption easier to use and deploy. But for various reasons it’s hard to deploy end-to-end email encryption, and we’ve spent decades trying. Also, STARTTLS works just fine with end-to-end encryption.

Please indulge me: I think a small rant is appropriate here. There are some security specialists who think that only the perfect is acceptable. Nonsense! Requiring perfection is crazy. I think it is important, when creating and maintaining systems, to have an engineering mindset. In particular, you must always remember that that choices have trade-offs. It is not possible to have no risk; an asteroid might land on your head tomorrow. It is not reasonable to demand that systems be used regardless of their difficulty or expense; we all have limited time and money. Security issues are real, and we do need to address them, but time, money, and ease-of-use also matter greatly.

Unlike most other systems, STARTTLS is completely automatic (end-users don’t have to do anything) once it is set up, it is not hard to set up, and it counters a large class of attacks. For almost all users, email encryption with STARTTLS is a major improvement over what they had before. Let’s keep working to deploy even better systems, but let’s take partial victories where we can get them.