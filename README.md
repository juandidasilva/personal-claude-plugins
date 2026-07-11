# Apartment Buyer Research — Claude Code Plugin

Multi-agent toolkit for investigating an apartment purchase before reserving, negotiating, or signing.

## Included agents

- `apartment-research-coordinator`: delegates and consolidates the full investigation.
- `family-fit-analyst`: layout, daily use, accessibility, and long-term household fit.
- `urban-connectivity-analyst`: travel times, public transport, walkability, and car dependence.
- `neighborhood-quality-analyst`: safety, noise, services, flooding, and urban change.
- `market-valuation-analyst`: comparable properties, price range, and negotiation.
- `mortgage-financial-analyst`: full acquisition cost, monthly cost, and stress scenarios.
- `property-technical-inspector`: defects, repairs, and on-site inspection plan.
- `building-copropiedad-auditor`: building finances, maintenance, and special-assessment risk.
- `real-estate-legal-analyst`: documentary and legal due diligence.
- `resale-rental-analyst`: resale liquidity, rental demand, and exit options.
- `apartment-devils-advocate`: adversarial review of the purchase thesis.

## Installation in Claude Code

Add this repository as a plugin marketplace and install the plugin:

```
/plugin marketplace add juandidasilva/personal-claude-plugins
/plugin install apartment-buyer-research@personal-claude-plugins
```

For local development, launch Claude Code pointing at a clone of this repository:

```
claude --plugin-dir /path/to/personal-claude-plugins
```

The plugin manifest is located at `.claude-plugin/plugin.json`, and the subagents are discovered from `agents/*.md`.

## Defaults and conventions

- **Jurisdiction**: agents default to Uruguay (UI, ITP, escribano, propiedad horizontal / Ley 10.751, gastos comunes) and adapt automatically when the property is clearly in another country.
- **Common report format**: every specialist returns the same structure — executive summary, evidence reviewed, findings, red flags, missing information, financial impact, a 0–10 score, a recommendation (advance / advance only if negotiated / investigate more / reject), and a confidence level — so reports are comparable and easy to consolidate.
- **Language**: agent prompts are in English; agents respond in the language of your conversation.

## Suggested use

Ask Claude to use `apartment-research-coordinator` and provide:

- Property listing URL or description
- Exact or approximate address
- Asking price and currency
- Interior, balcony/terrace, garage, and total areas
- Common expenses and taxes
- Building age and floor
- Photos, plans, meeting minutes, regulations, and known repairs
- Household requirements
- Available cash, financing assumptions, and acceptable monthly cost
- Important destinations for connectivity analysis

Example:

> Use the apartment research coordinator to evaluate this property. Delegate all relevant specialists, identify hard-stop risks, estimate the true purchase and monthly cost, propose a negotiation range, and give me a final advance/negotiate/reject recommendation.

## Safety and professional review

The agents organize research and surface risks. They do not replace an on-site inspection, appraisal, title study, notarial or legal advice, mortgage approval, or licensed financial advice.
