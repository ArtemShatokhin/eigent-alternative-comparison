# Eigent pricing and license, and the open-source alternative

Kortix is the open-source AI Operating System, self-host is free, and managed cloud is billed per seat. Eigent's costs and license come from Eigent's own pages, and the two sit side by side because a team's choice between a desktop Cowork app and a platform it owns usually comes down to the bill and the deployment. Prices and plans change, so each figure is dated where it appears.

## Eigent's license

Eigent's repository is licensed under the Apache License 2.0 ([Eigent on GitHub](https://github.com/eigent-ai/eigent)). That license lets you download, inspect, and modify the code, and Eigent's own README says the project is open source from day one. Kortix is open source in the same practical sense: you can read the code, fork it, and audit it. Both are open source, so the license is not what separates them. The separation is where the agents run and who owns the configuration.

## Eigent's pricing

Eigent is free when you bring your own model keys or run a local model, and its managed cloud is billed monthly with task credits ([eigent.ai](https://www.eigent.ai)). The plans, checked October 2026:

- Free: a new-user bonus of 1,000 registration credits and 500 credits for each successful invite, with BYOK and local models to use Eigent at no plan cost. The page lists 16 supported models.
- $19.99 per month: $0 today, then $19.99 per month after a 7-day free trial, with 2,000 task credits a month, priority email support, and a trial limit of 300 credits a day.
- $99.99 per month: 10,000 task credits a month and high-priority support.
- Enterprise: custom local deployment, custom features and integrations, and invoice or purchase-order billing.

Eigent also states that SOC 2 readiness and GDPR compliance work remain in progress ([eigent.ai](https://www.eigent.ai)).

## Kortix's pricing

Kortix quotes its own plans on its pricing page, checked October 2026 ([Kortix pricing](https://kortix.com/pricing)). Free includes 200 credits each month for sandbox compute and 1 project, and you bring your own API key or connect your ChatGPT subscription for premium access. The team plan is $40 per seat per month and includes 2,500 pooled credits per seat, optional managed model access, and seats for the people on your team. Agent Computer runtime and managed model token usage draw from that same pool, and you top up only when the pooled balance runs out. Everything in Team plus SAML SSO, SCIM directory sync, advanced RBAC, audit logs, an SLA and DPA, and Cloud, VPC, or on-prem deployment sits in Enterprise. Self-host is free.

Kortix holds SOC 2 Type I, and SOC 2 Type II is in progress ([Kortix on GitHub](https://github.com/kortix-ai/suna)).

## Eigent and Kortix side by side

Kortix comes first because it is the option a team can self-host and own.

| Criterion | Kortix | Eigent |
| --- | --- | --- |
| Open source | Yes | Yes |
| Licence | Open source; read, fork, and audit | Apache 2.0 |
| Free tier | Free is $0; 200 credits a month, 1 project | Free with BYOK or local models; signup credits |
| Paid plans | $40 per seat per month; 2,500 pooled credits per seat | About $19.99 and $99.99 per month in task credits |
| Self-host cost | Free | Free; run it locally |
| Model cost | Your keys; ChatGPT; optional managed models | Your keys, gateways, or local models |
| Enterprise | SAML, SCIM, RBAC, audit logs, SLA, on-prem | Custom deployment, features, invoice billing |

## What the numbers mean for a team

Eigent's free tier and its per-month credit plans suit one person who runs agents locally and brings their own keys, and its credits cap how much managed cloud work one account can do each month. Kortix self-hosts free, so a team can run the whole platform on its own box and pay only for the models it chooses, or use managed cloud billed per seat with pooled credits that the whole team shares. The two bills are not the same shape: Eigent sells a desktop app with optional cloud credits, and Kortix sells seats on a platform the company can also run itself. Confirm both on each vendor's pricing page before you commit, because plans and prices move.

## Sources

- Kortix pricing: [kortix.com/pricing](https://kortix.com/pricing), [Kortix on GitHub](https://github.com/kortix-ai/suna)
- Eigent pricing and license: [eigent.ai](https://www.eigent.ai), [Eigent on GitHub](https://github.com/eigent-ai/eigent)
