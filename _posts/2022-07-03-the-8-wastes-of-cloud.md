---
title: The 8 Wastes of Cloud
description: >-
  Optimising the Cloud Cost is the top priority for 70% of Enterprises according
  to State of Cloud reports by Flexera…
date: '2022-07-03T00:29:59.712Z'
categories: []
keywords: []
slug: /@ar.arun/the-8-wastes-of-cloud-d364b35425fe
---

According to the [State of Cloud](https://resources.flexera.com/web/media/documents/rightscale-2019-state-of-the-cloud-report-from-flexera.pdf) reports from Flexera, optimising the cloud spend is the top priority for around 70 percent of the enterprises.

With respect to optimising cloud spend, I found many articles that speak about housekeeping techniques that one can use, for instance, remove orphan resources, switch off test environments, etc., None of them gave me an encompassing view of addressing the cost issue covering all aspects.

To optimise the cloud spend, identifying wastes in the cloud implementation is a good starting point. Here I will touch upon aspects that can be looked at to identify waste taking inspiration from Lean. Before getting into 8 wastes, it is key to understand what can be termed as Waste and reason behind choosing Lean methodology for inspiration.

> Waste is any activity that produces no value to the customer. Non-value adding activity that can be eliminated is one form of waste. Non-value adding activity but unavoidable is another form of waste which needs to be reduced.

Reducing and eliminating wastes is embedded in one of the [5 core principles](https://en.wikipedia.org/wiki/Lean_manufacturing) of Lean methodology. So to identify entire spectrum of wastes in a cloud implementation, you can rely on the 8 wastes identified in Lean methodology.

![](C:\Users\wing\Downloads\medium-export\posts\md_1717553334817\img\1__ZbCXhGj5jzXsuYwfXrbR__A.png)

Being able to identify these wastes is the first step. This step, known as [Gemba Walk](https://en.wikipedia.org/wiki/Gemba#Gemba_Walk) in Lean terminology, is best done by browsing through the ‘[Gemba](https://en.wikipedia.org/wiki/Gemba)’(here it is the cloud implementation) and talking to its cloud engineers.

I will walk you through the 8 Lean wastes and will attempt to map each one of them to a relevant one in cloud implementation,

### 1\. Defects

Defect waste is a straight forward one to translate to cloud. If a cloud implementation doesn’t behave as intended then its a defect. Defect costs effort-and-time and are preventable.

Testing the code is the best way to avoid defects in SDLC. Now that infrastructure being coded using Infrastructure-as-Code practices, it is imperative that Test Driven Development (TDD) be followed to reduce defect waste. Tools like [TerraTest](https://terratest.gruntwork.io/), [LocalStack](https://localstack.cloud/), [ServerSpec](https://serverspec.org/) and many similar tools are available to unit test, integration test and end-to-end test your infrastructure code.

Another example of defect waste in cloud is when a cloud engineer uses an incorrect configuration (say, incorrect size) while provisioning the resources since there is no correct configuration defined. Proper resource capacity planning process can reduce such defect wastes.

### 2\. Overproduction

In Cloud implementation, overproduction relates to provisioning a different size of a resource or the resource being kept running or idle for a longer period of time than its actually necessary. This happens due to [just-in-case mindset](https://en.wikipedia.org/wiki/Just_in_case) instead of [just-in-time mindset](https://en.wikipedia.org/wiki/Lean_manufacturing).

A well known example is keeping the test environments switched on 24/7 even though the users (testers/developers) are going to use it only during their working hours. Infrastructure-as-Code practice and scheduling the switching on/off of the environment will reduce this type of overproduction waste.

Overprovisioning also falls in this waste category. Tools like [InfraCost](https://github.com/infracost/infracost) will help in determining the cost estimate of a resource configuration even before provisioning or making the changes to the existing infrastructure.

### 3\. Waiting

Wastes due to waiting is about people or resources being idle.

Environment downtime, dependency on other systems and waiting for approvals are waiting wastes.

Approval delays can be reduced by adopting more real time communications like in-person or instant messaging rather than mails. Forming cross functional teams that are independent to take decisions is another way to address this issue. It might take time to fully implement this kind of team structure but this will democratise decision making powers which is key for Lean approach.

### 4\. Non-Utilised Talent

This waste is about not utilising the human potential or utilising them for non-value adding work.

Cloud Engineers often needing to fight fires than using their skills for continuous improvement is a talent waste. Another instance is defining the cost budget for an application without involving the application team.

### 5\. Transportation

In Cloud implementation, Transportation waste is about unnecessary movement of data or resources.

For example, movement of data across different availability zones or regions is a waste since there is a cost involved. So its good to reevaluate the frequency of data backups. Another example of transportation waste is hosting an application in a far off region than the one close to the users.

Transportation waste also relates to hand-off of work from one person to another that results in loss of knowledge but this one is not just limited to cloud implementation.

### 6\. Inventory

Inventory waste in Cloud implementation is about data or resources kept on standby than necessary without adding any value.

Storing the data for a longer time period than its required by its compliance requirement is an inventory waste. Storing the archive data in a high cost storage service like S3 Standard than on an archive service liked S3 Glacier is another inventory waste.

Other inventory wastes are unused instances, unallocated (“zombie”) resources, orphan snapshots and unattached persistent volumes. Regular audits and housekeeping will reduce this waste.

### 7\. Motion

In manufacturing, this is unnecessary movement such as reaching out for tools or parts. If you abstract it, Motion waste is exerting unnecessary repeated effort to carry out day-to-day tasks. [Task switching](https://www.forbes.com/sites/jeanchatzky/2016/05/06/3-reasons-multitasking-is-a-huge-waste-of-time-and-how-to-stop-doing-it/) is also a motion waste.

Spending manual effort for setup/configuration of application during each and every application deployment is a motion waste. Instead you can use [application containers](https://www.sumologic.com/blog/application-containers-vs-system-containers-understanding-difference/) to avoid it.

### 8\. Excess Processing

This last form of waste occurs when non-value adding steps or activities are done to complete a process. For instance, an approval step in a provisioning process, where in an automated check suffices, is a waste.

Non-value adding features added to a product also comes under this type of waste. For instance, provisioning High Availability (HA) or Disaster Recovery (DR) setup to an application more than its required is an excess-processing waste.

### Next steps

To truly work on Cloud Optimisation, you need to go beyond just identifying the cloud wastes. You need to look at **why** the waste is there in the first place and **what** can be done about the cause of the wastes.

Hope you found this useful. What are the other cloud wastes that comes to your mind? Let me know in the comments section.