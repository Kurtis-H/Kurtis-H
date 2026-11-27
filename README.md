## Kurtis H · QA Engineer / SDET

I build test automation and the systems around it: frameworks, CI pipelines, load and security testing, and AI agents that do QA work. I care about tests that catch real bugs, so most projects here **prove** their tests work by planting bugs and showing they get caught.

Every repo has CI on GitHub Actions, a protected `main`, required checks, and pull requests reviewed with my own [PR review skill](https://github.com/Kurtis-H/qa-agent-skills/blob/main/skills/pr-review/SKILL.md).

**[Quality dashboard](https://kurtis-h.github.io/quality-dashboard/):** CI status for every repo and every assessment finding on one page, rebuilt daily and checked against its sources before it's published ([source](https://github.com/Kurtis-H/quality-dashboard)).

### The booking platform: one product, tested at every layer

A small ticketing product built end to end, so each kind of testing has something real to test.

| Project | What it is | What it shows |
|---|---|---|
| [api-performance-lab](https://github.com/Kurtis-H/api-performance-lab) | Python / FastAPI / Postgres API with six switchable performance problems | k6 load, soak, spike and stress tests with a regression gate; contract tests (Schemathesis); verifies both apps' Pact contracts; Postman; Grafana. Found three real bugs I hadn't planted |
| [booking-web](https://github.com/Kurtis-H/booking-web) | React + TypeScript front end | Vitest and MSW component tests, Playwright e2e on desktop and mobile, axe accessibility checks, OpenAPI-generated types, a Pact consumer contract |
| [booking-mobile](https://github.com/Kurtis-H/booking-mobile) | Flutter app | Unit, widget, golden and accessibility tests; integration tests and Maestro flows on an Android emulator in CI; a Pact consumer contract |
| [platform-probe](https://github.com/Kurtis-H/platform-probe) | Go synthetic monitor, standard library only | Concurrent checks, a purchase journey that also checks access control, Prometheus metrics, fuzzing, race detector |
| [locator-lens](https://github.com/Kurtis-H/locator-lens) | Chrome extension (Manifest V3) | Suggests the most robust Playwright or Cypress locator; tested by loading the real extension and running every suggestion |
| [framework-showdown](https://github.com/Kurtis-H/framework-showdown) | Playwright vs Cypress vs Appium vs Maestro | One test plan in four frameworks, measured over 10 CI runs each for setup time, speed, flakiness and code size |
| [booking-pentest](https://github.com/Kurtis-H/booking-pentest) | Penetration test of the API and web app | A professional report (CVSS 3.1, OWASP API Top 10) where every finding is a test that runs in CI. 8 findings, 5 fixed and retested, 3 accepted with reasons |
| [mobile-security-lab](https://github.com/Kurtis-H/mobile-security-lab) | Security assessment of the Android app (OWASP MASVS) | The release APK is built and scanned with MobSF in CI, and every scanner item must be triaged. Found an issue MobSF can't see in Flutter apps; 4 of 5 findings fixed and retested |
| [resilience-lab](https://github.com/Kurtis-H/resilience-lab) | Fault injection with Toxiproxy | The database goes down, slows, drops connections or stays locked, and the API goes silent. Each finding is an experiment; orders are checked to stay all or nothing. 4 findings, all fixed and retested |

### Test frameworks and tooling

| Project | What it is |
|---|---|
| [qa-reference-framework](https://github.com/Kurtis-H/qa-reference-framework) | Playwright + TypeScript framework: UI, API contracts, accessibility, security, k6 performance, and ZAP/Trivy scans in CI |
| [bug-hunt-lab](https://github.com/Kurtis-H/bug-hunt-lab) | Practice app with 21 switchable bugs and a mutation-testing scorecard showing which bugs a test suite catches |
| [flaky-hunter](https://github.com/Kurtis-H/flaky-hunter) | Finds flaky tests across CI runs from JUnit XML, and tells them apart from real regressions |

### Security testing

| Project | What it is |
|---|---|
| [supply-chain-lab](https://github.com/Kurtis-H/supply-chain-lab) | SBOMs, keyless-signed images and SLSA provenance, with a deploy gate proven in CI to reject tampered images, and a malicious-dependency demo showing which defenses really stop it |
| [security-practice-lab](https://github.com/Kurtis-H/security-practice-lab) | Automated OWASP Juice Shop attacks proven by the shop's own scoreboard, Atheris fuzzing that finds bugs a passing test suite missed, and a test runner built from scratch and checked with mutation testing |
| [vuln-shop](https://github.com/Kurtis-H/vuln-shop) | Intentionally vulnerable shop: every hole has a test proving it exists and a test proving the fix works |
| [scan-triage-bot](https://github.com/Kurtis-H/scan-triage-bot) | Merges ZAP, Trivy and SARIF reports into one ranked, deduplicated list with explainable scores |

### AI for QA

| Project | What it is |
|---|---|
| [qa-agent-skills](https://github.com/Kurtis-H/qa-agent-skills) | QA know-how packaged as skills for AI coding agents, plus a harness that measures whether each skill actually helps |
| [testgen-agent](https://github.com/Kurtis-H/testgen-agent) | Agent that writes API tests from an OpenAPI spec and must prove each test before it's kept |
| [agent-guardrails-lab](https://github.com/Kurtis-H/agent-guardrails-lab) | Guardrails for a tool-using AI agent, proven against a worst-case agent that obeys every prompt injection: 11 attacks blocked, real tasks still done, 19 of 19 weakened rules caught |
| [llm-arena](https://github.com/Kurtis-H/llm-arena) | Tests AI with AI: attacker, target and judge models, plus a check on whether the judge can be trusted |
| [bug-report-enhancer](https://github.com/Kurtis-H/bug-report-enhancer) | Turns vague bug reports into actionable ones, with secret redaction and a check for details the AI made up |

### Toolbox

**Testing:** Playwright · Cypress · Appium · Maestro · pytest · Vitest · Flutter test · k6 · Schemathesis · Pact · Postman/Newman · axe · Toxiproxy · OWASP ZAP · MobSF · Trivy · Semgrep · Sigstore/cosign · Syft · Grype  
**Languages:** TypeScript/JavaScript · Python · Go · Dart  
**Platform:** GitHub Actions · Docker · Postgres · Prometheus · Grafana · Android emulator CI
