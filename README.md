# Elori MCP — connection and listing guide

Elori helps consultants, sales professionals and small-business teams manage their sales pipeline and meeting workflows. Its hosted MCP server exposes a reviewed action catalog to compatible AI clients, with the user's existing Elori permissions.

**Endpoint:** https://elori.app/mcp  
**Transport:** stateless Streamable HTTP  
**Authentication:** OAuth authorization code with PKCE S256  
**Elori plans:** Director (€30/month) or Autopilot (€100/month). MCP is not included in Assistant.  
**Account requirement:** verified Elori email and an eligible organisation.  
**Support:** support@elori.app  
**Privacy:** https://elori.app/privacy  
**Terms:** https://elori.app/terms

This is a commercial hosted service, not an open-source release of Elori's application. No local package, shared API key or downloaded server is required. A directory listing is not an endorsement by Anthropic or OpenAI.

## Before connecting

1. Create an Elori account, verify its email and complete onboarding.
2. Use an eligible Director or Autopilot organisation.
3. For mail/calendar workflows, connect the desired Google or Microsoft account in Elori's mail/calendar setup. MCP consent does not itself connect a mailbox.
4. Open your Elori account settings and locate the Claude/ChatGPT MCP section. Copy the server URL shown there.
5. Check your AI client's custom-connector availability and workspace policy. Elori eligibility does not grant a Claude or ChatGPT plan.

## How to connect Claude to your sales calendar and pipeline using MCP

In Claude's settings, open **Connectors** and add a custom connector, where available in your plan/workspace. Name it **Elori** and paste:

    https://elori.app/mcp

Follow the OAuth sign-in, review Elori's permission screen and explicitly approve the connection. Start a conversation with a read-only request:

> Show my available Elori actions for pipeline and meetings. Describe the relevant read actions, then summarise my open deals and upcoming meetings. Do not change records, send emails, book meetings or spend money.

Before making a change, ask the assistant to explain the exact action, arguments and consequences. Elori's existing permission, subscription, provider, funding and approval checks still apply.

Claude menus and plan availability can change. Current instructions:
https://support.claude.com/en/articles/11175166-getting-started-with-custom-connectors-using-remote-mcp

### Claude Code alternative

If you already use Claude Code, add the hosted server:

    claude mcp add --transport http elori https://elori.app/mcp

Use Claude Code's MCP management/authentication flow to complete OAuth. Do not paste access tokens into prompts, configuration files or public posts.

## How to connect ChatGPT to your sales pipeline using MCP

Use ChatGPT's custom MCP app/connector setup where your plan and workspace administrator permit it. Enable developer mode if that setup requires it, create a custom app and use **https://elori.app/mcp** as its MCP endpoint. Complete Elori's OAuth consent.

Custom MCP support, especially write actions, depends on ChatGPT's current plan, workspace controls and rollout. Do not assume it is available on every personal plan.

Start with:

> Use Elori to summarise my pipeline and identify deals that need attention. Discover and describe the appropriate actions first. This request is read-only.

Current OpenAI instructions:
https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt

## Practical meeting workflow

After the read-only connection check:

> Help me prepare a meeting campaign based on my Elori business profile. First discover which campaign draft actions are available and describe their required inputs. Explain the proposed draft before executing any change. Do not activate a campaign, contact prospects, book calendar events or accept fees without the required approval.

A connected client can only use actions actually exposed to that user. An MCP connection never overrides a release hold or grants automatic authority to send email or charge a card. Meeting charges and other billing terms remain governed by Elori's billing policy.

## Disconnect

Revoke the connection from Elori's MCP section in account settings. Remove the connector in Claude/ChatGPT too. A revoked connection cannot continue using Elori through its old grant.

## Troubleshooting

- **401 when opening `/mcp`:** unauthenticated POSTs intentionally require OAuth; `/mcp` is not a marketing web page. Non-POST methods return 405.
- **No connection button:** check your Elori plan, verified email and the AI client's workspace permissions.
- **Calendar/mail unavailable:** connect the provider in Elori and inspect the available action's requirements.
- **An action is denied:** existing Elori role, entitlement, approval, provider and safety checks apply. Do not repeatedly retry a write whose outcome is unknown.
- **Directory scanner cannot inspect tools:** use the directory's authenticated review flow. Never provide a real customer's credentials or disable authentication to obtain a badge.

## Verification and publication status

Checked on 10 October 2026:

- Production OAuth protected-resource metadata returned HTTP 200.
- Production OAuth authorization-server metadata returned HTTP 200 and advertises dynamic client registration and PKCE S256.
- An unauthenticated MCP initialization POST returned HTTP 401 with the correct discovery challenge.
- Source inspection found tool titles and read/write annotations for the three MCP tools: `elori_list_actions`, `elori_describe_action` and `elori_execute_action`.

These checks do **not** establish an authenticated production handshake in Claude/ChatGPT, a successful live meeting workflow, directory acceptance or a completed third-party review.

The registry manifest uses **`io.github.elori-debug/mcp`**, matching the verified publishing GitHub account. The public documentation repository is https://github.com/elori-debug/elori-mcp. Official-registry publication is pending its publisher's separate GitHub authorization. Check the registry result before claiming that a version is published. This is a registry identity, not the URL users connect to: the endpoint remains **https://elori.app/mcp**.

This repository contains documentation and metadata only, not Elori's server implementation. It does not claim an open-source license for the hosted service. There is no automatic publishing workflow in this repository.

Community submissions currently awaiting maintainer review:

- TensorBlock MCP Index: https://github.com/TensorBlock/awesome-mcp-servers/pull/3445
- mcpHQ catalog: https://github.com/mcpHQ/awesome-mcp-servers/pull/190

A submitted pull request is not an accepted directory listing. No official Claude or OpenAI directory acceptance is claimed.

Only documentation and public metadata should be uploaded to a launch repository. Do not upload Elori's private application, database contents, environment files, OAuth credentials, reviewer passwords or customer data.
