---
title: Wren:DS 5.1.0 Released
date: 2026-04-07
excerpt: |
  A new version of Wren:DS 5.1.0 has been released, bringing JDK 25 support,
  improved container image, security improvements, and important bug fixes.
sidebar: false
---

<Post>

A new version of [Wren:DS 5.1.0](https://github.com/WrenSecurity/wrends/releases/5.1.0) has been released.

This release brings important improvements across the board, including JDK 25 build support, migration to a UBI-based Temurin container image, and a number of bug fixes addressing replication, JMX monitoring, and the control panel. On the security side, the project has migrated from `sun.security.x509` to the Bouncy Castle API and adopted Scorecard security assessment with Dependabot integration.


## Changes

List of significant changes:

* Add JDK 25 build support
* Migrate to UBI-based Temurin container image
* Replace JUEL with Eclipse Expressly
* Replace clirr with japicmp for API compatibility checking
* Migrate from `sun.security.x509` to Bouncy Castle API
* Correct replication late queue handling
* Fix unavailable monitoring attributes over JMX
* Resolve false "unsaved changes" warnings in control panel
* Correct `writabilityPolicy` evaluation for `readOnlyDiscardWrites`
* Implement Scorecard security assessment and add Dependabot configuration
* Multiple dependency upgrades


## How to Get

Refer to the [Getting Started](https://docs.wrensecurity.org/wrends/latest/getting-started.html) page to learn how to get and run Wren:DS.

Alternatively you can run the official Docker image from [Docker Hub](https://hub.docker.com/r/wrensecurity/wrends):

```bash
docker run --rm --name wrends-test -p 1389:1389 -p 1636:1636 wrensecurity/wrends:5.1.0
```

</Post>
