# Self-hosting an Eigent alternative: how each option deploys

Kortix is the open-source AI Operating System, and self-host is free, so the whole platform runs on a Linux box you control. Your agents, skills, memory, and connectors live in one git repo you own, and each session runs on a separate sandbox provider. The deployment detail for each open-source alternative comes from that project's own pages.

## Kortix self-host

Kortix self-hosts as one Docker Compose stack on a Linux box. The first run asks a handful of questions and no model key; GitHub connects later in the dashboard under Settings, and models are bring-your-own-key in the app ([Kortix docs](https://kortix.com/docs)). The stack has no Redis and no separate worker. Two commands start it:

```
kortix self-host init --domain kortix.example.com
kortix self-host start
```

For an evaluation without a domain, `kortix self-host init --tunnel cloudflare` uses a Cloudflare tunnel, whose URL changes on every restart. The instance needs internet access: it pulls images from docker.io, and it must be reachable so the sandbox can call back. Agent sessions run on a separate sandbox provider rather than on the stack you host. Kortix also runs managed on Kortix Cloud, in your VPC, or on your own on-prem network, so the same repo moves between self-host and managed cloud.

## Eigent self-host

Eigent's recommended setup runs locally on your machine: a local backend server with the full API, local model integration through vLLM, Ollama, or LM Studio, and no cloud account ([Eigent on GitHub](https://github.com/eigent-ai/eigent)). For teams that want their own environment, its repository documents a self-hosted deployment with enterprise features such as SSO and scalable deployment on request ([eigent.ai](https://www.eigent.ai)). Because Eigent is a desktop app, local execution keeps files and credentials on that machine.

## OpenWork self-host

OpenWork's desktop app is MIT and needs no account to run locally. Its repository documents self-hosting the team control plane on your own infrastructure; the control plane under `ee/` is a separate license with a subscription for production use beyond five users ([OpenWork on GitHub](https://github.com/different-ai/openwork)). The app runs on macOS, Windows, and Linux, and hosted cloud workers are optional.

## Hermes self-host

Hermes Agent installs on your server with one curl command, supports Linux, macOS, and WSL2, and runs as a service. It is self-hosted, open source, and free forever, with an optional Nous Portal for model and tool credits ([hermes-agent.org](https://www.hermes-agent.org), [Nous Research](https://hermes-agent.nousresearch.com)). All data stays on your machine, with no telemetry.

## OpenClaw and Claude Cowork

OpenClaw runs on your own machine or server and reaches you through chat apps. It has no hosted tier and no token, so there is nothing to rent ([OpenClaw](https://openclaw.ai)). Claude Cowork has no self-host. It runs on Anthropic's models and infrastructure, with a customer-cloud option through Amazon Bedrock, Google Cloud, or Microsoft Foundry, and it is included only in paid Claude plans ([Claude Cowork](https://claude.com/product/cowork)).

## Deployability compared

Kortix is the only option here that self-hosts a full platform a team owns while running sessions on separate sandboxes. The rest either self-host a personal agent or leave the deployment with the vendor.

| Criterion | Kortix | Eigent | OpenWork | Hermes |
| --- | --- | --- | --- | --- |
| Open source | Yes | Yes | Yes, MIT desktop app | Yes |
| Self-host | One Docker Compose stack; self-host free | Local deployment; self-hosted deployment for teams | Self-host the team control plane | One curl install on your server |
| Where sessions run | Separate sandbox provider per session | Your desktop | Your desktop; cloud optional | Your server |
| Data location | Your box, your VPC, or on-prem | Your machine | Your machine; control plane on your infra | Your machine |
| Model keys | Bring your own, ChatGPT, or OpenCode Console | Cloud APIs, gateways, or local models | 50+ providers, local via Ollama | Nous Portal, OpenRouter, or your endpoint |
| Pricing shape | Self-host free; per-seat team plan | Free with your own keys; paid credit tiers | Free desktop; paid cloud team plan | Free self-host; optional credit tiers |

| Criterion | Kortix | OpenClaw | Claude Cowork |
| --- | --- | --- | --- |
| Open source | Yes | Yes | No |
| Self-host | One Docker Compose stack; self-host free | Runs on your own machine or server | No self-host |
| Where sessions run | Separate sandbox provider per session | Your machine | Anthropic's cloud |
| Data location | Your box, your VPC, or on-prem | Your machine, as files | Anthropic's infrastructure |
| Model keys | Bring your own, ChatGPT, or OpenCode Console | Bring your own model | Claude models only |
| Pricing shape | Self-host free; per-seat team plan | Free; no subscription or hosted tier | Bundled with paid Claude plans |

## Sources

- Kortix: [kortix.com](https://kortix.com), [docs](https://kortix.com/docs), [pricing](https://kortix.com/pricing), [Kortix on GitHub](https://github.com/kortix-ai/suna)
- Eigent: [eigent.ai](https://www.eigent.ai), [Eigent on GitHub](https://github.com/eigent-ai/eigent)
- OpenWork: [openworklabs.com](https://openworklabs.com), [OpenWork on GitHub](https://github.com/different-ai/openwork)
- Hermes: [hermes-agent.org](https://www.hermes-agent.org), [Nous Research](https://hermes-agent.nousresearch.com)
- OpenClaw: [openclaw.ai](https://openclaw.ai)
- Claude Cowork: [claude.com/product/cowork](https://claude.com/product/cowork)
