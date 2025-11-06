🧠 My SOC Journey — Week 1: Email Phishing Analysis

As part of my hands-on blue team learning, I recently completed an Email Phishing Analysis Lab on Blue Team Labs Online
. This challenge, titled “The Planet’s Prestige,” was designed to simulate a real-world phishing investigation — and it truly tested both my analytical thinking and technical skills.

🔍 Objective:

To investigate a suspicious email, identify hidden threats, and uncover any embedded malicious payloads or encoded attachments.

🧰 Tools Used:

HxD, 7Zip, Gary Kessler File Signatures, SquareX, CyberChef, and ExifTool

🧩 My Approach:

Header Analysis:
I examined key headers such as Delivered-To, Received By, ARC Headers, and Authentication Results to trace the email route and check SPF/DKIM/DMARC validation.
Comparing From and Reply-To fields quickly revealed inconsistencies — a classic red flag in phishing emails.

Payload Examination:
The email contained an encoded message and a disguised attachment. Using CyberChef, I decoded the Base64 content and uncovered a file signature mismatch — the supposed .pdf was actually a .zip file!

File Signature & Hidden Content Discovery:
With HxD and Gary Kessler’s File Signature Database, I confirmed the true nature of the hidden files. One turned out to be a JPEG image, and another an Excel sheet concealing a secret code in the second worksheet — which I decoded successfully.

OSINT Verification:
I performed IP and domain reputation checks on the sender’s mail server and confirmed suspicious indicators that aligned with a potential phishing campaign.

🧠 Key Takeaways:

Always validate email headers — small inconsistencies can expose big threats.

File signatures never lie — what looks like a .pdf could be something entirely different.

Tools like CyberChef and ExifTool are invaluable in digital forensics and SOC investigations.

Phishing emails remain one of the most effective attack vectors — but with the right skills and vigilance, they can be dissected and neutralized.

This lab reinforced the importance of analytical rigor and tool mastery in threat detection and email forensics — a crucial skill set for any aspiring SOC Analyst.
