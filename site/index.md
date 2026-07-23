---
layout: home
title: 'Home'
hero:
  name: Identity & Access Management
  text: Open-Source Platform
  tagline: The freedom of open source. The robustness of enterprise solutions. A modular, scalable, and sustainable IAM platform designed to support organizations today and in the future.
  image:
    src: /wren-logo.svg
    alt: Wren Security logo
  actions:
    - theme: brand
      text: Explore the Platform
      link: https://docs.wrensecurity.org
    - theme: alt
      text: View on GitHub
      link: https://github.com/WrenSecurity

buildingBlocks:
  title: "All the Building Blocks of Digital Identity Security"
  description: "Use one component, or combine them into a broader IAM architecture for access management, lifecycle automation, directory services, gateway protection and integration."
  items:
    - title: Identity Governance
      description: Manage identity lifecycle processes, provisioning, workflows, self-service and governance automation.
      link: /projects/wrenidm/
      linkText: "Explore Wren:IDM"
    - title: Access Management & SSO
      description: Centralize authentication and authorization across applications and services, with federation and single sign-on.
      link: /projects/wrenam/
      linkText: "Explore Wren:AM"
    - title: Directory Services
      description: Store and serve identity data with a reliable LDAP directory foundation designed for enterprise workloads.
      link: /projects/wrends/
      linkText: "Explore Wren:DS"
    - title: Identity Gateway
      description: Protect applications, APIs and services with gateway-based access control and integration patterns.
      link: /projects/wrenig/
      linkText: "Explore Wren:IG"
    - title: Connector Framework
      description: Connect identity systems to applications, directories and infrastructure using reusable integration patterns.
      link: /projects/wrenicf/
      linkText: "Explore Wren:ICF"
# callout:
#   title: See how it all fits together
#   description: Understand the architecture, how the components interact, and which products to combine for your use cases.
#   link: /guide/
#   linkText: Platform Overview

openSource:
  title: "Why Open Source for Identity Infrastructure"
  description: "Identity & Access Management (IAM) is not just administrative software – it is critical infrastructure. Choosing an open-source foundation for your IAM stack delivers strategic, operational, and security advantages."
  items:
    - label: Strategic Independence
      description: Retain full sovereignty over your identity data, deployment models, and integrations. You have the freedom to manage the platform internally or leverage professional partner support on your own terms.
    - label: Auditability & Verifiable Security
      description: Trust should be verified. With open source, your security teams can inspect every line of code, run independent security audits, and guarantee there are no hidden vulnerabilities.
    - label: Continuous Evolution
      description: Benefit from a platform maintained by dedicated open-source experts. Open standards (OIDC, SAML, LDAPv3) ensure long-term interoperability and guard your infrastructure against technology deprecation.

# This section will be added later after additional content for it will be created.
# choosePath:
#   title: "Choose the path that matches your needs."
#   description: "Start with the path that fits your current IAM work. Evaluate Wren Security locally, plan a migration, prepare for production use or explore how to deliver open-source IAM solutions for clients. Each path gives teams a practical next step without assuming a single implementation model."
#   items:
#     - label: "01"
#       title: Evaluate Wren Security locally
#       description: Download our lightweight Docker Compose setup and run a complete reference IAM stack on your machine in under 15 minutes.
#       link: /guide/
#       linkText: Start Evaluating
#     - label: "02"
#       title: Migrate from legacy IAM
#       description: Modernising away from unsupported, end-of-life systems or high-overhead commercial platforms? Access structured guides on how to safely migrate your users, schemas, and security policies.
#       link: /guide/
#       linkText: Review Migration Path
#     - label: "03"
#       title: Upgrade OpenAM to Wren:AM
#       description: Keep your authentication infrastructure supported and secure. Access direct upgrade paths from legacy OpenAM to the modernized Wren:AM.
#       link: /guide/
#       linkText: Review Upgrade Path
#     - label: "04"
#       title: Run Wren Security in production
#       description: Prepare your environment for enterprise deployment. Explore high-availability blueprints, directory replication, and security hardening checklists.
#       link: /guide/
#       linkText: Plan Production Use
#     - label: "05"
#       title: Deliver Wren Security for clients
#       description: Deliver scalable IAM solutions for your clients. Explore adaptable enterprise blueprints, mitigate deployment risks, and secure certified L3 backend support.
#       link: /guide/
#       linkText: Join Partner Program

builtFor:
  title: "Built for Transparency, Security and Continuity"
  description: "Wren Security is built for teams that treat identity as critical infrastructure. Open code, standards-based architecture and documented upgrade paths help organizations inspect, maintain and evolve their IAM systems over time."
  items:
    - label: Open by default
      title: Transparency builds trust.
      description: The code, documentation and community discussions remain open. Knowledge is not gated. We believe in collaboration and technology that can be freely inspected, improved, and trusted.
    - label: Secure by design
      title: Security you can verify.
      description: Built around open standards, secure defaults, responsible vulnerability handling, and robust standards-based cryptography. Our approach to identity security is proactive, not reactive.
    - label: Crafted to last
      title: Built for continuity.
      description: Designed for modularity, stable operations, documented upgrade paths and long-term maintainability. We build software that endures, scales, and evolves alongside your organization.

actionBanner:
  title: "Secure Your IAM Infrastructure on an Open Foundation."
  description: "Whether you are setting up a local prototype or deploying an enterprise IAM stack, choose the path that fits your project."
  actions:
    - text: Explore the Platform
      link: https://docs.wrensecurity.org
    - text: View on GitHub
      link: https://github.com/WrenSecurity
    - text: Talk to a Partner
      link: /partners
---

<script setup>
import { useData } from 'vitepress'

const { frontmatter } = useData()
</script>

<BuildingBlocks v-bind="frontmatter.buildingBlocks" />
<OpenSource v-bind="frontmatter.openSource" />
<!-- <ChoosePath v-bind="frontmatter.choosePath" /> -->
<BuiltFor v-bind="frontmatter.builtFor" />
<ActionBanner v-bind="frontmatter.actionBanner" />
