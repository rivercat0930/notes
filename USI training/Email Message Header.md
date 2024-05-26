# Email Header Analysis

## What is an Email?

Email, short for electronic mail, is a digital message sent from one computer to another over the internet or a network.

![](https://miro.medium.com/v2/resize:fit:720/format:webp/1*FszypaBw0fv6tvU52ChAEA.png)

- Composing the Message: The sender creates the message using an email client, such as Gmail.

- Sending the message: The message is sent through the Mail Transfer Agent (MTA) using Simple Mail Transfer Protocol (SMTP).

- Transfer of Message: The message travels over the internet or a network from one mail server to another through SMTP protocols until it reaches the recipient's mail server.

- Delivery Agent Check: The mail delivery agent checks whether the email is spam or non-spam using Sender Policy Framework(SPF). If it is non-spam, the email continues to the recipient's mailbox.

- Accessing the Message: The recipient accesses their mailbox to view the message and its content.

---

## Parts of an Email

1. Email Header

1. Email Body

1. Attachments

1. Signatures

1. Salutations

1. Closings

1. Quotations

---

## Analyze an email

Example Email Header:

```
Received: from TY0PR0101MB4165.apcprd01.prod.exchangelabs.com
 (2603:1096:400:1bb::9) by SI2PR01MB4273.apcprd01.prod.exchangelabs.com with
 HTTPS; Mon, 15 Apr 2024 14:20:03 +0000
ARC-Seal: i=2; a=rsa-sha256; s=arcselector9901; d=microsoft.com; cv=pass; b=Zfpgl5Yal0A1syPCftpM1jiSvYomifaADZqubkyehH8D25Ry1h2bWcoxKgTCuB1iDOm5DVwafcm9Tf6Z5AXhpQ/uoxi4idgH93FXQnHAYMrFvlXX+QCMZo6Nt8xvQDjBaAjbo057jA8rS8ICvaAzMeJX8/1M2T+EtZVOhI3JimH2eDAJ286VWUX6N1kjCuSeUbBnVNHKzPF+HkW+uJn/FrsOVG8lRsI/1VF8mWtyMYHXE3KAu/M8dnLol5mmTXuY0LQXHaS/6/S7t4I3mjbHQAWZxGEBa6sOKa90U0TmRVAP+qU14zzCnrqjxo42QLgAWQJrsZa6az5rcj9zZDOVYw==
ARC-Message-Signature: i=2; a=rsa-sha256; c=relaxed/relaxed; d=microsoft.com; s=arcselector9901; h=From:Date:Subject:Message-ID:Content-Type:MIME-Version:X-MS-Exchange-AntiSpam-MessageData-ChunkCount:X-MS-Exchange-AntiSpam-MessageData-0:X-MS-Exchange-AntiSpam-MessageData-1; bh=ppPCgz5KJUqOzgh8CC7MaJ5oEfM/j9nsUhKpn3UellY=; b=Hq6EHxVMlzCG6Fwa2t1cXbnMls7Og8KwfagZyas1NOi+r5v+f+VFvMhXLknOQu2jgYK4Q3r5ForI75pHQeDlcVPBDnFMXfAyxbZ9IuUliYTber/mgVz0kM4NKimc2kTo2a6Y0NHBp4lEsnwS9PqER6ZqKJdoz1ukW+/3tInB38ix6ggVPS0kDgzfxkEJBgOXIGeyOskSz+AWw1sVF28SsyX4ne4LFzWqCOwtBskuJA71LWQFnCWOL5DTSkAE2IJ8sSY0614rwkiyYYBtlZYp0Sq2/9MhX3Fpmc1DvI4wyTgXoK2swWE5+JvP/DdNxunaAD9qEMwUr5QytSMjMreMtA==
ARC-Authentication-Results: i=2; mx.microsoft.com 1; spf=pass (sender ip is 40.107.93.132) smtp.rcpttodomain=asteelflash.com smtp.mailfrom=transunited.com; dmarc=pass (p=none sp=none pct=100) action=none header.from=transunited.com; dkim=fail (no key for signature) header.d=transunited.com; arc=pass (0 oda=0 ltdi=1)
Received: from SG2PR02CA0123.apcprd02.prod.outlook.com (2603:1096:4:188::22) by TY0PR0101MB4165.apcprd01.prod.exchangelabs.com (2603:1096:400:1bb::9) with Microsoft SMTP Server (version=TLS1_2, cipher=TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384) id 15.20.7452.50; Mon, 15 Apr 2024 14:19:57 +0000
Received: from HK3PEPF00000220.apcprd03.prod.outlook.com (2603:1096:4:188:cafe::7a) by SG2PR02CA0123.outlook.office365.com (2603:1096:4:188::22) with Microsoft SMTP Server (version=TLS1_2, cipher=TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384) id 15.20.7472.33 via Frontend Transport; Mon, 15 Apr 2024 14:19:56 +0000
Authentication-Results: spf=pass (sender IP is 40.107.93.132) smtp.mailfrom=transunited.com; dkim=fail (no key for signature) header.d=transunited.com;dmarc=pass action=none header.from=transunited.com;compauth=pass reason=100
```

1. Return-Path:

    This field indicates the email address to which bounce message (undeliverable emails) are sent.

    It may differ from the "From" or "Reply-To" fields and can help identify the actual source of the email.

1. Received:

    This field provides a chronological list of servers or relays through which the email passed during its journey to your inbox.

    Each relay is represented by an entry containing information such as the IP address, server name, date, and time.

    ***You can using these information to examining if suspicious or unauthorized relays.***

    ```
    Received: from TY0PR0101MB4165.apcprd01.prod.exchangelabs.com (2603:1096:400:1bb::9) by SI2PR01MB4273.apcprd01.prod.exchangelabs.com with HTTPS; Mon, 15 Apr 2024 14:20:03 +0000
    ```

1. Message-ID:

    This field is a unique identifier assigned to each email.

    format: \<unique_id@domain\>

    ```
    Message-ID: <20240415071948.8976C81781726808@transunited.com>
    ```

1. From:

    This field specifies the sender's name and email address.

    ***Easily spoofed*** => Need alongside other header information to determine if the sender is legitimate.

1. Reply-To:

    This field indicates the email address where replies should be directed.

    ***Worth to checking this field to ensure it aligns with the sender's identity and is not pointing to a suspicious or unrelated address.***

1. X-Sender, X-Originating-IP, X-Mailer:

    These fields are often found in the header and provide additional information about the email’s origin, sender’s IP address, or the software used to send the email.

    While not always present, they can offer valuable insights during the analysis.

1. SPF, DKIM and DMARC:

    - SPF => Sender Policy Framework - Verifies that the email comes from an authorized server.

    - DKIM => DomainKeys Identified Mail - Uses a digital signature to verify the authenticity of the email.

    - DMARC => Domain-based Message Authentication, Reporting, and Conformance - Uses SPF and DKIM to ensure that emails are not spoofed.

1. X-Spam-Status, X-Spam-Score:

    ***Usually added by spam filters and indicate the likelihood of the email being spam.***

    ```
    X-Spam-Status: No, score=1.0 required=5.0 tests=BAYES_50,DKIM_ADSP_CUSTOM_MED,HTML_MESSAGE,MIME_HTML_ONLY,RCVD_IN_DNSWL_MED,URIBL_BLOCKED
    ```

1. X-antivirus or X-AntiAbuse:

    ***Some email servers append these fields to indicate if the email has been scanned for viruses or potential abuse.***

    ```
    X-AntiAbuse: This header was added to track abuse, please include it with any abuse report
    ```

---

Reference:

- [Step by step tutorial on email header analysis](https://blog.bugzero.io/step-by-step-tutorial-on-email-header-analysis-449a26700220)
