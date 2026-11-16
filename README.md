# Awesome Deception [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of cyber deception resources: honeytokens, canary tokens, honeypots, frameworks, government guidance, research, and the newest frontier, deception for AI agents and MCP.

Deception is the one detection that doesn't need to recognise the attacker. Nothing legitimate touches a decoy, so any use is a high-confidence signal, whether the intruder is a person, a script or an AI agent.

Maintained by [FalseTrail](https://falsetrail.com/). Every link was checked when added; pull requests welcome (see [Contributing](#contributing)).

## Contents

- [Frameworks and standards](#frameworks-and-standards)
- [Government guidance](#government-guidance)
- [Open-source tools](#open-source-tools)
- [Canary token services](#canary-token-services)
- [Commercial platforms](#commercial-platforms)
- [Honeytoken placement](#honeytoken-placement)
- [Deception for AI agents and MCP](#deception-for-ai-agents-and-mcp)
- [AI agent and MCP security](#ai-agent-and-mcp-security)
- [Incidents where decoys mattered](#incidents-where-decoys-mattered)
- [Research](#research)
- [Datasets](#datasets)

## Frameworks and standards

- [MITRE Engage](https://github.com/mitre/engage) - Framework for adversary engagement, deception and denial; activities are mapped to ATT&CK.
- [MITRE D3FEND, Deceive tactic](https://d3fend.mitre.org/tactic/d3f:Deceive/) - Defensive techniques such as Decoy File, Decoy User Credential and Decoy Network Resource.
- [MITRE ATT&CK, T1552 Unsecured Credentials](https://attack.mitre.org/techniques/T1552/) - The technique family most decoy credentials are built to catch.
- [MITRE ATLAS](https://atlas.mitre.org/) - Adversary tactics and techniques against AI systems.
- [NIST SP 800-53 Rev. 5](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) - Controls SC-26 Decoys and SC-30 Concealment and Misdirection.
- [NIST SP 800-160 Vol. 2 Rev. 1](https://doi.org/10.6028/NIST.SP.800-160v2r1) - Cyber-resilient systems engineering, including deception and dynamic positioning.

## Government guidance

- [CISA, Using Cyber Decoys to Strengthen Detection and Response](https://www.cisa.gov/resources-tools/resources/using-cyber-decoys-strengthen-detection-and-response) - September 2026 guidance for critical infrastructure: objectives, placement, alerting, testing and tuning.
- [CISA announcement of the decoy guidance](https://www.cisa.gov/news-events/news/new-cisa-guidance-helps-critical-infrastructure-detect-observe-and-impede-malicious-cyber-activity) - Summary of the above.
- [Careful Adoption of Agentic AI Services](https://www.ncsc.govt.nz/protect-your-organisation/careful-adoption-of-agentic-ai-services/) - Joint guidance from CISA, NSA and Five Eyes partners on deploying AI agents (May 2026).

## Open-source tools

- [decoy-kit](https://github.com/falsetrailhq/decoy-kit) - Inert decoy files (.env, kubeconfig, MCP config, git and npm credentials, SSH config) that alert on a domain you control.
- [OpenCanary](https://github.com/thinkst/opencanary) - Lightweight network service honeypot from Thinkst.
- [Canarytokens (self-hosted)](https://github.com/thinkst/canarytokens-docker) - Docker setup for running your own Canarytokens server.
- [T-Pot](https://github.com/telekom-security/tpotce) - Multi-honeypot platform from Deutsche Telekom Security.

## Canary token services

- [Canarytokens.org](https://canarytokens.org/) - Free hosted tokens from Thinkst; [documentation of token types](https://docs.canarytokens.org/guide/).
- [Tracebit Community Edition](https://tracebit.com/community-edition) - Free decoy credentials and an MIT-licensed CLI.
- [GitGuardian Honeytoken](https://www.gitguardian.com/honeytoken) - Decoy AWS keys and kubeconfigs for the software supply chain; [token types](https://docs.gitguardian.com/honeytoken/honeytoken-types).
- [Microsoft Defender for Identity honeytoken accounts](https://learn.microsoft.com/en-us/defender-for-identity/entity-tags) - Tag dormant AD accounts and devices as honeytokens.

## Commercial platforms

- [Acalvio ShadowPlex](https://www.acalvio.com/shadowplex-platform/) - Deception platform across IT, OT and cloud.
- [FalseTrail](https://falsetrail.com/) - Customer-hosted deception for AI-driven attacks; follows the trail after the first decoy is used.
- [FortiDeceptor](https://www.fortinet.com/products/fortideceptor) - Fortinet's deception appliance, integrated with the Fortinet Security Fabric.
- [Thinkst Canary](https://docs.canary.tools/guide/terminology) - Canary devices and tokens managed from a hosted console.

## Honeytoken placement

- [Lenny Zeltser, Plant Honeytokens to Detect Intrusions](https://zeltser.com/plant-honeytokens) - Where to plant them and how to keep them believable.
- [Sean Metcalf, Kerberoast service account honeypot](https://adsecurity.org/?p=3513) - The classic Active Directory decoy.
- [Honeytoken examples mapped to ATT&CK](https://falsetrail.com/guides/honeytoken-examples/) - 34 concrete placements with the technique each one catches.
- [Thinkst, A safety net for AWS Canarytokens](https://blog.thinkst.com/2022/02/a-safety-net-for-aws-canarytokens.html) - On fingerprinting of public canary keys and how Thinkst responded.
- [Truffle Security, Canaries](https://trufflesecurity.com/canaries) - How scanners recognise keys from public canary services.

## Deception for AI agents and MCP

- [Thinkst, One for all the models out there](https://blog.thinkst.com/2026/06/one-for-all-the-models-out-there.html) - The Canarytokens MCP configuration token (June 2026).
- [Canarytokens MCP token docs](https://docs.canarytokens.org/guide/mcp-token)
- [Lenny Zeltser, A decoy MCP server as a honeypot](https://zeltser.com/decoy-mcp-server-honeypot) - Using an MCP server as a tripwire.
- [Acalvio, Deception Guardrails for AI agents](https://www.acalvio.com/press-releases/acalvio-unveils-deception-guardrails-to-secure-ai-agents/) - Vendor announcement (July 2026).
- [MCP servers as decoys](https://falsetrail.com/guides/mcp-server-decoys/) - Why a decoy MCP entry is a high-signal placement.

## AI agent and MCP security

- [MCP specification, security best practices](https://modelcontextprotocol.io/specification/latest/basic/security_best_practices) - Confused deputy, token passthrough, SSRF, session hijacking.
- [MCP authorization specification](https://modelcontextprotocol.io/specification/2025-11-25/basic/authorization) - OAuth 2.1 with audience-bound tokens.
- [OWASP Top 10 for LLM Applications 2025](https://genai.owasp.org/llm-top-10/) - Including LLM01 Prompt Injection and LLM06 Excessive Agency.
- [OWASP GenAI Security Project](https://genai.owasp.org/) - Home of the Top 10 for Agentic Applications for 2026.
- [Simon Willison, The lethal trifecta for AI agents](https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/) - Private data, untrusted content and external communication.
- [Invariant Labs, MCP tool poisoning attacks](https://invariantlabs.ai/blog/mcp-security-notification-tool-poisoning-attacks)
- [Invariant Labs, GitHub MCP exploited](https://invariantlabs.ai/blog/mcp-github-vulnerability) - Prompt injection through an issue leaks private repositories.
- [Microsoft, Understanding and mitigating security risks in MCP implementations](https://techcommunity.microsoft.com/blog/microsoft-security-blog/understanding-and-mitigating-security-risks-in-mcp-implementations/4404667)
- [Cloud Security Alliance, MAESTRO](https://cloudsecurityalliance.org/blog/2025/02/06/agentic-ai-threat-modeling-framework-maestro) - Threat modeling for agentic AI.
- [CoSAI, Principles for Secure-by-Design Agentic Systems](https://www.coalitionforsecureai.org/announcing-the-cosai-principles-for-secure-by-design-agentic-systems/)
- [AI agent security guide](https://falsetrail.com/guides/ai-agent-security/) - OWASP ASI01-ASI10, ATLAS, incidents and 11 controls.

## Incidents where decoys mattered

- [Grafana Labs, Canary tokens at Grafana Labs](https://grafana.com/blog/2025/08/25/canary-tokens-learn-all-about-the-unsung-heroes-of-security-at-grafana-labs) - A decoy key in CI secrets fired and the intrusion was contained within minutes.
- [Anthropic, Disrupting the first reported AI-orchestrated cyber espionage campaign](https://www.anthropic.com/news/disrupting-AI-espionage) - AI agents doing most of an intrusion, credential harvesting included.
- [Sysdig, LLMjacking](https://sysdig.com/blog/llmjacking-stolen-cloud-credentials-used-in-new-ai-attack/) - Stolen cloud credentials used to run AI models at the victim's expense.
- [Sysdig, EMERALDWHALE](https://sysdig.com/blog/emeraldwhale/) - 15,000 cloud credentials stolen from exposed Git configs.
- [GitGuardian, The GhostAction campaign](https://blog.gitguardian.com/ghostaction-campaign-3-325-secrets-stolen/) - 3,325 secrets stolen through malicious GitHub workflows.
- [Nx, s1ngularity postmortem](https://nx.dev/blog/s1ngularity-postmortem) - A supply-chain attack that used AI CLIs to hunt for secrets.

## Research

- [Ferguson-Walter et al., Examining the Efficacy of Decoy-based and Psychological Cyber Deception](https://www.usenix.org/conference/usenixsecurity21/presentation/ferguson-walter) - USENIX Security 2021, controlled experiment with red teamers.
- [Ferguson-Walter, Imposing a Cyber Penalty Against Attackers with Cyber Deception](https://www.usenix.org/node/278212) - USENIX ;login:.

## Datasets

- [ATT&CK to deception mapping](https://github.com/falsetrailhq/attack-deception-mapping) - 28 ATT&CK techniques mapped to Engage, D3FEND, example decoys and alert signals (CC BY 4.0).

## Contributing

Pull requests welcome. Please add one link per pull request, in the right section, alphabetically within commercial platforms, with a one-line description that says what it is rather than how good it is. Vendor marketing pages go under Commercial platforms only.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, FalseTrail has waived all copyright and related rights to this list.
