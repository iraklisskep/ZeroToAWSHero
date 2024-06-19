---
title: "The Begining: Understanding the basics"
date: 2024-06-19
---

# Intro

Hello world! As I was studying about AWS products, I decided that I need to keep some notes. Inspired by other Cyber Security proffesionals, I started my own blog. So this is what this blog is about, my journey on learning about AWS and keeping notes that I wish might be usefull to some of you! 

### A little bit of me

My name is Iraklis Skepasianos, a 31 year old lifelong student, working as a Cyber Security Engineer and Tier 2 Analyst at a financial institution. I have lived in Greece for the last 29 years and since 2022 I reside in the beautiful Netherlands. 
Currently I am working with Microsoft Azure products, however this is soon going to change and I will be working with AWS. Despite having a good overview of the products of AWS, never had the opportunity to work with them, so I am planning to change that.
Note: I am going to usually compare/correlate Azure to AWS products, so if you have Azure background, I believe this is going to help you understand AWS easier.

### Bedankt

I would also like to say thanks to my work-husband and very good friend BJ, who has a great blog on KQL (kqlquery.com), and is moving to another company to follow his Incident Response wet dreams. He has helped me a lot to grow as a SOC Analyst and Engineer, taught me a lot and inspired me to start this blog and study more on cloud security. Bedankt and good luck my man!

# AWS Security Hub

Security Hub, Guard Duty, Detective, Inspector... What is going on? A bit overwhelming, so in the following lines I will try to best describe the products in 2-3 lines.

#### 1. Security Hub

Security Hub is the single pane of glass for all security products of AWS. Similar to Microsoft Sentinel, Security hub acts as CSPM, SIEM and SOAR solution of AWS. It utilizes machine learning to detect anomalies in the data that comes from numerous other products, including 3rd party ones. You can check your security posture, look into audit logs and automate responses on findings. Okay, but how do we investigate incidents? Well, that's something for Detective.

#### 2. Detective

Detective is used to investigate security indicents helping you understand the data and find the root cause. Additionally, it offers graph based visualization to help you better understand the environment and conduct a faster investigation. As I was checking the documentation, it seems it aggregates and correlates data from AWS CloudTrail, Amazon VPC Flow Logs, and GuardDuty findings. A good transition to GuardDuty right?

#### 3. GuardDuty

GuardDuty is the main tool for Threat Detection. It's main capabilities are: Continuous monitoring, threat detection, and alerting for AWS resources. This means that GuardDuty is between Security Hub and Detective. You can compare it with Defender, however it is only used for cloud resources. GuardDuty is *not* an EDR.

#### 4. Inspector

Last in the list is Inspector. Inspector is the vulnerability management of AWS. It assesses the security of AWS products, best practices, scan for vulnerabilities and provides remediation steps for vulnerabilities.

# How They Work Together

- Security Hub acts as the central console, bringing together findings from GuardDuty, Inspector, and other integrated services.
- Detective uses data from GuardDuty and other sources to help security analysts investigate and understand security events in detail.
- GuardDuty detects threats and feeds these findings into Security Hub and can also provide data for deeper investigation with Detective.
- Inspector provides vulnerability assessments that are also reported to Security Hub for a consolidated view.

![Aws Security Stack](https://d2908q01vomqb2.cloudfront.net/22d200f8670dbdb3e253a90eee5098477c95c23d/2022/11/18/img9-2.png)

# Outro

There are many other aspects in the Security stack of AWS. However this post is just an intro of this blog and the AWS security products. In the next post, we will talk about GuardDuty and how to set up a sample environment to demo GuardDuty's capabilities. If you read this far, thank you!
