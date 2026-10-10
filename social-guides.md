# Publiceringsklara MCP-guider

Status: **utkast, inte publicerade**. Ingen extern postning eller katalogregistrering har genomförts. Anpassa länkar till den publicerade MCP-guiden när den finns. Säg inte att Claude/ChatGPT har verifierats i produktion förrän motsvarande klienttest faktiskt har passerat.

## LinkedIn — English

### How to connect Claude to your sales calendar and pipeline using MCP

Your sales context should not have to be copied into every new AI conversation.

Elori offers a hosted MCP connection for accessing your pipeline and meeting workflows from a compatible AI client.

Here is the setup:

1. Create and verify your Elori account. MCP access requires Director (€30/month) or Autopilot (€100/month).
2. Connect Google or Microsoft in Elori if you want to use mail/calendar workflows.
3. In Claude's connector settings, add a custom connector named Elori:
   https://elori.app/mcp
4. Complete OAuth and review the permissions.
5. Start read-only: “Summarise my open deals and upcoming meetings. Do not change anything.”

Then ask for help preparing a meeting campaign. Discover the available actions first; sending messages, changing records and booking meetings still follow Elori's permissions and required approvals.

Custom connector availability depends on your Claude plan and workspace. This is our product, and it is a commercial service—not a free or open-source server.

For consultants and small teams, the practical benefit is working with your actual sales context rather than another pasted spreadsheet.

Start here:
https://elori.app/?utm_source=linkedin&utm_medium=organic_social&utm_campaign=mcp_launch

What would you want your sales assistant to do first: review the pipeline, prepare follow-ups or help organise meetings?

## LinkedIn — svenska

### Så kopplar du Claude till din säljpipeline och kalender med MCP

Du ska inte behöva klistra in din säljpipeline i varje ny AI-konversation.

Med Eloris MCP-anslutning kan en kompatibel AI-assistent använda din säljinformation med de behörigheter du redan har i Elori.

Så kommer du igång:

1. Skapa och verifiera ditt Elori-konto. MCP ingår i Director (30 €/månad) och Autopilot (100 €/månad).
2. Koppla Google eller Microsoft i Elori för mejl- och kalenderfunktioner.
3. Lägg till en egen anslutning i Claude med adressen https://elori.app/mcp.
4. Logga in och godkänn behörigheterna.
5. Börja med: ”Sammanfatta mina öppna affärer och kommande möten. Ändra ingenting.”

Be sedan om hjälp att förbereda en möteskampanj. Utskick, bokningar och andra ändringar följer fortfarande Eloris behörigheter och godkännanden. Din Claude-plan och organisation måste också stödja egna anslutningar.

Vi utvecklar Elori; det här är en kommersiell tjänst.

https://elori.app/?utm_source=linkedin&utm_medium=organic_social&utm_campaign=mcp_launch_sv

Vilken del av din försäljningsadministration skulle du helst vilja sköta direkt från din AI-assistent?

## X — four-post thread

1/4
How to connect Claude to your sales pipeline using MCP:
Add Elori's hosted endpoint: https://elori.app/mcp
OAuth connects your Elori permissions—not a shared API key.
Disclosure: this is our product.

2/4
Before connecting: verify your Elori email and use Director (€30/month) or Autopilot (€100/month).
Connect Google/Microsoft in Elori for mail/calendar workflows.
Your AI client's plan/workspace must support custom MCP connections.

3/4
First prompt:
“Summarise my open deals and upcoming meetings. Discover the relevant read actions first. Do not change anything.”
Then prepare campaign drafts. Sending, booking and paid actions still require the applicable approvals.

4/4
MCP brings your sales context into a compatible AI conversation. It does not bypass permissions or give every AI client the same features.
Explore Elori:
https://elori.app/?utm_source=x&utm_medium=organic_social&utm_campaign=mcp_launch

## Reddit — r/ClaudeAI draft

### How to connect Claude to your sales calendar and pipeline using MCP

