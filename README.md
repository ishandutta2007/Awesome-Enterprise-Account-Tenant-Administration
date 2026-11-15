# Awesome-Enterprise-Account-Tenant-Administration

## Top Enterprise Account & Tenant Administration Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Multi-Tenant Identity, Directory Synchronization & Self-Hosted IGA*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Enterprise Account & Tenant Administration**. These tools help organizations manage identities, roles, and access across multiple tenants, directories, and applications—covering everything from cloud IAM suites to self-hosted identity governance platforms that eliminate per-user pricing at scale.

**Examples** include Microsoft Entra ID, Okta, Ping Identity, CyberArk, Workday, ServiceNow, Keycloak, Casdoor, ZITADEL, and midPoint (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted identity and access management, open-source tenant administration, and community-driven IGA—ideal for organizations seeking data sovereignty and avoiding per-user SaaS pricing that compounds across large workforces.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global Identity and Access Management (IAM) and Enterprise Administration market is valued at approximately **$24.3 billion to $25.6 billion in 2026** (up from ~$20.5B in 2025) and is projected to expand at a CAGR of ~15% to over $45 billion by 2031.  
The sector remains **moderately fragmented**: while foundational directory and single sign-on infrastructure experiences strong hyperscaler concentration (e.g., Microsoft Entra ID), specialized governance, customer identity, privileged tenant security, and machine identity ecosystems feature diverse independent platform leaders and emerging point solutions.

## SaaS/Hosted Platforms

| Product | Company Size (Market Cap / Revenue) | Description | Pricing (Starting Tier) | Free Tier / Trial Limits |
|---|---|---|---|---|
| **[Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id)** | ~$3.1T Market Cap / ~$245B Ann. Rev | Cloud IAM with tenant-level administration, conditional access, and hybrid identity synchronization via Cloud Sync or Connect Sync. | Entra ID P1: **$6.00/user/month** (annual commitment); P2: $9.00/user/month | **Free edition**: Basic directory and security defaults with Azure/M365 subscriptions (unlimited users for basic core SSO/sync) |
| **[Oracle Cloud Infrastructure IAM](https://www.oracle.com/cloud/)** | ~$480B Market Cap / ~$53B Ann. Rev | Cloud IAM with compartments, policies, identity domains, and cross-cloud federation. | Basic OCI IAM: **$0.00/month** (Included); OCI IAM Premium: **$3.20/user/month** | **Always Free tier**: Unlimited users for base OCI tenancy administration and resource management; includes $300 cloud credits for 30 days |
| **[SAP Cloud Identity Services](https://www.sap.com/)** | ~$280B Market Cap / ~$34B Ann. Rev | Identity provisioning and single sign-on embedded within the SAP Business Technology Platform ecosystem. | Bundled with SAP BTP subscriptions; unbundled test/dev tenants starting at **~$0.20/user/month** or base service packs | **SAP BTP Free Trial**: 90-day trial capped at 1 trial tenant and a maximum of 50 users (no on-premise Cloud Connector support) |
| **[ServiceNow System Administration](https://www.servicenow.com/)** | ~$215B Market Cap / ~$11B Ann. Rev | Enterprise platform administration with tenant-level configuration, role-based governance, and audit trails. | ITSM Foundation tier starts at **~$70.00/fulfiller user/month** (annual enterprise contract) | **Personal Developer Instance (PDI)**: Free indefinite access for admins/developers, but instance reclaims after 10 days of inactivity; no production free tier |
| **[Workday Tenant Management](https://www.workday.com/)** | ~$68B Market Cap / ~$8.4B Ann. Rev | HCM and finance tenant administration with enterprise-wide full service equivalent (FSE) workforce governance. | Core HCM starting at **~$8.00/employee/month** ($96/employee/year billed annually with multi-year contract) | **30-day free trial** available specifically for Workday Adaptive Planning; 0-day free trial for core HCM/Financials |
| **[CyberArk Identity](https://www.cyberark.com/)** | ~$17B Market Cap / ~$1.0B Ann. Rev | Workforce identity security platform providing unified SSO, MFA, and automated lifecycle management. | Workforce Identity starting at **~$5.00/user/month** (typically subject to annual contract minimums) | **14-day free trial**: Fully functional evaluation sandbox tenant for up to 50 users |
| **[Okta](https://www.okta.com/)** | ~$14B Market Cap / ~$2.6B Ann. Rev | Enterprise workforce and customer identity platform with multi-tenant organization management. | Workforce Starter: **$6.00/user/month** (annual contract); Single Sign-On: $2.00/user/month | **30-day free trial** for Workforce Identity Cloud with full features; Developer Edition free up to 7,500 monthly active users |
| **[Ping Identity](https://www.pingidentity.com/)** | ~$6.5B Valuation (Acquired by Thoma Bravo) / ~$350M+ Ann. Rev | Enterprise IAM with identity governance, lifecycle management, and directory administration. | PingOne Workforce starting at **$3.00/user/month** (minimum 5,000 user contract commitment) | **30-day free trial**: PingOne trial tenant with complete access to SSO and MFA configurations |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---|---|---|
| **[Keycloak](https://github.com/keycloak/keycloak)** | [![Stars](https://img.shields.io/github/stars/keycloak/keycloak?style=social&color=white)](https://github.com/keycloak/keycloak/stargazers) | **The most widely deployed open-source IAM with proven multi-tenancy.** Apache-2.0, Java/Quarkus. **Realms serve as the foundational isolation unit**—each realm manages its own users, credentials, roles, clients, and authentication policies independently. **One realm per tenant is the recommended pattern** for strongest isolation. Supports OAuth 2.0, OIDC, SAML 2.0, LDAP federation, and SCIM 2.0. |
| **[Authelia](https://github.com/authelia/authelia)** | [![Stars](https://img.shields.io/github/stars/authelia/authelia?style=social&color=white)](https://github.com/authelia/authelia/stargazers) | **Lightweight authentication and authorization server providing 2FA and SSO.** Apache-2.0, Go. Acts as a companion portal for reverse proxies (Nginx, Traefik, Envoy, Caddy) to verify tenant access, multi-factor login (TOTP, WebAuthn/Passkeys, Duo), and header-based remote authentication. |
| **[authentik](https://github.com/goauthentik/authentik)** | [![Stars](https://img.shields.io/github/stars/goauthentik/authentik?style=social&color=white)](https://github.com/goauthentik/authentik/stargazers) | **All-in-one open-source Identity Provider emphasizing flexibility and multi-tenancy.** GPL-3.0, Python/Go. Features built-in tenant isolation, policy flows, stage execution engines, integrated LDAP outpost servers, RADIUS support, and SAML/OAuth2/OIDC provider modes. |
| **[Ory Hydra](https://github.com/ory/hydra)** | [![Stars](https://img.shields.io/github/stars/ory/hydra?style=social&color=white)](https://github.com/ory/hydra/stargazers) | **Hardened OpenID Connect Certified & OAuth 2.0 Authorization Server.** Apache-2.0, Go. Headless engine designed to connect to any existing user database and tenant management backend without taking over user account storage. |
| **[ZITADEL](https://github.com/zitadel/zitadel)** | [![Stars](https://img.shields.io/github/stars/zitadel/zitadel?style=social&color=white)](https://github.com/zitadel/zitadel/stargazers) | **Event-sourced IAM with infrastructure-level tenant isolation.** AGPL-3.0, Go/TypeScript. **Strict multi-tenant hierarchy**: Systems → Organizations → Projects, with isolated data and policy scoping. Every mutation is written as an immutable event for a complete, API-accessible audit trail. |
| **[Casdoor](https://github.com/casdoor/casdoor)** | [![Stars](https://img.shields.io/github/stars/casdoor/casdoor?style=social&color=white)](https://github.com/casdoor/casdoor/stargazers) | **Lightweight Go-based IAM with built-in LDAP and RADIUS servers.** Apache-2.0. **Multi-tenancy via Organizations**—each with independent users, applications, providers, and roles. Single Go binary supporting MySQL, PostgreSQL, SQL Server, Oracle, and SQLite, plus native MCP server for AI agents. |
| **[Ory Kratos](https://github.com/ory/kratos)** | [![Stars](https://img.shields.io/github/stars/ory/kratos?style=social&color=white)](https://github.com/ory/kratos/stargazers) | **API-first identity, user management, and credential provisioning system.** Apache-2.0, Go. Provides cloud-native headless account administration, self-service profile registration, recovery flows, MFA/WebAuthn, and customizable tenant schemas. |
| **[FreeIPA](https://github.com/freeipa/freeipa)** | [![Stars](https://img.shields.io/github/stars/freeipa/freeipa?style=social&color=white)](https://github.com/freeipa/freeipa/stargazers) | **Integrated enterprise domain and directory administration suite for Linux/UNIX.** GPL-3.0, C/Python. Combines 389 Directory Server (LDAP), MIT Kerberos, Dogtag Certificate System, NTP, and DNS for centralized workforce domain administration and cross-realm trust. |
| **[Tesseral](https://github.com/tesseral-labs/tesseral)** | [![Stars](https://img.shields.io/github/stars/tesseral-labs/tesseral?style=social&color=white)](https://github.com/tesseral-labs/tesseral/stargazers) | **Open-source auth infrastructure built specifically for B2B SaaS multi-tenancy.** Apache-2.0 / Commercial. Offers tenant-level self-service config dashboards, customer-delegated SAML/SCIM directory sync without code, and granular RBAC. |
| **[OpenIdentityPlatform OpenAM](https://github.com/OpenIdentityPlatform/OpenAM)** | [![Stars](https://img.shields.io/github/stars/OpenIdentityPlatform/OpenAM?style=social&color=white)](https://github.com/OpenIdentityPlatform/OpenAM/stargazers) | **Community fork of Sun/ForgeRock OpenAM for enterprise access management.** CDDL-1.0, Java. Offers full multi-tenant realm administration, SAML 2.0, OAuth 2.0 / OpenID Connect, centralized access audit logging, and legacy web policy agents. |
| **[WSO2 Identity Server](https://github.com/wso2/product-is)** | [![Stars](https://img.shields.io/github/stars/wso2/product-is?style=social&color=white)](https://github.com/wso2/product-is/stargazers) | **Enterprise-grade open-source customer and workforce IAM.** Apache-2.0, Java. Supports multi-tenancy with tenant domain segregation, identity federation, adaptive authentication, SCIM 2.0 provisioning, and fine-grained authorization. |
| **[Janssen Project](https://github.com/JanssenProject/jans)** | [![Stars](https://img.shields.io/github/stars/JanssenProject/jans?style=social&color=white)](https://github.com/JanssenProject/jans/stargazers) | **High-performance identity platform originating from Gluu Server.** Apache-2.0, Java/Python. Engineered for high concurrency, OAuth 2.0 / OIDC compliance, FAPI security profiles, and enterprise tenant account lifecycle workflows. |
| **[midPoint](https://github.com/Evolveum/midpoint)** | [![Stars](https://img.shields.io/github/stars/Evolveum/midpoint?style=social&color=white)](https://github.com/Evolveum/midpoint/stargazers) | **Comprehensive open-source Identity Governance and Administration (IGA) platform.** Apache-2.0 + EUPL, Java. Full identity provisioning, periodic access certification reviews, role catalog administration, and connectors for AD, LDAP, and cloud endpoints. |
| **[Apache Syncope](https://github.com/apache/syncope)** | [![Stars](https://img.shields.io/github/stars/apache/syncope?style=social&color=white)](https://github.com/apache/syncope/stargazers) | **Open-source digital identity manager for identity provisioning, access governance, and directory synchronization.** Apache-2.0, Java. Manages user lifecycle, role-based provisioning, reporting, and connector integration with enterprise directories. |
| **[LSC (LDAP Synchronization Connector)](https://github.com/lsc-project/lsc)** | [![Stars](https://img.shields.io/github/stars/lsc-project/lsc?style=social&color=white)](https://github.com/lsc-project/lsc/stargazers) | **Mature open-source directory synchronization engine.** BSD-3-Clause, Java. Reads from heterogeneous data sources (RDBMS, LDAP directories, flat files) and transforms/synchronizes identity objects with Active Directory or LDAP endpoints. |

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format and table schemas).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Enterprise account and tenant administration platforms handle authentication credentials and identity data; enforce MFA, least-privilege access, and compliance with applicable regulations (GDPR, SOC 2, HIPAA where relevant). **Tenant isolation failures can expose one customer's data to another.**
- **Open-source IAM has different trade-offs across projects.** **Keycloak's realm-per-tenant model provides the strongest isolation** but management overhead scales with tenant count. **Casdoor is the lightest to operate** (single Go binary) and uniquely offers built-in LDAP/RADIUS servers. **ZITADEL provides the strongest audit trail** through event sourcing. **midPoint is the only open-source option matching commercial IGA** (access reviews, certification, SoD). **Validate tenant isolation requirements, IGA feature needs, and operational capacity** before committing.

---

**Made for identity architects, IT administrators, and organizations building multi-tenant identity infrastructure.**  
Let's make enterprise account and tenant administration more open, isolated, and auditable.
