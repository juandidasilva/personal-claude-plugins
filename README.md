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

From a local clone of this repository, install the plugin using Claude Code's plugin command for a local directory, or add the repository as a plugin marketplace/source according to the current Claude Code documentation.

The plugin manifest is located at `.claude-plugin/plugin.json`, and the subagents are discovered from `agents/*.md`.

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
