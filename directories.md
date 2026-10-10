# MCP directory submission checklist

Researched: 10 October 2026. “Prepared” is not “submitted”, “approved” or “published”. Save the submission receipt and final listing URL when each status changes. Do not submit duplicate entries. Social posts have not been published.

| Destination | Submission route | Current status / requirements |
| --- | --- | --- |
| Official MCP Registry | https://modelcontextprotocol.io/registry/remote-servers | Manifest prepared as `io.github.elori-debug/mcp`, using the verified GitHub owner and OIDC publication. Publication receipt pending. Registry publication is separate from a Claude directory listing. |
| Anthropic / Claude Connectors Directory | https://claude.ai/directory/manage | Not submitted. Paid Claude account with submission access, review of directory terms, listing assets, reviewer test account and successful testing of each tool in Claude required. |
| OpenAI directory | https://platform.openai.com/plugins | Not submitted. Current official flow requires a plugin package, verified publishing identity, MCP review and client tests; a bare registry entry does not create a ChatGPT directory listing. |
| Glama remote connectors | https://glama.ai/mcp/connectors | Not submitted. Use Add Server and complete its registration/review. Do not invent a connector badge URL before approval. |
| Smithery | https://smithery.ai/new | Not submitted. Supports hosted Streamable HTTP, but its current URL-publishing docs use Client ID Metadata Documents. Elori currently uses dynamic client registration, not CIMD; compatibility requires verification before claiming support. |
| Awesome MCP Servers / mcpservers.org | https://mcpservers.org/submit | Free queue available; page states review within two weeks. Choose Free, remote connections, Productivity/Marketing as appropriate and support@elori.app. Direct form access from this environment returned 403, so no submission was attempted. Never choose the $39 paid option without approval. |
| MCP Market | https://mcpmarket.com/submit | Free Queue available; page quotes average 4–6 weeks, not a guarantee. Select Remote MCP and Free Queue. Not submitted. Do not choose the $29 option without approval. |
| MCP.so | https://mcp.so/submit?type=server | Current fetched form advertises a $39 paid submission. Excluded from paid submission unless the owner approves or a verified free route is available. |
| PulseMCP | https://www.pulsemcp.com/submit | Submissions and listing changes are paused. Their page recommends publishing to the Official MCP Registry first for later ingestion. Not submitted. |
| punkpeye/awesome-remote-mcp-servers | https://github.com/punkpeye/awesome-remote-mcp-servers | Not currently eligible under published guidelines: requires an existing Glama badge and an initialize handshake that does not fail behind a paywall. Elori's MCP is restricted to Director/Autopilot. Do not bypass paid-plan gating for a listing. |
| punkpeye/awesome-mcp-servers | https://github.com/punkpeye/awesome-mcp-servers | Not applicable to Elori's remote-only service: contributing guide requires an installable public repository and refers remote-only servers to its remote list. |
| modelcontextprotocol/servers | https://github.com/modelcontextprotocol/servers | Not an open commercial listing target. Current README directs listings to the Official MCP Registry; this repository maintains reference implementations. |
| appcypher/awesome-mcp-servers | https://github.com/appcypher/awesome-mcp-servers | Archived; no PR submitted. Readable contribution rules do not mean a repository is still accepting submissions. |

## Shared listing fields

- Name: **Elori**
- Endpoint: **https://elori.app/mcp**
- Website: **https://elori.app**
- Transport: **Streamable HTTP**
- Authentication: **OAuth 2.0 / authorization code / PKCE S256**
- Support: **support@elori.app**
- Privacy: **https://elori.app/privacy**
- Terms: **https://elori.app/terms**
- Icon candidate: **https://elori.app/assets/elori-icon.webp**; use the required dimensions/file type for each portal.
- Categories: **CRM, Sales, Productivity, Meeting workflows**
- Short description: **Manage your sales pipeline, contacts and meeting workflows through an authenticated Elori connection.**
- Prerequisites: verified Elori email, Director or Autopilot, and a compatible client's eligible plan/workspace.
- Public documentation URL: **https://github.com/elori-debug/elori-mcp**. This is a documentation-only repository, not a release of the application source. `/how-it-works` is general product documentation, not a substitute for a complete MCP setup guide.

### Longer description

Elori provides a hosted MCP server for sales professionals, consultants and small-business teams. Connect a compatible AI client using OAuth to discover approved actions, inspect their schemas and work with your Elori pipeline, contacts and meeting workflows. Requests use the signed-in user's existing Elori organisation and permissions; they cannot bypass subscription, provider, financial or safety approvals. Mail and calendar access is connected separately through Google or Microsoft in Elori. MCP access is included in Director and Autopilot. No local server installation is required.

## GitHub submission policy

Prepare a documentation-only public repository first, with this README and the registry manifest. Do not make the existing Elori application repository public.

For any community repository, read its current contribution rules before opening a PR or issue. Respect category, commercial-service, authentication, handshake and badge requirements. A PR is not a published listing; record the PR URL and wait for acceptance. Do not claim eligibility or create a fake badge.

## Sources

- Official remote manifest: https://modelcontextprotocol.io/registry/remote-servers
- Registry authentication: https://modelcontextprotocol.io/registry/authentication
- Claude submission requirements: https://claude.com/docs/connectors/building/submission
- OpenAI submission flow: https://developers.openai.com/plugins/deploy/submission
- Smithery URL publication: https://smithery.ai/docs/build/publish
- Remote-list rules: https://github.com/punkpeye/awesome-remote-mcp-servers/blob/main/CONTRIBUTING.md
- Local-list scope: https://github.com/punkpeye/awesome-mcp-servers/blob/main/CONTRIBUTING.md
- Official reference-server scope: https://github.com/modelcontextprotocol/servers
