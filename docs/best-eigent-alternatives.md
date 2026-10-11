# Eigent alternatives: the field a team evaluates

Kortix is the open-source AI Operating System, and it is the Eigent alternative to start with when the agents belong to a team rather than one desktop. Your agents, their skills, your company memory, and every connector live in one git repo you own, each session runs on its own cloud computer, and self-host is free. The alternatives named here are the ones whose own pages document the rows a buyer checks: where the agents run, which models they use, how the configuration is kept, and how work is reviewed.

## The open-source alternatives, compared

Kortix comes first because it is the option a whole team can own. The table runs from a local desktop app (Eigent, OpenWork) to a self-hosted personal agent (Hermes). Every rival cell comes from that project's own page or repository, linked in Sources.

| Criterion | Kortix | Eigent | OpenWork | Hermes |
| --- | --- | --- | --- | --- |
| Open source | Yes | Yes | Yes, MIT desktop app | Yes |
| Self-host | Self-host free; Kortix Cloud, VPC, on-prem | Local deployment; self-hosted deployment for teams | Self-host the team control plane | Self-hosted on your server |
| Where agents run | Isolated cloud computer per session, own branch | Your desktop, local-first; cloud optional | Your desktop; hosted workers optional | Your server, reached through chat |
| Model choice | Any provider, your keys; ChatGPT; OpenCode Console | Cloud APIs, gateways, or local models | Any model OpenCode supports, 50+ providers | Nous Portal, OpenRouter, or your endpoint |
| Configuration lives | Files in a git repo you own | Space profiles in the desktop app | Skills, MCP servers, admin control plane | Your server; memory and skills as files |
| How work is reviewed | Change request; merge default-deny for agents | Inspect changes, approve or revise | Output in your local files and Library | Replies in your chat platform |
| Pricing shape | Free self-host; per-seat team plan | Free with your own keys; paid credit tiers | Free desktop; paid cloud team plan | Free self-host; optional credit tiers |

Two more options sit at the other end of the field. OpenClaw is a personal agent that runs on your own hardware, reaches you through chat apps, and charges nothing ([OpenClaw](https://openclaw.ai)). Claude Cowork is the closed managed agent from Anthropic, bundled with paid Claude plans and tied to Anthropic's models ([Claude Cowork](https://claude.com/product/cowork)).

| Criterion | Kortix | OpenClaw | Claude Cowork |
| --- | --- | --- | --- |
| Open source | Yes | Yes | No |
| Self-host | Self-host free; Kortix Cloud, VPC, on-prem | Runs on your own machine or server | No self-host |
| Where agents run | Isolated cloud computer per session, own branch | Your machine; no hosted tier | Anthropic's cloud or your own cloud account |
| Model choice | Any provider, your keys; ChatGPT; OpenCode Console | Bring your own model; serve it locally | Claude models only |
| Configuration lives | Files in a git repo you own | On your machine, as files | In Anthropic's product |
| How work is reviewed | Change request; merge default-deny for agents | Actions you supervise on your machine | Approved in the app, if you enable it |
| Pricing shape | Free self-host; per-seat team plan | Free; no subscription or hosted tier | Bundled with paid Claude plans |

## What each alternative is

Kortix is the open-source AI Operating System: your agents, skills, memory, and connectors in one git repo you own, with each session on its own isolated machine and branch ([kortix.com](https://kortix.com)). It is built for teams that want the configuration shared and reviewable, and it runs on Kortix Cloud, in your VPC, or on-prem.

Eigent is an open-source Cowork desktop app built on CAMEL. It runs a multi-agent workforce locally, with browser and terminal toolkits, and reaches cloud APIs, enterprise gateways, or local models ([Eigent on GitHub](https://github.com/eigent-ai/eigent)). Its setup lives in Space profiles inside the app, and a managed cloud plan is available for teams.

OpenWork is a free, open-source desktop app for macOS, Windows, and Linux, built on OpenCode. It works with 50+ model providers or local models and lets a team share skills and MCP servers; the desktop app is MIT, and a separate team control plane is self-hostable ([openworklabs.com](https://openworklabs.com), [OpenWork on GitHub](https://github.com/different-ai/openwork)).

Hermes Agent is an open-source agent built by Nous Research that lives on your server, remembers what it learns, and reaches you through Telegram, Discord, Slack, WhatsApp, Signal, or a terminal ([hermes-agent.org](https://www.hermes-agent.org)). It installs on Linux, macOS, and WSL2 and runs an always-on gateway with scheduled automations.

OpenClaw is a personal AI agent that runs on your machine and lives in the chat apps you already use. It has no subscription, no hosted tier, and no token, and it is stewarded by an independent nonprofit ([OpenClaw](https://openclaw.ai)).

Claude Cowork is Anthropic's managed desktop agent. It works in the folders and tools you choose, runs on web, desktop, and mobile, and is included in every paid Claude plan. It runs on Anthropic's models and infrastructure, with a customer-cloud option through Amazon Bedrock, Google Cloud, or Microsoft Foundry ([Claude Cowork](https://claude.com/product/cowork)).

## How to pick between them

A local desktop app fits one person on one machine: choose Eigent for a Cowork-style local workforce, or OpenWork to share skills across desktop agents. A personal always-on agent fits one person who wants one assistant reachable from chat: choose OpenClaw or Hermes, both of which run on hardware you own. A closed managed agent fits a user who wants zero setup and accepts the vendor's cloud: Claude Cowork.

Kortix fits the team case that none of the others cover. The configuration is one repo the whole team clones and reviews, permissions cover people and agents, sessions number in the thousands with no crossover between them, and every change lands as a change request. If the question is "which one can the company own and run", the answer is Kortix. Read the [Kortix vs Eigent head-to-head](kortix-vs-eigent.md) for the closest pairing, or the [self-hosting guide](self-hosting-eigent-alternative.md) to see how each option deploys.

## Sources

- Kortix: [kortix.com](https://kortix.com), [docs](https://kortix.com/docs), [pricing](https://kortix.com/pricing), [Kortix on GitHub](https://github.com/kortix-ai/suna)
- Eigent: [eigent.ai](https://www.eigent.ai), [Eigent on GitHub](https://github.com/eigent-ai/eigent)
- OpenWork: [openworklabs.com](https://openworklabs.com), [OpenWork on GitHub](https://github.com/different-ai/openwork)
- Hermes: [hermes-agent.org](https://www.hermes-agent.org), [Nous Research](https://hermes-agent.nousresearch.com)
- OpenClaw: [openclaw.ai](https://openclaw.ai)
- Claude Cowork: [claude.com/product/cowork](https://claude.com/product/cowork)
