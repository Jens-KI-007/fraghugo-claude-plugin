# frag.hugo – German GDPR (DSGVO) assistant for Claude

German data protection in Claude: GDPR fines, deadlines, software checks and supervisory authorities, plus breach
reports and access requests filed straight into your frag.hugo account.

This plugin connects Claude to the frag.hugo MCP server (`https://mcp.fraghugo.de/mcp`) and adds three skills that carry
the working method of a German data protection officer (Datenschutzbeauftragter): which questions to ask in which order,
and when to call which tool.

## What you get

**Skills**

| Skill | Use it when |
|---|---|
| `datenpanne-einschaetzen` | A personal data breach happened and you need to know whether and where to report it (Art. 33/34 GDPR, EDPB Guidelines 9/2022, 72-hour deadline, the competent German state authority and its mandatory fields). |
| `betroffenenanfrage-beantworten` | Someone asked for access, erasure, rectification, restriction, portability or objected (Art. 12, 15–22 GDPR): identity check, one-month deadline and extension, exceptions, reply draft. |
| `ki-einsatz-pruefen` | You want to introduce or review an AI tool: GDPR fitness from the frag.hugo DSGVO-Prüfstand, role and risk class under the EU AI Act, prohibited practices, Art. 50 transparency, Art. 4 AI literacy, documentation. |

**Tools without an account:** GDPR fines search, compliance deadlines (GDPR, NIS2/BSIG, AI Act, CRA), software GDPR
check (DSGVO-Prüfstand), subprocessor changes, supervisory authority finder, ransomware picture for Germany, email
security check, website privacy check and vendor profile.

**Tools with a frag.hugo account:** your open privacy deadlines, report a data breach, log a data subject request, plan
the introduction of new software. Writing tools always show a preview first and act only after you confirm. Your appointed
data protection officer is notified to review.

## Installation

In Claude Code:

```
/plugin marketplace add Jens-KI-007/fraghugo-claude-plugin
/plugin install fraghugo@fraghugo
```

Or load it for one session from a local copy: `claude --plugin-dir ./fraghugo-claude-plugin`.

The public tools work right away. For the account tools, run `/mcp`, choose `fraghugo` and sign in with your
frag.hugo account in the browser.

## Limits

The skills and tools give orientation with sources. They are not legal advice for the individual case and they do not
decide for you whether a breach must be reported — that assessment stays with the controller. Nothing is sent to a
supervisory authority or to a data subject by this plugin.

## Privacy Policy

Controller: frag.hugo Informationssicherheit GmbH, Hamburg, Germany — imprint and full privacy policy:
<https://www.fraghugo.de/impressum/> and <https://www.fraghugo.de/datenschutzerklaerung/>. Contact:
support@fraghugo.de.

- **The plugin itself** consists of text files (skills) and the server address. It collects nothing and runs no code on
  your machine.
- **Public tools** (no account): search terms, software names and domains for the email check are processed to answer
  the request and are neither stored nor logged. Rate limiting uses short-lived counters with a hashed IP address,
  discarded after two hours. The email check queries the given domain's DNS from our servers.
- **Website privacy check** (`start_website_check`, and `vendor_profile` when asked to check the website): the URL is sent
  to the frag.hugo scanner, which loads the website like a visitor. As with every Hugo Check, the scanner logs the URL,
  keeps the result available for retrieval, and stores which third-party services it found per domain. For one hour a
  hash of the URL is kept to return the same scan to repeated requests.
- **Account tools:** sign-in uses OAuth with your existing frag.hugo account. We store the token, timestamps, the name of
  the connecting client and your organisation, so that you can see and revoke the connection in the app. Breaches,
  requests and records you create are processed under your existing frag.hugo contract and data processing agreement
  (frag.hugo acts as processor). The log of tool calls holds no free text — only IDs, tool name, time and a checksum of
  the arguments.
- **Your AI provider:** whatever a tool returns is seen by the AI provider you use with Claude (Anthropic). Use a plan
  with a data processing agreement for personal data; the frag.hugo DSGVO-Prüfstand shows which plans qualify.
- Servers: Cloudflare (MCP server), Hetzner in Germany (frag.hugo platform).

## License

MIT — see [LICENSE](LICENSE).
