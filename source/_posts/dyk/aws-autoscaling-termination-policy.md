---
title: AWS Auto Scaling Termination Policy
author: Veronique Robitaille
categories:
  - - AWS
  - - Did You Know?
  - - Compute
date: 2017-06-13 10:42:32
tags:
- Auto Scaling
- Configuration
---
Did you know when you use the default termination policy with AWS Auto Scaling it doesn’t terminate the instance with the oldest launch configuration automatically?  It first tries to balance the number of instances across Availability Zones, then picks the Availability Zone with the most instances and terminates the instance with the oldest launch configuration.  If there are more than one, then it ends the process by randomly picking the instance to terminate.
