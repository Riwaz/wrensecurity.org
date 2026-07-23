---
title: Wren:IG
sidebarDepth: 2
features:
  - title: Protection
    description: An additional layer of protection that provides authentication (and authorization) according to your security standards for any application.
  - title: Simplicity
    description: Works as a proxy, providing trustworthy security information to your systems. Simplifying implementation in the applications itself.
  - title: Control
    description: Changes in the security configurations can be made without altering the applications and central audit provides insight into potentially malicious activities.
  - title: Authentication & Authorization
    description: Secure your applications using industry-standard protocols, including SAML 2.0, OAuth 2.0, and OpenID Connect.
  - title: Single Sign-On (SSO)
    description: Let users authenticate once and access every application behind the gateway without logging in again.
  - title: Single Logout (SLO)
    description: Terminate all active sessions across connected applications with a single logout action.
  - title: Session Management
    description: Centrally manage and monitor active user sessions across all protected applications.
  - title: Password Replay
    description: Automatically supply credentials to legacy applications that don't support modern authentication protocols.
---

<script setup>
import { useData } from 'vitepress'

const { frontmatter } = useData()
</script>

# Wren:IG

## Overview

Place an identity gateway in front of your applications, microservices, and APIs to ensure consistent security
measures, regardless of their technology or authentication capabilities. Including the most problematic legacy
systems.

Wren:IG is a community‐developed reverse proxy server providing single sign-on (SSO) to any application behind
the proxy. Wren:IG includes a number of pre-built filters to transform data of intercepted requests / responses.
Scripted filter allows you to easily create your own filter using the Groovy language.

<FeatureGrid :columns="2">
  <FeatureCard
    v-for="feature in frontmatter.features"
    :key="feature.title"
    v-bind="feature"
  />
</FeatureGrid>

## Acknowledgments

Wren:IG is standing on the shoulders of giants and is a continuation of a prior work:

* OpenIG by ForgeRock AS

We'd like to thank them for supporting the idea of open-source software.


## Disclaimer

Please note that the acknowledged parties are not affiliated with this project.
Their trade names, product names and trademarks should not be used to refer to
the Wren Security products, as it might be considered an unfair commercial
practice.

Wren Security is open source and always will be.
