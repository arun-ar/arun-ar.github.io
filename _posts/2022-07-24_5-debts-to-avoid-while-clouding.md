---
title: 5 Debts to avoid while Clouding
description: >-
  When it comes to removing technical debt in cloud migration, there is more to
  it than just version upgrading your application stack.
date: '2022-07-24T19:17:21.367Z'
categories: cloud migration
keywords: []
tags: cloud migration tech-debt
slug: /@ar.arun/5-debts-to-avoid-while-clouding-d3692ef25171
---

> When you are confronted by any complex social system…with things about it that you’re dissatisfied with and anxious to fix, you cannot just step in and set about fixing with much hope of helping…If you want to fix something, you are first obliged to understand…the whole system.

> — Lewis Thomas, The Medusa and the Snail: More Notes of a Biology Watcher.

While migrating an application to Cloud, version upgrading the OS or App server or DB engine that are out-of-support (or about-to-be) is typically done as part of the technical debt removal. But when it comes to technical debt in cloud migration, there is more to it than that.

Wikipedia defines Technical Debt as

> …the implied cost of additional rework caused by choosing an easy solution now instead of using a better approach that would take longer.

When it comes to cloud migration, if a migration activity results in additional rework to make the application perform at optimum level then the cost of rework is a debt. So,

> Application Migration Debt can be termed as the result that occurs when the migration team takes certain actions to expedite the migration which later requires rework , incurring additional cost, effort and time.

Migration debt usually occurs when an application that resides in a data centre (DC) environment, that has been tuned to take advantage of its current environment, is migrated as is (commonly known as Lift-and-Shift approach) to cloud environment.

So, while migrating an application to cloud, the following 5 aspects should be accounted for.

1.  Performance
2.  Stability
3.  Operations — Incident Management/ Change Management /DR
4.  Security
5.  Run Cost

### 1\. Performance

After migrating the application to cloud, if it experiences intermittent performance problems or misses its performance requirements or experiences latency issues while integrating with dependents applications or components then it can be termed as having performance related debt.

This can be mainly attributed to sizing the server (CPU, memory, disk space) and network (connections, bandwidth), skipping performance tests. Each kind of user of the application should be taken into account. There might be front-desk-users accessing the application via a secure tunnel to DC, in which case the migration tests should include performance-testing the secure tunnel too.

Beyond right-sizing the servers, enhancing the application to horizontally scale is the solution to improve and maintain its performance in the cloud.

Another cause of performance issues could be due to migrating a part of the application leaving the rest in DC. Sometimes, this could be unavoidable but it should not become a norm. Overall migration plan should consider grouping the applications based on their inter dependencies and executed as waves.

### 2\. Stability

Stability of an application depends on two factors, namely, application health and user experience. Post migration, if the application gets more defects in terms of service availability or user experience, considering there is no functional changes done, then it can be termed as having stability related debt.

Inefficient configurations of infrastructure or application on the cloud is the key contributor for application instability.

For example, in a DC environment, autoscaling is not something that is commonly done, so this configuration is error prone when done in cloud without sufficient testing. Autoscaling an application based on the CPU or memory threshold depends on the configuration of health check interval. If the default health check interval, say 5 minutes, is too long then the application will go down and become unavailable.

Also, based on the application’s traffic pattern and other needs, Operations team should be able to choose from various auto scaling options, namely, simple scaling, step scaling, predictive scaling and scheduled scaling.

### 3\. Operations

Operations related debt comprises of issues in managing the incidents or changes to application or disaster recovery.

For instance, applications logs in DC environment are configured within the server but in cloud, servers are not permanent assets. If the logs are not centralised using a cloud service then there will be gaps in monitoring, leading to longer time to defect resolution. As a best practice, all logs are stored in a centralised logging account to manage them better.

Application and Operations teams need to be up-skilled in cloud before (or while) moving to cloud.

### 4\. Security

Post Cloud migration, if security issues prop up due to incorrect or insufficient security configuration of network or servers, then the application has security related migration debt.

For instance, an internal employee-facing-web-application, when put on cloud, might be exposed to whole web until its access is secured over a VPN or a similar security setup. Similar setup should be applied to the operations/development team accessing the application on cloud.

### 5\. Run Cost

In cloud, application run cost is a variable one as opposed to DC. So meeting the cost target is a critical aspect of successful migration. Run Cost related debt is when the application fails to meet its cost savings target.

For example, if an application, with an active-passive setup across two DC, is migrated as is to cloud with a Disaster Recovery (DR) setup across two regions(with warm standby approach), then the application run cost will not meet its cost savings target and it might even end up much more than in DC .

Providing cost breakup at application level (like cost per application, cost per environment, cost per feature) is the first step towards making cost as one of the architectural fitness function for application teams. Further, unit level cost (like cost per search, cost per booking) breakup will provide further clarity if the increased cost is due to business growth or otherwise.

If you need a head start on optimising cloud cost, you can have a look at [my previous article](https://medium.com/@ar.arun/the-8-wastes-of-cloud-d364b35425fe) on cloud wastes.

### Concluding Thoughts

Migrating an application to cloud requires understanding the nature of the application and its dependencies via Systems-Thinking lens since it encourages to zoom out and see the broader picture. It enables to paint an holistic view, in terms of perceiving the bottlenecks, leverage points and feedback loops, that needs to be taken care of.

Talking about Systems Thinking, I could relate application migration with homeostasis of a system. So, what is Homeostasis?

_Homeostasis can be described as the state of a system in which variables are regulated so that internal conditions remain stable and relatively constant, despite changes in the system’s environment._

Body temperature control in us is a typical example of homeostasis.

Similarly, as part of cloud migration, when changing the environment of an application from DC to cloud, you should ensure that relevant internal homeostatic changes are done to ensure the application remains stable and performs optimally.

Comment if you find this article useful.