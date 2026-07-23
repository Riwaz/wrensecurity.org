---
title: Wren:AM
sidebarDepth: 2
features:
  - title: Single Sign-On
    description: Centralize authentication and uniformly protect all your applications according to the highest security standards, while also improving the login experience.
  - title: Multi-Factor Authentication
    description: Add OTP, SMS, Email, or 3rd party MFA tools to your authentication flow for additional protection against compromised passwords.
  - title: Adaptive Authentication
    description: Do not compromise between security and login experience. Adjust the authentication requirements based on the evaluated risk.
  - title: Identity Provider
    description: Take control of access to external or cloud services. Leverage an identity provider to supply service providers with authentication that complies with your policy and security rules.
  - title: Federations
    description: Establish an identity federation or connect with an existing one to link the identities across multiple identity management systems.
  - title: Standard Protocols
    description: OAuth 2.0, OIDC, SAML,... Choose from a variety of authentication protocols to easily integrate your applications according to industry standards.
  - title: Social Login
    description: Delegate authentication to 3rd-party services like Google, Facebook, GitHub, or any other compatible identity provider, to make the sign-in and onboarding even more convenient.
  - title: User Self-Service
    description: Place the user self-registration, account management, and password reset features where they belong, without the need to re-implement it in your apps.
  - title: Authorization
    description: Consolidate the management of your access policies and implement fine-grained access control to multiple resources using a central policy decision point.
---

<script setup>
import { useData } from 'vitepress'

const { frontmatter } = useData()
</script>

# Wren:AM

## Overview

A secure portal for your digital services. Use Wren:AM to establish consistent access policies and advanced
observability across all your applications, cloud services and IT infrastructure with minimal effort. Avoid
multiple logins with Single Sign-On to deliver a superior login experience for your users.

<FeatureGrid :columns="2">
  <FeatureCard
    v-for="feature in frontmatter.features"
    :key="feature.title"
    v-bind="feature"
  />
</FeatureGrid>

## Acknowledgments

Wren:AM is standing on the shoulders of giants and is a continuation of a prior work:

* OpenSSO by Sun Microsystems
* OpenAM by ForgeRock AS

We'd like to thank them for supporting the idea of open-source software.


## Disclaimer

Please note that the acknowledged parties are not affiliated with this project. Their trade names, product names
and trademarks should not be used to refer to the Wren Security products, as it might be considered an unfair
commercial practice.

Wren Security is open source and always will be.