Disclosure: this is our product, Elori, a commercial sales workspace. This is a practical setup guide, not an independent recommendation.

If you want Claude to work with CRM context without pasting records into each conversation:

1. Verify your Elori account and use Director (€30/month) or Autopilot (€100/month). MCP is not available on Assistant.
2. Connect your Google/Microsoft account inside Elori for the mail/calendar workflows you intend to use.
3. Add https://elori.app/mcp as a custom connector in Claude, where your plan/workspace allows it.
4. Complete OAuth and review the consent screen.
5. Start with a read-only request: “Discover the Elori pipeline and meeting actions, describe their inputs, then summarise my open deals. Do not modify anything.”

The server exposes discovery, action-description and action-execution tools. Catalogue visibility is not permission to execute everything: your Elori role, plan and required approvals still apply. A mailbox connection is separate from MCP consent.

For meeting campaigns, ask for a proposed draft before any activation. Do not let a prompt silently approve outreach, calendar writes or fees.

If a connection is denied, check verified email, Elori plan, client availability and workspace policy. Revocation is available in Elori's MCP settings.

Product:
https://elori.app/?utm_source=reddit&utm_medium=community&utm_campaign=mcp_launch_claude

What would make this safer or more useful for your workflow?

**Posting gate:** Check the current r/ClaudeAI rules and approved showcase/promotion threads. Obtain moderator approval if required. Do not repost repeatedly or present an affiliated product as an independent discovery.

## Reddit — r/ChatGPTCoding technical draft

### An OAuth MCP pattern for CRM workflows: discover, describe, then execute

Disclosure: this is our product, Elori. We are sharing a connector-design pattern, not claiming that our application source is open-source.

Our hosted sales MCP interface uses three tools:

- `elori_list_actions`: discover the reviewed action catalogue.
- `elori_describe_action`: inspect a specific action's argument schema and policy requirements.
- `elori_execute_action`: invoke an explicitly named action with its described arguments.

The important design choice is that discovery does not grant authority. An execution still goes through the user's current organisation, role, subscription, provider and required approval checks. MCP OAuth consent also does not connect a Google/Microsoft mailbox.

For a first client request, use a read-only pipeline summary. For a write, discover the action, describe the inputs, confirm the intended change, then execute only when applicable approvals allow it. Never blindly retry a write after a timeout with an unknown outcome.

Endpoint: https://elori.app/mcp
Transport: Streamable HTTP
Authentication: OAuth authorization code with PKCE S256
Elori access: Director or Autopilot; ChatGPT custom MCP availability depends on plan/workspace policy.

How are you modelling the boundary between tool discovery and execution authority in your own MCP projects?

**Posting gate:** This community focuses on coding. Do not post a generic sales promotion here. Only use this technical draft if current rules allow affiliated project discussions; otherwise request moderator permission or use an approved showcase thread.

## Praktisk publiceringsordning

1. Verifiera anslutningen i den klient som guiden avser innan du påstår att den har testats.
2. Publicera en offentlig installationsguide och registrera i relevanta kostnadsfria kataloger.
3. Publicera LinkedIn-guiden.
4. Publicera X-tråden med ett eget, verkligt exempel utan kunddata.
5. Använd Reddit endast där moderatorer/regler tillåter innehållet. Anpassa varje post till communityn.
6. Besvara frågor sakligt. Undvik identiska massinlägg, falska rekommendationer och påhittade resultat.

## Mätning utan löften

60–70 nya användare är ett mål, inte ett garanterat utfall. Vid exempelvis 5 % registreringsgrad behövs cirka 1 200–1 400 kvalificerade webbplatsbesök. Det är en räkneillustration, inte en prognos.

Använd UTM-länkar till webbplatsen, inte till OAuth/MCP-endpointen. Följ besök, faktiskt skapade konton (`sign_up`), slutförd onboarding och betalda abonnemang separat. Besök på `/meetings` är inte i sig ett nytt konto.
