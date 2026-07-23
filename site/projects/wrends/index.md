---
title: Wren:DS
sidebarDepth: 2
features:
  - title: Uniform Access
    description: Access the data using the established LDAP (Lightweight Directory Access Protocol) or leverage the REST API where necessary.
  - title: Efficiency
    description: It can withstand even the highest loads on its own, but use replicated deployments to make your critical authentication services highly available.
  - title: Security
    description: Fine-grained access control, coupled with a comprehensive audit, ensures that your most valuable data is always secure.
---

<script setup>
import { useData } from 'vitepress'

const { frontmatter } = useData()
</script>

# Wren:DS

## Overview

Efficiently store and organize your digital identities, even in the most complex IT environments. Wren:DS provides
a secure and scalable directory service that complies with industry standards.

Wren:DS is an LDAPv3 compliant directory service built for the Java platform. Its easy installation process,
combined with the power of the Java platform, makes Wren:DS the simplest, fastest directory to deploy and manage.

<FeatureGrid :columns="2">
  <FeatureCard
    v-for="feature in frontmatter.features"
    :key="feature.title"
    v-bind="feature"
  />
</FeatureGrid>

## Acknowledgments

Wren:DS is standing on the shoulders of giants and is a continuation of a prior work:

* OpenDS by Sun Microsystems
* OpenDJ by ForgeRock AS

We'd like to thank them for supporting the idea of open-source software.


## Disclaimer

Please note that the acknowledged parties are not affiliated with this project. Their trade names, product names
and trademarks should not be used to refer to the Wren Security products, as it might be considered an unfair
commercial practice.

Wren Security is open source and always will be.