---
title: Become a Partner
partnerItems:
  - title: Open-source foundation
    description: Wren Security components are freely available and built on established identity standards, including OAuth 2.0, OpenID Connect, SAML, and LDAPv3.
  - title: Flexible delivery model
    description: Solutions can be designed around specific client requirements without dependency on commercial licensing models.
  - title: Technical collaboration
    description: Architecture discussions, implementation guidance, and technical support are available when deeper platform expertise is useful.
  - title: Roadmap visibility
    description: Partners can stay closer to the development of Wren Security and provide technical feedback based on real implementation experience.
collaborationItems:
  - label: '01'
    title: Start the conversation
    description: A first discussion covers IAM experience, typical client projects, and the intended use of Wren Security.
  - label: '02'
    title: Explore the technical fit
    description: Relevant Wren Security components, architecture considerations, and areas where technical guidance may be useful are discussed.
  - label: '03'
    title: Work on real projects
    description: Collaboration can continue around evaluations, architecture design, implementation, migration, or production deployment as needed.
  - label: '04'
    title: Stay connected
    description: Partners can share implementation feedback, discuss technical developments, and stay connected to the evolution of Wren Security.
formBanner:
  title: Apply for partnership
  description: Partnership starts with a conversation about Wren Security, relevant IAM experience, and the types of projects where the platform could be used.
---

<script setup>
import { useData } from 'vitepress'

const { frontmatter } = useData()
</script>

# Become a Partner

Build and deliver IAM solutions on an open-source foundation designed for long-term maintainability and interoperability.

The Wren Security partner ecosystem is open to system integrators, IAM consultants, and solution providers delivering Wren Security-based solutions for their clients.

## Benefits of Partnership

Build and deliver IAM solutions on an open-source foundation designed for long-term maintainability and interoperability.

The Wren Security partner ecosystem is open to system integrators, IAM consultants, and solution providers delivering Wren Security-based solutions for their clients.

<FeatureGrid :columns="2" class="wren-partner-feature-grid">
  <FeatureCard
    v-for="item in frontmatter.partnerItems"
    :key="item.title"
    v-bind="item"
  />
</FeatureGrid>

## How Partnership Works

Wren Security partnerships are built around practical collaboration and the needs of individual partners and projects.

Partners can work with the team behind Wren Security on architecture, implementation questions, migrations, and other technical topics where deeper platform expertise is useful.

The scope of collaboration develops according to each partner's experience, client projects, and involvement with Wren Security.

## Partner Profile

Partnership is intended for organizations with experience in identity and access management, system integration, security architecture, or related enterprise technologies.

Relevant experience with Wren Security is valuable, while broader IAM expertise and the ability to design, deliver, and maintain production environments are equally important.

## How Collaboration Starts

<FeatureGrid :columns="2" class="wren-partner-feature-grid">
  <FeatureCard
    v-for="item in frontmatter.collaborationItems"
    :key="item.label"
    variant="outline"
    v-bind="item"
  />
</FeatureGrid>

<ActionBanner class="wren-partner-form-banner" v-bind="frontmatter.formBanner">
  <PipedriveForm form-url="https://webforms.pipedrive.com/f/c5fUU73glsU9MWZpV5rcAEBXFOieRr7OO4UKGSgyfmwgIQqpZEGvLdLc4NVtHXPyef" />
</ActionBanner>

Partnership inquiries are handled by Orchitech, the core maintainer of Wren Security. Wren Security remains open source; source code, documentation, and community resources remain publicly available.

<style scoped>
.wren-partner-form-banner {
  margin-top: 72px;
  margin-bottom: 32px;
}

.wren-partner-feature-grid {
  margin-top: 24px;
}
</style>