---
title: Wren:IDM
sidebarDepth: 2
features:
  - title: Identity Lifecycle Management
    description: Automatically retrieve users from the source system and provision accounts to the target systems according to clearly defined rules.
  - title: Workflows
    description: Define your workflow and approval processes, and empower managers to make decisions in access provisioning while leaving the rest to automation.
  - title: Extensions
    description: Utilize a variety of extension points to customize the logic or the CRESTful interfaces and make sure that the identity management smoothly integrates into your existing environment.
  - title: Auditing
    description: Dig into the built-in audit tracks or integrate them with log collection and SIEM tools to get complete insight into the identity management activities.
  - title: User Self-Service
    description: Built-in self-service allows users to manage their identities. The changes are immediately reflected where necessary.
  - title: Connector Framework
    description: With connectors provided by Wren:ICF framework you can manage every piece of software within your organization.
---

<script setup>
import { useData } from 'vitepress'

const { frontmatter } = useData()
</script>

# Wren:IDM

## Overview

Regain control over people's access. Use Wren:IDM to streamline your identity governance and gain full control
over where and why users have access. Increase productivity with efficient access provisioning. Reduce operational
labour through automation and user self-service. And ensure that everyone has all the access they need, but no
other.

<FeatureGrid :columns="2">
  <FeatureCard
    v-for="feature in frontmatter.features"
    :key="feature.title"
    v-bind="feature"
  />
</FeatureGrid>

## Acknowledgments

Large portions of the source code are based on the open-source projects
previously released by:
* Sun Microsystems
* ForgeRock

We'd like to thank them for supporting the idea of open-source software.


## Disclaimer

Please note that the acknowledged parties are not affiliated with this project.
Their trade names, product names and trademarks should not be used to refer to
the Wren Security products, as it might be considered an unfair commercial
practice.

Wren Security is open source and always will be.
