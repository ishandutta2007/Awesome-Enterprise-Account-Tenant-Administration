# Awesome-Enterprise-Account-Tenant-Administration

# Top Enterprise Account & Tenant Administration Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Multi-Tenant Identity, Directory Synchronization & Self-Hosted IGA*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Enterprise Account & Tenant Administration**. These tools help organizations manage identities, roles, and access across multiple tenants, directories, and applications—covering everything from cloud IAM suites to self-hosted identity governance platforms that eliminate per-user pricing at scale.

**Examples** include Microsoft Entra ID, Okta, Ping Identity, CyberArk, Workday, ServiceNow, Keycloak, Casdoor, ZITADEL, and midPoint (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted identity and access management, open-source tenant administration, and community-driven IGA—ideal for organizations seeking data sovereignty and avoiding per-user SaaS pricing that compounds across large workforces. The open-source landscape is genuinely mature: **Keycloak** provides battle-tested realm-based multi-tenancy used by countless enterprises [citation:2], **Casdoor** offers a lightweight Go-based alternative with built-in LDAP and RADIUS servers [citation:13], **ZITADEL** delivers event-sourced audit trails with infrastructure-level tenant isolation , and **midPoint** stands as the closest open-source equivalent to commercial IGA platforms [citation:11].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id)** | Cloud IAM with tenant-level administration, conditional access, and hybrid identity synchronization via Cloud Sync or Connect Sync. **P1: $6/user/month**; P2: $9/user/month adds Identity Protection and PIM. | P1: **$6/user/month**; P2: **$9/user/month** | **Free edition**: basic directory and security defaults with Azure/M365 subscriptions |
| **[Okta](https://www.okta.com/)** | Enterprise workforce and customer identity with multi-tenant org management. **Workforce Starter: $6/user/month** (annual); Enterprise: $17/user/month. Customer Identity requires separate base platform pricing. | Starter: **$6/user/month**; Enterprise: **$17/user/month** | No free tier for workforce; developer edition available |
| **[Ping Identity](https://www.pingidentity.com/)** | Enterprise IAM with identity governance, lifecycle management, and AI-driven access certification. **PingOne Workforce: from $3/user/month** (minimum 5,000 users); Customers: from $35,000/year. | Workforce: **$3/user/month** (min 5,000); Customers: **$35,000/year** | No free tier; demo via sales |
| **[CyberArk Identity](https://www.cyberark.com/)** | Identity security platform with SSO, MFA, and lifecycle management. Privileged access management available as separate product. | Quote-only | Free trial available |
| **[Workday Tenant Management](https://www.workday.com/)** | HCM tenant administration with FSE-based pricing. Worker type weighting and count overages (8–18% above clean census) are common. | Quote-only (FSE-based enterprise contract) | No free tier; demo via sales |
| **[ServiceNow System Administration](https://www.servicenow.com/)** | Platform administration with tenant-level configuration, role management, and audit logs. | Quote-only (enterprise contract) | No free tier; demo via sales |
| **[SAP Cloud Identity](https://www.sap.com/)** | Identity provisioning and SSO within the SAP ecosystem. | Quote-only (bundled with SAP licensing) | No free tier; demo via sales |
| **[Oracle Cloud Infrastructure IAM](https://www.oracle.com/cloud/)** | Cloud IAM with compartments, policies, and federation. **Always Free** tier includes limited IAM resources. | Pay-as-you-go beyond Always Free limits | **Always Free**: basic IAM with OCI free tier |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Keycloak](https://github.com/keycloak/keycloak)** | [![Stars](https://img.shields.io/github/stars/keycloak/keycloak?style=social&color=white)](https://github.com/keycloak/keycloak/stargazers) | **The most widely deployed open-source IAM with proven multi-tenancy.** Apache-2.0, Java/Quarkus. **Realms serve as the foundational isolation unit**—each realm manages its own users, credentials, roles, clients, and authentication policies independently [citation:2]. **One realm per tenant is the recommended pattern** for strongest isolation, though management overhead scales with realm count [citation:2]. Supports OAuth 2.0, OIDC, SAML, LDAP federation, and SCIM (since 26.8) [citation:10]. **Best for enterprises needing battle-tested multi-tenant identity** with extensive Java extension points and CNCF backing. |
| **[Casdoor](https://github.com/casdoor/casdoor)** | [![Stars](https://img.shields.io/github/stars/casdoor/casdoor?style=social&color=white)](https://github.com/casdoor/casdoor/stargazers) | **Lightweight Go-based IAM with built-in LDAP and RADIUS servers.** Apache-2.0. **Multi-tenancy via Organizations**—each with its own users, applications, providers, and roles [citation:3]. **Single Go binary** with support for MySQL, PostgreSQL, SQL Server, Oracle, SQLite, TiDB, and CockroachDB [citation:13]. **Standout features**: built-in **CAS server**, **LDAP server**, **RADIUS server**, and **70+ social/enterprise providers** including WeChat, DingTalk, and Lark [citation:13]. **MCP server and OAuth 2.1 for AI agents** built in—no other open-source IdP offers this natively [citation:10]. **Best for teams wanting a simpler-to-operate IAM** with legacy protocol support (LDAP/RADIUS) and AI-agent readiness. |
| **[ZITADEL](https://github.com/zitadel/zitadel)** | [![Stars](https://img.shields.io/github/stars/zitadel/zitadel?style=social&color=white)](https://github.com/zitadel/zitadel/stargazers) | **Event-sourced IAM with infrastructure-level tenant isolation.** AGPL-3.0, Go/TypeScript. **Strict multi-tenant hierarchy**: Identity System → Organizations → Projects, with isolated data and policy scoping at multiple levels . **Every mutation is written as an immutable event** for a complete, API-accessible audit trail—streamable to external systems via webhooks . **API-first design** with connectRPC, gRPC, and HTTP/JSON. **Zero-downtime updates** and horizontal scalability without external session stores . **Best for organizations needing the strongest audit trail and tenant isolation** with a modern, developer-friendly API. |
| **[midPoint](https://github.com/Evolveum/midpoint)** | [![Stars](https://img.shields.io/github/stars/Evolveum/midpoint?style=social&color=white)](https://github.com/Evolveum/midpoint/stargazers) | **The closest open-source equivalent to enterprise IGA (Identity Governance and Administration).** Apache-2.0 + EUPL. **Full provisioning, access reviews, role management, and connector library** covering AD/LDAP, Microsoft Graph, Exchange, and more [citation:11]. **Practitioners describe it as genuinely capable**—one REWE Group practitioner reported being reasonably happy with it in production, and another got HR data into the system and creating AD accounts with group assignments within days of evaluation [citation:11]. **Honest constraints**: documentation is not beginner-friendly, requires identity engineering experience, and community activity could be more active [citation:11]. **Best for organizations with in-house identity engineering capability** wanting enterprise IGA without commercial licensing. |
| **[LSC (LDAP Synchronization Connector)](https://github.com/lsc-project/lsc)** | [![Stars](https://img.shields.io/github/stars/lsc-project/lsc?style=social&color=white)](https://github.com/lsc-project/lsc/stargazers) | **Mature open-source directory synchronization engine.** BSD-licensed, Java. Reads from **any data source** (databases, LDAP directories, files) and transforms/compares data to an LDAP destination [citation:4]. Supports continuous sync, one-shot imports, and CSV/LDIF diff reports. **Active Directory-specific functions** built in: password updates, account status manipulation, lastLogon detection [citation:4]. **Best for organizations needing proven directory sync between heterogeneous sources and AD/LDAP** without a full IAM platform. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Tesseral](https://github.com/tesseral-labs/tesseral)** | [![Stars](https://img.shields.io/github/stars/tesseral-labs/tesseral?style=social&color=white)](https://github.com/tesseral-labs/tesseral/stargazers) | **Open-source auth infrastructure built specifically for B2B SaaS multi-tenancy.** Self-hostable or managed. Features: **B2B multitenancy** where customer admins control their own users' login methods, **self-service config pages** for customers, SAML/SCIM support without writing code, RBAC, MFA, passkeys, and API key management [citation:9]. **Best for B2B SaaS products** needing customer-facing tenant administration out of the box. |
| **[OpenIAM](https://github.com/openiam/openiam)** | [![Stars](https://img.shields.io/github/stars/openiam/openiam?style=social&color=white)](https://github.com/openiam/openiam/stargazers) | **Comprehensive open-source IAM with full user lifecycle management.** Community edition includes connectors for LDAP, Active Directory, Google Apps, relational databases, and Linux servers [citation:4]. Features: provisioning/deprovisioning, access review, certification, workflow, password management, audit, self-service, delegated administration, and SSO [citation:14]. **Best for organizations wanting a broader IGA feature set** than pure authentication providers offer. |

**Frameworks for building custom systems**: Choose **Keycloak** for battle-tested realm-based multi-tenancy with the broadest enterprise adoption [citation:2], **Casdoor** for a lightweight Go binary with built-in LDAP/RADIUS and AI-agent MCP support [citation:13], **ZITADEL** for event-sourced audit trails and strict tenant hierarchy , or **midPoint** for full IGA capabilities (access reviews, certification, SoD) when you have identity engineering expertise [citation:11]—all without per-user pricing that compounds across large workforces.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Enterprise account and tenant administration platforms handle authentication credentials and identity data; enforce MFA, least-privilege access, and compliance with applicable regulations (GDPR, SOC 2, HIPAA where relevant). **Tenant isolation failures can expose one customer's data to another.**
- **Open-source IAM has different trade-offs across projects.** **Keycloak's realm-per-tenant model provides the strongest isolation** but management overhead scales with tenant count—a shared realm with groups is lighter but weaker for strict compliance [citation:2]. **Casdoor is the lightest to operate** (single Go binary) and uniquely offers built-in LDAP/RADIUS servers and MCP support for AI agents [citation:13]. **ZITADEL provides the strongest audit trail** through event sourcing, but its AGPL-3.0 license may matter for some organizations . **midPoint is the only open-source option matching commercial IGA** (access reviews, certification, SoD), but **documentation is not beginner-friendly and requires identity engineering experience** [citation:11]. **Commercial platforms are quote-only at enterprise scale** except Microsoft Entra ID ($6–$9/user/month) and Okta ($6–$17/user/month). **Validate tenant isolation requirements, IGA feature needs, and operational capacity** before committing.

---

**Made for identity architects, IT administrators, and organizations building multi-tenant identity infrastructure.**  
Let's make enterprise account and tenant administration more open, isolated, and auditable.
