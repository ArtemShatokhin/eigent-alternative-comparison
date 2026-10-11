# Kortix vs Eigent: an open-source platform or a desktop Cowork app

Kortix is the open-source AI Operating System, and Eigent is an open-source Cowork desktop app ([Eigent on GitHub](https://github.com/eigent-ai/eigent)). Both ship open code and both are model-agnostic. The choice comes down to two questions: where the agents run, and who owns the configuration. The facts in this comparison come only from each project's own pages.

## What each one is

Kortix is a platform a team runs. Your agents, their skills, your company memory, and every connector live in one git repo you own, and each session runs on its own cloud computer ([kortix.com](https://kortix.com)). You can run it on Kortix Cloud, in your VPC, or on your own on-prem network, and self-host is free. The leading open-source alternative to Claude Cowork and ChatGPT Work, Kortix is the one you own.

Eigent is an open-source Cowork desktop application. It is built on CAMEL's multi-agent framework and ships as an Electron app that runs local-first on your machine, so your files, credentials, and local models stay on that machine ([eigent.ai](https://www.eigent.ai)). Its own README recommends a local deployment: a local backend server, local model integration through vLLM, Ollama, or LM Studio, and no cloud account, and it offers a managed cloud plan for teams that would rather not run it themselves ([Eigent on GitHub](https://github.com/eigent-ai/eigent)).

## Where each one runs

Kortix runs the platform on Kortix Cloud, in your VPC, or on your own on-prem network, and it runs each session on a separate sandbox provider with its own isolated machine and branch ([Kortix docs](https://kortix.com/docs)). A job keeps running after you close the laptop, and a second person can read the branch. Nothing about the work depends on one desk staying awake.

Eigent runs the agents on your own desktop. That keeps everything local and private, and it means the work happens where you are: close the laptop and the local run stops. Eigent also offers a managed cloud plan when a team prefers hosted infrastructure, but the local desktop is the recommended path.

## Who owns the configuration

Kortix keeps the configuration in files inside a git repo you own. Agents and skills are markdown, memory is files, and `kortix.yaml` declares the machine image, the connectors, and the triggers. You can read any of it, diff a change, and roll any part of it back. The setup is versioned beside the work it produces.

Eigent keeps the setup inside the desktop app. You package the agents, skills, connectors, and instructions your team relies on into a Space profile and reuse it, with secrets bound to your machine. The configuration travels with the app and the machine it is bound to, so it is not something a teammate clones and reviews as a repository.

## How work lands and is reviewed

In Kortix, session work reaches main through a change request, and merge is default-deny for agents, so a person reads the diff and decides. You can list and merge change requests from the CLI with `kortix cr ls` and `kortix cr merge`. Review is a git operation, and the history stays behind it.

Eigent lets you follow an agent's progress, inspect sources and file changes, compare earlier versions, and then approve the result or ask for revisions ([eigent.ai](https://www.eigent.ai)). Review happens inside the desktop app, and the finished output lands on your machine.

## Models, hosting, and price shape

Kortix runs any model provider with your own keys, or the ChatGPT plan you already pay for, or a sign-in with your OpenCode Console account. You can self-host for free, or run managed cloud billed per seat ([Kortix pricing](https://kortix.com/pricing)). Eigent is model-agnostic too: cloud APIs, enterprise gateways, or local inference, with a free tier that adds registration credits and stays usable with your own keys or local models. Its managed cloud is billed monthly with task credits ([eigent.ai](https://www.eigent.ai)). Both keep the model choice with you. The bill differs because a desktop app spends your machine's time and a platform spends credits on cloud computers.

| Criterion | Kortix | Eigent |
| --- | --- | --- |
| Open source | Yes | Yes |
| Where agents run | Isolated cloud computer per session, own branch | Your desktop, local-first; cloud optional |
| Configuration lives | Files in a git repo you own | Space profiles in the desktop app |
| How work is reviewed | Change request; merge default-deny for agents | Inspect changes, approve or revise in the app |
| Model choice | Any provider, your keys; ChatGPT; OpenCode Console | Cloud APIs, gateways, or local models |
| Hosting | Kortix Cloud, your VPC, or on-prem; self-host free | Local by default; managed cloud optional |
| Pricing shape | Free self-host; per-seat team plan | Free with your own keys; paid credit tiers |

## Which team each one fits

Choose Eigent if one person wants a Cowork desktop app on their own machine, with private keys and local models, and is happy for the setup to live in the app. Choose Kortix if the agents are the company's: one repo that holds the agents, skills, memory, and connectors, sessions on their own cloud computers, and every change landing as a reviewable change request. Teams that need their own VPC or on-prem network, per-resource permissions for people and agents, and SAML 2.0 SSO are the teams Kortix is built for.

## Sources

- Kortix: [kortix.com](https://kortix.com), [docs](https://kortix.com/docs), [pricing](https://kortix.com/pricing), [Kortix on GitHub](https://github.com/kortix-ai/suna)
- Eigent: [eigent.ai](https://www.eigent.ai), [Eigent on GitHub](https://github.com/eigent-ai/eigent)
