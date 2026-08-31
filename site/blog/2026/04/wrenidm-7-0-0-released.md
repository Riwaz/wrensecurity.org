---
title: Wren:IDM 7.0.0 Released
date: 2026-04-02
excerpt: |
  We are excited to announce the release of Wren:IDM 7.0.0. This major
  release brings Jakarta EE migration, JDK 25 support, and upgraded dependencies.
sidebar: false
---

<Post>

We are excited to announce that the brand new release of [Wren:IDM 7.0.0](https://github.com/WrenSecurity/wrenidm/releases/7.0.0)
is finally out!

This major release marks a significant milestone with the migration to Jakarta EE dependencies, ensuring long-term compatibility with the modern Java ecosystem. JDK 17 is now the minimum supported version, while JDK 25 is fully supported, keeping Wren:IDM aligned with the latest Java releases.
All major dependencies and Wren:ICF connectors have been upgraded, and the workflow engine has been migrated from Activiti to [Flowable](https://www.flowable.com/).


## Changes

List of significant changes:

* Migration to Jakarta EE dependencies
* Add JDK 25 support (JDK 17 is now the minimum supported version)
* Upgrade of all major dependencies and Wren:ICF connectors
* Change Wren:ICF _groupId_ to `org.wrensecurity.wrenicf.connectors`
* Migrate workflow engine to Flowable
* JDBC repository service overhaul (support additional native data types and COUNT queries)


## How to Get

Refer to the [Getting Started](https://docs.wrensecurity.org/wrenidm/latest/getting-started.html) page to learn how to get and run Wren:IDM.

Alternatively you can run the official Docker image from [Docker Hub](https://hub.docker.com/r/wrensecurity/wrenidm):

```bash
docker run --rm --name wrenidm-test -p 8080:8080 wrensecurity/wrenidm:7.0.0
```


### Upgrade to Wren:IDM 7

If you are upgrading from an existing Wren:IDM instance, please refer to the
[Upgrade Guide](https://docs.wrensecurity.org/wrenidm/latest/deployment/upgrade.html#_wrenidm_7)
for detailed instructions.

</Post>
