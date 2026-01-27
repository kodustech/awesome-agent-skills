# Awesome Agent Skills [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of agent skills for software engineering

> **Maintainer Note:** This list is curated and maintained by the engineering team at **[Kodus](https://kodus.io)**. We love open source and building better devtools.

---

## Content

- [What are Agent Skills?](#what-are-agent-skills)
- [Agent Skills](#agent-skills)
  - [Frontend Development](#frontend-development)
  - [Backend Development](#backend-development)
  - [DevOps](#devops)
  - [Testing & QA](#testing--qa)
  - [Security](#security)
  - [Observability](#observability)
  - [Performance](#performance)
  - [Mobile Development](#mobile-development)
  - [Blockchain](#blockchain)
  - [Infrastructure](#infrastructure)
  - [Data Science](#data-science)
  - [AI/ML](#aiml)
  - [Tooling](#tooling)
  - [Code Review](#code-review)
- [FAQ: Agent Skills](#faq-agent-skills)
- [Agent Skill Template](#agent-skill-template)



----
## What are Agent Skills?

Agent skills are modular, standardized capability packages that give agents on-demand abilities.

In practice, a skill is usually a small SKILL.md file that defines:

- When it should be used

- How the task should be executed

- What constraints and best practices apply

Skills follow a model of progressive disclosure: lightweight metadata loads first, and full instructions are loaded only when the skill becomes relevant.

This allows agents to stay fast and focused, while still executing tasks with real depth when needed.

-----

## Agent Skills

-----

### Frontend Development

| Skill | Description |
|-----------|-----------|
| [add-uint-support](https://github.com/pytorch/pytorch/tree/main/.claude/skills/add-uint-support) | Add unsigned integer (uint) type support to PyTorch operators by updating AT_DISPATCH macros. Use when adding support for uint16, uint32, uint64 types to operators, kernels, or when user mentions enabling unsigned types, barebones unsigned types, or uint support. |
| [writing-dev-server-tests](https://github.com/oven-sh/bun/tree/main/.claude/skills/writing-dev-server-tests) | Guides writing HMR/Dev Server tests in test/bake/. Use when creating or modifying dev server, hot reloading, or bundling tests. |
| [command-development](https://github.com/anthropics/claude-code/tree/main/plugins/plugin-dev/skills/command-development) | This skill should be used when the user asks to "create a slash command", "add a command", "write a custom command", "define command arguments", "use command frontmatter", "organize commands", "create command with file references", "interactive command", "use AskUserQuestion in command", or needs guidance on slash command structure, YAML frontmatter fields, dynamic arguments, bash execution in commands, user interaction patterns, or command development best practices for Claude Code. |
| [implementing-agent-modes](https://github.com/PostHog/posthog/tree/master/.claude/skills/implementing-agent-modes) | Guidelines to create/update a new mode for PostHog AI agent. Modes are a way to limit what tools, prompts, and prompt injections are applied and under what conditions. Achieve better results using your plan mode. |
| [wcag-audit-patterns](https://github.com/wshobson/agents/tree/main/plugins/accessibility-compliance/skills/wcag-audit-patterns) | Conduct WCAG 2.2 accessibility audits with automated testing, manual verification, and remediation guidance. Use when auditing websites for accessibility, fixing WCAG violations, or implementing accessible design patterns. |
| [risk-metrics-calculation](https://github.com/wshobson/agents/tree/main/plugins/quantitative-trading/skills/risk-metrics-calculation) | Calculate portfolio risk metrics including VaR, CVaR, Sharpe, Sortino, and drawdown analysis. Use when measuring portfolio risk, implementing risk limits, or building risk monitoring systems. |
| [nft-standards](https://github.com/wshobson/agents/tree/main/plugins/blockchain-web3/skills/nft-standards) | Implement NFT standards (ERC-721, ERC-1155) with proper metadata handling, minting strategies, and marketplace integration. Use when creating NFT contracts, building NFT marketplaces, or implementing digital asset systems. |
| [nextjs-app-router-patterns](https://github.com/wshobson/agents/tree/main/plugins/frontend-mobile-development/skills/nextjs-app-router-patterns) | Master Next.js 14+ App Router with Server Components, streaming, parallel routes, and advanced data fetching. Use when building Next.js applications, implementing SSR/SSG, or optimizing React Server Components. |
| [ml-pipeline-workflow](https://github.com/wshobson/agents/tree/main/plugins/machine-learning-ops/skills/ml-pipeline-workflow) | Build end-to-end MLOps pipelines from data preparation through model training, validation, and production deployment. Use when creating ML pipelines, implementing MLOps practices, or automating model training and deployment workflows. |
| [istio-traffic-management](https://github.com/wshobson/agents/tree/main/plugins/cloud-infrastructure/skills/istio-traffic-management) | Configure Istio traffic management including routing, load balancing, circuit breakers, and canary deployments. Use when implementing service mesh traffic policies, progressive delivery, or resilience patterns. |

---

### Backend Development

| Skill | Description |
|-----------|-----------|
| [bun-file-io](https://github.com/anomalyco/opencode/tree/dev/.opencode/skill/bun-file-io) | Use this when you are working on file operations like reading, writing, scanning, or deleting files. It summarizes the preferred file APIs and patterns used in this repo. It also notes when to use filesystem helpers for directories. |
| [add-admin-api-endpoint](https://github.com/TryGhost/Ghost/tree/main/.claude/skills/add-admin-api-endpoint) | Add a new endpoint or endpoints to Ghost's Admin API at `ghost/api/admin/**`. |
| [generate-migration](https://github.com/getsentry/sentry/tree/master/.claude/skills/generate-migration) | Generate Django database migrations for Sentry. Use when creating migrations, adding/removing columns or tables, adding indexes, or resolving migration conflicts. |
| [temporal-python-testing](https://github.com/wshobson/agents/tree/main/plugins/backend-development/skills/temporal-python-testing) | Test Temporal workflows with pytest, time-skipping, and mocking strategies. Covers unit testing, integration testing, replay testing, and local development setup. Use when implementing Temporal workflow tests or debugging test failures. |
| [zarr-python](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/zarr-python) | Chunked N-D arrays for cloud storage. Compressed arrays, parallel I/O, S3/GCS integration, NumPy/Dask/Xarray compatible, for large-scale scientific computing pipelines. |
| [sympy](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/sympy) | Use this skill when working with symbolic mathematics in Python. This skill should be used for symbolic computation tasks including solving equations algebraically, performing calculus operations (derivatives, integrals, limits), manipulating algebraic expressions, working with matrices symbolically, physics calculations, number theory problems, geometry computations, and generating executable code from mathematical expressions. Apply this skill when the user needs exact symbolic results rather than numerical approximations, or when working with mathematical formulas that contain variables and parameters. |
| [shap](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/shap) | Model interpretability and explainability using SHAP (SHapley Additive exPlanations). Use this skill when explaining machine learning model predictions, computing feature importance, generating SHAP plots (waterfall, beeswarm, bar, scatter, force, heatmap), debugging models, analyzing model bias or fairness, comparing models, or implementing explainable AI. Works with tree-based models (XGBoost, LightGBM, Random Forest), deep learning (TensorFlow, PyTorch), linear models, and any black-box model. |
| [sentencepiece](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/tokenization-sentencepiece) | Language-independent tokenizer treating text as raw Unicode. Supports BPE and Unigram algorithms. Fast (50k sentences/sec), lightweight (6MB memory), deterministic vocabulary. Used by T5, ALBERT, XLNet, mBART. Train on raw text without pre-tokenization. Use when you need multilingual support, CJK languages, or reproducible tokenization. |
| [scvi-tools](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/scvi-tools) | This skill should be used when working with single-cell omics data analysis using scvi-tools, including scRNA-seq, scATAC-seq, CITE-seq, spatial transcriptomics, and other single-cell modalities. Use this skill for probabilistic modeling, batch correction, dimensionality reduction, differential expression, cell type annotation, multimodal integration, and spatial analysis tasks. |
| [quality-manager-qmr](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/enterprise-communication/quality-manager-qmr) | Senior Quality Manager Responsible Person (QMR) for HealthTech and MedTech companies. Provides overall quality system responsibility, regulatory compliance oversight, management accountability, and strategic quality leadership. Use for quality system governance, regulatory compliance oversight, management responsibility, and quality strategic planning. |

---

### DevOps

| Skill | Description |
|-----------|-----------|
| [gitops-workflow](https://github.com/wshobson/agents/tree/main/plugins/kubernetes-operations/skills/gitops-workflow) | Implement GitOps workflows with ArgoCD and Flux for automated, declarative Kubernetes deployments with continuous reconciliation. Use when implementing GitOps practices, automating Kubernetes deployments, or setting up declarative infrastructure management. |
| [managing-devops-pipeline](https://github.com/TencentBlueKing/bk-ci/tree/master/ai/skills/managing-devops-pipeline) | Manage BlueKing CI pipeline build operations, including querying build history, retrieving startup parameters, checking build status, and triggering builds. Use when the user mentions pipelines, builds, deployments, CI/CD, BlueKing, or needs to trigger a build job. |
| [opentelemetry-instrumentation-extension](https://github.com/docker/mcp-gateway/tree/main/.claude/skills/otel-instrument) | Extend OpenTelemetry instrumentation when new functionality is added to the MCP Gateway. Use when (1) new operations/functions are added, (2) reviewing code for missing instrumentation, (3) user requests otel/telemetry additions, or (4) working with state-changing operations. Analyzes git diff, suggests instrumentation points following project standards in docs/telemetry/README.md, implements with approval, writes tests, updates documentation, and verifies with debug logging and docker logs. |
| [yaml-config-validator](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/planned-skills/generated/01-devops-basics/yaml-config-validator) | Yaml Config Validator - Auto-activating skill for DevOps Basics. Triggers on: yaml config validator, yaml config validator Part of the DevOps Basics skill category. |
| [version-bumper](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/skills/01-devops-basics/version-bumper) | Manage version bumper operations. Auto-activating skill for DevOps Basics. Triggers on: version bumper, version bumper Part of the DevOps Basics skill category. Use when working with version bumper functionality. Trigger with phrases like "version bumper", "version bumper", "version". |
| [terraform-state-manager](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/planned-skills/generated/02-devops-advanced/terraform-state-manager) | Terraform State Manager - Auto-activating skill for DevOps Advanced. Triggers on: terraform state manager, terraform state manager Part of the DevOps Advanced skill category. |
| [terraform-provider-config](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/skills/02-devops-advanced/terraform-provider-config) | Configure terraform provider config operations. Auto-activating skill for DevOps Advanced. Triggers on: terraform provider config, terraform provider config Part of the DevOps Advanced skill category. Use when configuring systems or services. Trigger with phrases like "terraform provider config", "terraform config", "terraform". |
| [terraform-module-creator](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/planned-skills/generated/02-devops-advanced/terraform-module-creator) | Terraform Module Creator - Auto-activating skill for DevOps Advanced. Triggers on: terraform module creator, terraform module creator Part of the DevOps Advanced skill category. |
| [ssh-key-manager](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/skills/01-devops-basics/ssh-key-manager) | Manage ssh key manager operations. Auto-activating skill for DevOps Basics. Triggers on: ssh key manager, ssh key manager Part of the DevOps Basics skill category. Use when working with ssh key manager functionality. Trigger with phrases like "ssh key manager", "ssh manager", "ssh". |
| [readme-generator](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/planned-skills/generated/01-devops-basics/readme-generator) | Readme Generator - Auto-activating skill for DevOps Basics. Triggers on: readme generator, readme generator Part of the DevOps Basics skill category. |

---

### Testing & QA

| Skill | Description |
|-----------|-----------|
| [qms-audit-expert](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/enterprise-communication/qms-audit-expert) | Senior QMS Audit Expert for internal and external quality management system auditing. Provides ISO 13485 audit expertise, audit program management, nonconformity identification, and corrective action verification. Use for internal audit planning, external audit preparation, audit execution, and audit follow-up activities. |
| [it-operations](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/development/it-operations) | Manages IT infrastructure, monitoring, incident response, and service reliability. Provides frameworks for ITIL service management, observability strategies, automation, backup/recovery, capacity planning, and operational excellence practices. |
| [evaluating-code-models](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/evaluation-bigcode-evaluation-harness) | Evaluates code generation models across HumanEval, MBPP, MultiPL-E, and 15+ benchmarks with pass@k metrics. Use when benchmarking code models, comparing coding abilities, testing multi-language support, or measuring code generation quality. Industry standard from BigCode Project used by HuggingFace leaderboards. |
| [resolve-conflicts](https://github.com/antinomyhq/forge/tree/main/.forge/skills/resolve-conflicts) | Use this skill immediately when the user mentions merge conflicts that need to be resolved. Do not attempt to resolve conflicts directly - invoke this skill first. This skill specializes in providing a structured framework for merging imports, tests, lock files (regeneration), configuration files, and handling deleted-but-modified files with backup and analysis. |
| [qlty-check](https://github.com/parcadei/Continuous-Claude-v3/tree/main/.claude/skills/qlty-check) | Code quality checks, formatting, and metrics via qlty CLI |
| [lint-and-validate](https://github.com/vudovn/antigravity-kit/tree/main/.agent/skills/lint-and-validate) | Automatic quality control, linting, and static analysis procedures. Use after every code modification to ensure syntax correctness and project standards. Triggers onKeywords: lint, format, check, validate, types, static analysis. |
| [simplify](https://github.com/meta-pytorch/OpenEnv/tree/main/.claude/skills/simplify) | Refactor code after tests pass. The "Refactor" phase of Red-Green-Refactor. |
| [changelog-orchestrator](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/automation/mattyp-changelog/skills/changelog-orchestrator) | Draft changelog PRs by collecting GitHub/Slack/Git changes, formatting with templates, running quality gates, and preparing a branch/PR. Use when generating weekly/monthly release notes or when the user asks to create a changelog from recent merges. Trigger with "changelog weekly", "generate release notes", "draft changelog", "create changelog PR". |
| [tdd-workflow](https://github.com/cfrs2005/claude-init/tree/main/templates/.claude/skills/tdd-workflow) | Use this skill when writing new features, fixing bugs, or refactoring code. Enforce test-driven development (TDD), including unit tests, integration tests, and end-to-end (E2E) tests, ensuring test coverage exceeds 80%. |
| [oping](https://github.com/bfly123/claude_code_bridge/tree/main/codex_skills/oping) | Test connectivity with OpenCode (shorthand: oc) using the oping CLI. Use when the user explicitly asks to check OpenCode/oc status or connectivity (e.g., “oc ping”, “oc is it alive?”, “is OpenCode connected?”), or when troubleshooting cases where OpenCode is not responding. |

---

### Security

| Skill | Description |
|-----------|-----------|
| [deployment-pipeline-design](https://github.com/wshobson/agents/tree/main/plugins/cicd-automation/skills/deployment-pipeline-design) | Design multi-stage CI/CD pipelines with approval gates, security checks, and deployment orchestration. Use when architecting deployment workflows, setting up continuous delivery, or implementing GitOps practices. |
| [wordpress-penetration-testing](https://github.com/zebbern/claude-code-guide/tree/main/skills/wordpress-penetration-testing) | This skill should be used when the user asks to "pentest WordPress sites", "scan WordPress for vulnerabilities", "enumerate WordPress users, themes, or plugins", "exploit WordPress vulnerabilities", or "use WPScan". It provides comprehensive WordPress security assessment methodologies. |
| [pentest-checklist](https://github.com/zebbern/claude-code-guide/tree/main/skills/pentest-checklist) | This skill should be used when the user asks to "plan a penetration test", "create a security assessment checklist", "prepare for penetration testing", "define pentest scope", "follow security testing best practices", or needs a structured methodology for penetration testing engagements. |
| [ton-vulnerability-scanner](https://github.com/trailofbits/skills/tree/main/plugins/building-secure-contracts/skills/not-so-smart-contracts-scanners/ton-vulnerability-scanner) | Scans TON (The Open Network) smart contracts for 3 critical vulnerabilities including integer-as-boolean misuse, fake Jetton contracts, and forward TON without gas checks. Use when auditing FunC contracts. (project, gitignored) |
| [performing-penetration-testing](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/security/penetration-tester/skills/performing-penetration-testing) | Perform security penetration testing to identify vulnerabilities. Use when conducting security assessments. Trigger with 'run pentest', 'security testing', or 'find vulnerabilities'. |
| [encrypting-and-decrypting-data](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/security/encryption-tool/skills/encrypting-and-decrypting-data) | Validate encryption implementations and cryptographic practices. Use when reviewing data security measures. Trigger with 'check encryption', 'validate crypto', or 'review security keys'. |
| [clerk-observability](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/saas-packs/clerk-pack/skills/clerk-observability) | Implement monitoring, logging, and observability for Clerk authentication. Use when setting up monitoring, debugging auth issues in production, or implementing audit logging. Trigger with phrases like "clerk monitoring", "clerk logging", "clerk observability", "clerk metrics", "clerk audit log". |
| [checking-owasp-compliance](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/security/owasp-compliance-checker/skills/checking-owasp-compliance) | Check compliance with OWASP Top 10 security risks and best practices. Use when performing comprehensive security audits. Trigger with 'check OWASP compliance', 'audit web security', or 'validate OWASP'. |
| [auditing-access-control](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/security/access-control-auditor/skills/auditing-access-control) | Audit access control implementations for security vulnerabilities and misconfigurations. Use when reviewing authentication and authorization. Trigger with 'audit access control', 'check permissions', or 'validate authorization'. |
| [llvm-obfuscation](https://github.com/gmh5225/awesome-llvm-security/tree/main/.claude/skills/llvm-obfuscation) | Expertise in LLVM-based code obfuscation techniques including OLLVM, control flow flattening, string encryption, virtualization, and anti-analysis methods. Use this skill when working on code protection, anti-reverse engineering, or implementing custom obfuscation passes. |

---

### Mobile Development

| Skill | Description |
|-----------|-----------|
| [stride-analysis-patterns](https://github.com/wshobson/agents/tree/main/plugins/security-scanning/skills/stride-analysis-patterns) | Apply STRIDE methodology to systematically identify threats. Use when analyzing system security, conducting threat modeling sessions, or creating security documentation. |
| [sast-configuration](https://github.com/wshobson/agents/tree/main/plugins/security-scanning/skills/sast-configuration) | Configure Static Application Security Testing (SAST) tools for automated vulnerability detection in application code. Use when setting up security scanning, implementing DevSecOps practices, or automating code vulnerability detection. |
| [web-performance-optimization](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/web-performance-optimization) | Optimize website and web application performance including loading speed, Core Web Vitals, bundle size, caching strategies, and runtime performance |
| [profiling-application-performance](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/backups/plugin-enhancements/plugin-backups/application-profiler_20251020_075450/skills/skill-adapter) | This skill enables Claude to profile application performance, analyzing CPU usage, memory consumption, and execution time. It is triggered when the user requests performance analysis, bottleneck identification, or optimization recommendations. The skill uses the application-profiler plugin to identify performance bottlenecks and suggest code-level optimizations. Use it when asked to "profile application", "analyze performance", or "find bottlenecks". It is also helpful when the user mentions specific performance metrics like "CPU usage", "memory leaks", or "execution time". |
| [granola-deploy-integration](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/saas-packs/granola-pack/skills/granola-deploy-integration) | Deploy Granola integrations to Slack, Notion, HubSpot, and other apps. Use when connecting Granola to productivity tools, setting up native integrations, or configuring auto-sync. Trigger with phrases like "granola slack", "granola notion", "granola hubspot", "granola integration", "connect granola". |
| [generating-end-to-end-tests](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/backups/plugin-enhancements/plugin-backups/e2e-test-framework_20251019_145520/skills/skill-adapter) | This skill enables Claude to generate end-to-end (E2E) tests for web applications. It leverages Playwright, Cypress, or Selenium to automate browser interactions and validate user workflows. Use this skill when the user requests to "create E2E tests", "generate end-to-end tests", or asks for help with "browser-based testing". The skill is particularly useful for testing user registration, login flows, shopping cart functionality, and other multi-step processes within a web application. It supports cross-browser testing and can be used to verify the responsiveness of web applications on different devices. |
| [creating-data-visualizations](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/backups/plugin-enhancements/plugin-backups/data-visualization-creator_20251019_190508/skills/skill-adapter) | This skill enables Claude to generate data visualizations, plots, charts, and graphs from provided data. It analyzes the data, selects the most appropriate visualization type, and creates a visually appealing and informative graphic. Use this skill when the user requests a visualization, plot, chart, or graph; when data needs to be presented visually; or when exploring data patterns. The skill is triggered by requests for "visualization", "plot", "chart", or "graph". |
| [single-cell-cellphonedb-communication-mapping](https://github.com/Starlitnightly/omicverse/tree/master/.claude/skills/single-cellphone-db) | Run omicverse's CellPhoneDB v5 wrapper on annotated single-cell data to infer ligand-receptor networks and produce CellChat-style visualisations. |
| [effect-patterns-platform-getting-started](https://github.com/PaulJPhilp/EffectPatterns/tree/main/config/.claude-plugin/plugins/effect-patterns/skills/effect-patterns-platform-getting-started) | Effect-TS patterns for Platform Getting Started. Use when working with platform getting started in Effect-TS applications. |
| [android-kotlin](https://github.com/alinaqi/claude-bootstrap/tree/main/skills/android-kotlin) | Android Kotlin development with Coroutines, Jetpack Compose, Hilt, and MockK testing |

---

### Blockchain

| Skill | Description |
|-----------|-----------|
| [gh-issue-triage](https://github.com/poindexter12/waypoint/tree/main/workflows/skills/gh-issue-triage) | Label taxonomy and triage workflow for GitHub issues. Defines type labels (bug/feature/enhancement/docs/chore), priority levels (critical/high/medium/low), status labels, and triage decision workflow. Use when categorizing and prioritizing issues. |
| [web-test-wallet-sign](https://github.com/automata-network/agent-skills/tree/main/web-test-wallet-sign) | Handle MetaMask signature and transaction popups during Web3 DApp testing - approve signatures, send transactions, call contracts. Detects popup type and handles gas errors. |
| [web-test-wallet-setup](https://github.com/automata-network/agent-skills/tree/main/web-test-wallet-setup) | Set up MetaMask wallet extension for Web3 DApp testing - download extension, import wallet from private key. Run at test start if tests/config.yaml has web3.enabled=true. |

---

### Infrastructure

| Skill | Description |
|-----------|-----------|
| [spark-optimization](https://github.com/wshobson/agents/tree/main/plugins/data-engineering/skills/spark-optimization) | Optimize Apache Spark jobs with partitioning, caching, shuffle optimization, and memory tuning. Use when improving Spark performance, debugging slow jobs, or scaling data processing pipelines. |
| [openrouter-debug-bundle](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/saas-packs/openrouter-pack/skills/openrouter-debug-bundle) | Execute set up comprehensive logging and debugging for OpenRouter. Use when investigating issues or monitoring requests. Trigger with phrases like 'openrouter debug', 'openrouter logging', 'openrouter trace', 'monitor openrouter'. |
| [linear-data-handling](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/saas-packs/linear-pack/skills/linear-data-handling) | Data synchronization, backup, and consistency patterns for Linear. Use when implementing data sync, creating backups, or ensuring data consistency across systems. Trigger with phrases like "linear data sync", "backup linear", "linear data consistency", "sync linear issues", "linear data export". |
| [master-plan-manager](https://github.com/ananddtyagi/cc-marketplace/tree/main/plugins/claude-dev-infrastructure/skills/master-plan-manager) | Safe MASTER_PLAN.md management with backup, validation, and intelligent updates. Use when updating task tracking, adding features to roadmap, or modifying project documentation. |
| [delegation-core](https://github.com/athola/claude-night-market/tree/master/plugins/conjure/skills/delegation-core) | Delegate tasks to external LLM services (Gemini, Qwen) with quota, logging, and error handling. |
| [market-signal-tracker](https://github.com/gtmagents/gtm-agents/tree/main/plugins/competitive-intelligence/skills/market-signal-tracker) | Operating system for logging market/competitive signals with severity, confidence, and routing. |
| [orchestrator](https://github.com/draphonix/skills/tree/main/.agents/skills/orchestrator) | Plan and coordinate multi-agent bead execution. Use when starting a new epic, assigning tracks to agents, or monitoring parallel work progress. |
| [dbt-projects-on-snowflake](https://github.com/sfc-gh-dflippo/snowflake-dbt-demo/tree/main/.claude/skills/dbt-projects-on-snowflake) | Deploying, managing, executing, and monitoring dbt projects natively within Snowflake using dbt PROJECT objects and event tables. Use this skill when you want to set up dbt development workspaces, deploy projects to Snowflake, schedule automated runs, monitor execution with event tables, or enable team collaboration directly in Snowflake. |
| [etl-core-patterns](https://github.com/majesticlabs-dev/majestic-marketplace/tree/master/plugins/majestic-data/skills/etl-core-patterns) | Core ETL reliability patterns including idempotency, checkpointing, error handling, chunking, retry logic, and logging. |
| [logcli-logs](https://github.com/cristianoliveira/dotfiles/tree/main/ai/shared/skills/logcli-logs) | Query and analyze logs from Grafana Loki using logcli. Use when the user mentions Loki, Grafana logs, logcli, or LogQL. Triggers on phrases like "query loki", "loki logs", "grafana logs", "use logcli", "LogQL query", or when explicitly asked to search logs using Loki/Grafana infrastructure. |

---

### AI/ML

| Skill | Description |
|-----------|-----------|
| [git-advanced-workflows](https://github.com/wshobson/agents/tree/main/plugins/developer-essentials/skills/git-advanced-workflows) | Master advanced Git workflows including rebasing, cherry-picking, bisect, worktrees, and reflog to maintain clean history and recover from any situation. Use when managing complex Git histories, collaborating on feature branches, or troubleshooting repository issues. |
| [pr-build-status](https://github.com/dotnet/maui/tree/main/.github/skills/pr-build-status) | Retrieve Azure DevOps build information for GitHub Pull Requests, including build IDs, stage status, and failed jobs. |
| [agentic-eval](https://github.com/github/awesome-copilot/tree/main/skills/agentic-eval) | Patterns and techniques for evaluating and improving AI agent outputs. Use this skill when: - Implementing self-critique and reflection loops - Building evaluator-optimizer pipelines for quality-critical generation - Creating test-driven code refinement workflows - Designing rubric-based or LLM-as-judge evaluation systems - Adding iterative improvement to agent outputs (code, reports, analysis) - Measuring and improving agent response quality |
| [senior-architect](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/development/senior-architect) | Comprehensive software architecture skill for designing scalable, maintainable systems using ReactJS, NextJS, NodeJS, Express, React Native, Swift, Kotlin, Flutter, Postgres, GraphQL, Go, Python. Includes architecture diagram generation, system design patterns, tech stack decision frameworks, and dependency analysis. Use when designing system architecture, making technical decisions, creating architecture diagrams, evaluating trade-offs, or defining integration patterns. |
| [railway-templates](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/railway/templates) | Search and deploy services from Railway's template marketplace. Use when user wants to add a service from a template, find templates for a specific use case, or deploy tools like Ghost, Strapi, n8n, Minio, Uptime Kuma, etc. For databases (Postgres, Redis, MySQL, MongoDB), prefer the railway-database skill. |
| [railway-database](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/railway/database) | Add official Railway database services (Postgres, Redis, MySQL, MongoDB). Use when user wants to add a database, says "add postgres", "add redis", "add database", "connect to database", or "wire up the database". For other templates (Ghost, Strapi, n8n), use the railway-templates skill. |
| [clinicaltrials-database](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/clinicaltrials-database) | Query ClinicalTrials.gov via API v2. Search trials by condition, drug, location, status, or phase. Retrieve trial details by NCT ID, export data, for clinical research and patient matching. |
| [redis-inspect](https://github.com/civitai/civitai/tree/main/.claude/skills/redis-inspect) | Inspect Redis cache keys, values, and TTLs for debugging. Supports both main cache and system cache. Use for debugging cache issues, checking cached values, and monitoring cache state. Read-only by default. |
| [networkx](https://github.com/K-Dense-AI/claude-scientific-skills/tree/main/scientific-skills/networkx) | Comprehensive toolkit for creating, analyzing, and visualizing complex networks and graphs in Python. Use when working with network/graph data structures, analyzing relationships between entities, computing graph algorithms (shortest paths, centrality, clustering), detecting communities, generating synthetic networks, or visualizing network topologies. Applicable to social networks, biological networks, transportation systems, citation networks, and any domain involving pairwise relationships. |
| [hula-skill](https://github.com/HuLaSpark/HuLa/tree/master/skills/hula-skill) | HuLa project skill for frontend (Vue 3 + Vite + UnoCSS + Naive UI/Vant), backend (Tauri v2 + Rust + SeaORM/SQLite), full-stack flows, and build/release work. Use when the user mentions hula or HuLa or requests changes in this repository; after triggering, ask which scope (frontend/backend/fullstack/build-release) to enable. |

---

### Data Science

| Skill | Description |
|-----------|-----------|
| [docstring](https://github.com/pytorch/pytorch/tree/main/.claude/skills/docstring) | Write docstrings for PyTorch functions and methods following PyTorch conventions. Use when writing or updating docstrings in PyTorch code. |
| [website-maintainer](https://github.com/yamadashy/repomix/tree/main/.claude/skills/website-maintainer) | Use this skill when working on the Repomix documentation website in `website/` directory, including VitePress configuration, multi-language content, or translation workflows. |
| [torchdrug](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/torchdrug) | Graph-based drug discovery toolkit. Molecular property prediction (ADMET), protein modeling, knowledge graph reasoning, molecular generation, retrosynthesis, GNNs (GIN, GAT, SchNet), 40+ datasets, for PyTorch-based ML on molecules, proteins, and biomedical graphs. |
| [skypilot-multi-cloud-orchestration](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/infrastructure-skypilot) | Multi-cloud orchestration for ML workloads with automatic cost optimization. Use when you need to run training or batch jobs across multiple clouds, leverage spot instances with auto-recovery, or optimize GPU costs across providers. |
| [simpo-training](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/post-training-simpo) | Simple Preference Optimization for LLM alignment. Reference-free alternative to DPO with better performance (+6.4 points on AlpacaEval 2.0). No reference model needed, more efficient than DPO. Use for preference alignment when want simpler, faster training than DPO/PPO. |
| [ray-data](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/data-processing-ray-data) | Scalable data processing for ML workloads. Streaming execution across CPU/GPU, supports Parquet/CSV/JSON/images. Integrates with Ray Train, PyTorch, TensorFlow. Scales from single machine to 100s of nodes. Use for batch inference, data preprocessing, multi-modal data loading, or distributed ETL pipelines. |
| [quantizing-models-bitsandbytes](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/optimization-bitsandbytes) | Quantizes LLMs to 8-bit or 4-bit for 50-75% memory reduction with minimal accuracy loss. Use when GPU memory is limited, need to fit larger models, or want faster inference. Supports INT8, NF4, FP4 formats, QLoRA training, and 8-bit optimizers. Works with HuggingFace Transformers. |
| [pytorch-lightning](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/pytorch-lightning) | Deep learning framework (PyTorch Lightning). Organize PyTorch code into LightningModules, configure Trainers for multi-GPU/TPU, implement data pipelines, callbacks, logging (W&B, TensorBoard), distributed training (DDP, FSDP, DeepSpeed), for scalable neural network training. |
| [pytdc](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/pytdc) | Therapeutics Data Commons. AI-ready drug discovery datasets (ADME, toxicity, DTI), benchmarks, scaffold splits, molecular oracles, for therapeutic ML and pharmacological prediction. |
| [pyhealth](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/pyhealth) | Comprehensive healthcare AI toolkit for developing, testing, and deploying machine learning models with clinical data. This skill should be used when working with electronic health records (EHR), clinical prediction tasks (mortality, readmission, drug recommendation), medical coding systems (ICD, NDC, ATC), physiological signals (EEG, ECG), healthcare datasets (MIMIC-III/IV, eICU, OMOP), or implementing deep learning models for healthcare applications (RETAIN, SafeDrug, Transformer, GNN). |

---

### Observability

| Skill | Description |
|-----------|-----------|
| [risk-metrics-calculation](https://github.com/wshobson/agents/tree/main/plugins/quantitative-trading/skills/risk-metrics-calculation) | Calculate portfolio risk metrics including VaR, CVaR, Sharpe, Sortino, and drawdown analysis. Use when measuring portfolio risk, implementing risk limits, or building risk monitoring systems. |
| [domain-cloud-native](https://github.com/rustfs/rustfs/tree/main/.claude/skills/domain-cloud-native) | Use when building cloud-native applications. Keywords: Kubernetes, k8s, Docker, containers, gRPC, Tonic, microservices, service mesh, observability, tracing, metrics, health checks, cloud, deployment, cloud-native, microservices, containers. |
| [appinsights-instrumentation](https://github.com/github/awesome-copilot/tree/main/skills/appinsights-instrumentation) | Instrument a webapp to send useful telemetry data to Azure App Insights |
| [senior-qa](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/development/senior-qa) | Comprehensive QA and testing skill for quality assurance, test automation, and testing strategies for ReactJS, NextJS, NodeJS applications. Includes test suite generation, coverage analysis, E2E testing setup, and quality metrics. Use when designing test strategies, writing test cases, implementing test automation, performing manual testing, or analyzing test coverage. |
| [pyvene-interventions](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/mechanistic-interpretability-pyvene) | Provides guidance for performing causal interventions on PyTorch models using pyvene's declarative intervention framework. Use when conducting causal tracing, activation patching, interchange intervention training, or testing causal hypotheses about model behavior. |
| [pytorch-lightning](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/pytorch-lightning) | Deep learning framework (PyTorch Lightning). Organize PyTorch code into LightningModules, configure Trainers for multi-GPU/TPU, implement data pipelines, callbacks, logging (W&B, TensorBoard), distributed training (DDP, FSDP, DeepSpeed), for scalable neural network training. |
| [it-operations](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/development/it-operations) | Manages IT infrastructure, monitoring, incident response, and service reliability. Provides frameworks for ITIL service management, observability strategies, automation, backup/recovery, capacity planning, and operational excellence practices. |
| [evaluating-code-models](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/evaluation-bigcode-evaluation-harness) | Evaluates code generation models across HumanEval, MBPP, MultiPL-E, and 15+ benchmarks with pass@k metrics. Use when benchmarking code models, comparing coding abilities, testing multi-language support, or measuring code generation quality. Industry standard from BigCode Project used by HuggingFace leaderboards. |
| [cto-advisor](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/business-marketing/cto-advisor) | Technical leadership guidance for engineering teams, architecture decisions, and technology strategy. Includes tech debt analyzer, team scaling calculator, engineering metrics frameworks, technology evaluation tools, and ADR templates. Use when assessing technical debt, scaling engineering teams, evaluating technologies, making architecture decisions, establishing engineering metrics, or when user mentions CTO, tech debt, technical debt, team scaling, architecture decisions, technology evaluation, engineering metrics, DORA metrics, or technology strategy. |
| [migrating-to-vendure-dashboard](https://github.com/vendurehq/vendure/tree/master/.claude/skills/vendure-dashboard-migration) | Migrates Vendure Admin UI extensions (legacy Angular-based) to the new React Dashboard. |

---

### Performance

| Skill | Description |
|-----------|-----------|
| [spark-optimization](https://github.com/wshobson/agents/tree/main/plugins/data-engineering/skills/spark-optimization) | Optimize Apache Spark jobs with partitioning, caching, shuffle optimization, and memory tuning. Use when improving Spark performance, debugging slow jobs, or scaling data processing pipelines. |
| [hybrid-cloud-networking](https://github.com/wshobson/agents/tree/main/plugins/cloud-infrastructure/skills/hybrid-cloud-networking) | Configure secure, high-performance connectivity between on-premises infrastructure and cloud platforms using VPN and dedicated connections. Use when building hybrid cloud architectures, connecting data centers to cloud, or implementing secure cross-premises networking. |
| [gitlab-ci-patterns](https://github.com/wshobson/agents/tree/main/plugins/cicd-automation/skills/gitlab-ci-patterns) | Build GitLab CI/CD pipelines with multi-stage workflows, caching, and distributed runners for scalable automation. Use when implementing GitLab CI/CD, optimizing pipeline performance, or setting up automated testing and deployment. |
| [zarr-python](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/scientific/zarr-python) | Chunked N-D arrays for cloud storage. Compressed arrays, parallel I/O, S3/GCS integration, NumPy/Dask/Xarray compatible, for large-scale scientific computing pipelines. |
| [skypilot-multi-cloud-orchestration](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/infrastructure-skypilot) | Multi-cloud orchestration for ML workloads with automatic cost optimization. Use when you need to run training or batch jobs across multiple clouds, leverage spot instances with auto-recovery, or optimize GPU costs across providers. |
| [simpo-training](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/post-training-simpo) | Simple Preference Optimization for LLM alignment. Reference-free alternative to DPO with better performance (+6.4 points on AlpacaEval 2.0). No reference model needed, more efficient than DPO. Use for preference alignment when want simpler, faster training than DPO/PPO. |
| [senior-ml-engineer](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/development/senior-ml-engineer) | World-class ML engineering skill for productionizing ML models, MLOps, and building scalable ML systems. Expertise in PyTorch, TensorFlow, model deployment, feature stores, model monitoring, and ML infrastructure. Includes LLM integration, fine-tuning, RAG systems, and agentic AI. Use when deploying ML models, building ML platforms, implementing MLOps, or integrating LLMs into production systems. |
| [senior-backend](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/development/senior-backend) | Comprehensive backend development skill for building scalable backend systems using NodeJS, Express, Go, Python, Postgres, GraphQL, REST APIs. Includes API scaffolding, database optimization, security implementation, and performance tuning. Use when designing APIs, optimizing database queries, implementing business logic, handling authentication/authorization, or reviewing backend code. |
| [senior-architect](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/development/senior-architect) | Comprehensive software architecture skill for designing scalable, maintainable systems using ReactJS, NextJS, NodeJS, Express, React Native, Swift, Kotlin, Flutter, Postgres, GraphQL, Go, Python. Includes architecture diagram generation, system design patterns, tech stack decision frameworks, and dependency analysis. Use when designing system architecture, making technical decisions, creating architecture diagrams, evaluating trade-offs, or defining integration patterns. |
| [ray-train](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/skills/ai-research/distributed-training-ray-train) | Distributed training orchestration across clusters. Scales PyTorch/TensorFlow/HuggingFace from laptop to 1000s of nodes. Built-in hyperparameter tuning with Ray Tune, fault tolerance, elastic scaling. Use when training massive models across multiple machines or running distributed hyperparameter sweeps. |

---

### Tooling

| Skill | Description |
|-----------|-----------|
| [implementing-agent-modes](https://github.com/PostHog/posthog/tree/master/.claude/skills/implementing-agent-modes) | Guidelines to create/update a new mode for PostHog AI agent. Modes are a way to limit what tools, prompts, and prompt injections are applied and under what conditions. Achieve better results using your plan mode. |
| [wox-plugin-creator](https://github.com/Wox-launcher/Wox/tree/master/wox.core/resource/ai/skills/wox-plugin-creator) | Create and scaffold Wox plugins (nodejs, python, script-nodejs, script-python). Use when cloning official SDK templates, generating script plugin templates, or preparing plugins for publish. |
| [temporal-python-testing](https://github.com/wshobson/agents/tree/main/plugins/backend-development/skills/temporal-python-testing) | Test Temporal workflows with pytest, time-skipping, and mocking strategies. Covers unit testing, integration testing, replay testing, and local development setup. Use when implementing Temporal workflow tests or debugging test failures. |
| [sast-configuration](https://github.com/wshobson/agents/tree/main/plugins/security-scanning/skills/sast-configuration) | Configure Static Application Security Testing (SAST) tools for automated vulnerability detection in application code. Use when setting up security scanning, implementing DevSecOps practices, or automating code vulnerability detection. |
| [ml-pipeline-workflow](https://github.com/wshobson/agents/tree/main/plugins/machine-learning-ops/skills/ml-pipeline-workflow) | Build end-to-end MLOps pipelines from data preparation through model training, validation, and production deployment. Use when creating ML pipelines, implementing MLOps practices, or automating model training and deployment workflows. |
| [javascript-testing-patterns](https://github.com/wshobson/agents/tree/main/plugins/javascript-typescript/skills/javascript-testing-patterns) | Implement comprehensive testing strategies using Jest, Vitest, and Testing Library for unit tests, integration tests, and end-to-end testing with mocking, fixtures, and test-driven development. Use when writing JavaScript/TypeScript tests, setting up test infrastructure, or implementing TDD/BDD workflows. |
| [incident-runbook-templates](https://github.com/wshobson/agents/tree/main/plugins/incident-response/skills/incident-runbook-templates) | Create structured incident response runbooks with step-by-step procedures, escalation paths, and recovery actions. Use when building runbooks, responding to incidents, or establishing incident response procedures. |
| [gitops-workflow](https://github.com/wshobson/agents/tree/main/plugins/kubernetes-operations/skills/gitops-workflow) | Implement GitOps workflows with ArgoCD and Flux for automated, declarative Kubernetes deployments with continuous reconciliation. Use when implementing GitOps practices, automating Kubernetes deployments, or setting up declarative infrastructure management. |
| [gitlab-ci-patterns](https://github.com/wshobson/agents/tree/main/plugins/cicd-automation/skills/gitlab-ci-patterns) | Build GitLab CI/CD pipelines with multi-stage workflows, caching, and distributed runners for scalable automation. Use when implementing GitLab CI/CD, optimizing pipeline performance, or setting up automated testing and deployment. |
| [git-advanced-workflows](https://github.com/wshobson/agents/tree/main/plugins/developer-essentials/skills/git-advanced-workflows) | Master advanced Git workflows including rebasing, cherry-picking, bisect, worktrees, and reflog to maintain clean history and recover from any situation. Use when managing complex Git histories, collaborating on feature branches, or troubleshooting repository issues. |

---

### Code Review

| Skill | Description |
|-----------|-----------|
| [dyadmulti-pr-review](https://github.com/dyad-sh/dyad/tree/main/.claude/skills/multi-pr-review) | Multi-agent code review system that spawns three independent Claude sub-agents to review PR diffs. Each agent receives files in different randomized order to reduce ordering bias. Issues are classified as high/medium/low severity. Results are aggregated using consensus voting - only issues identified by 2+ agents where at least one rated it medium or higher severity are reported and posted as PR comments. Use when reviewing PRs, performing code review with multiple perspectives, or when consensus-based issue detection is needed. |
| [prowler-pr](https://github.com/prowler-cloud/prowler/tree/master/skills/prowler-pr) | Creates Pull Requests for Prowler following the project template and conventions. Trigger: When working on pull request requirements or creation (PR template sections, PR title Conventional Commits check, changelog gate/no-changelog label), or when inspecting PR-related GitHub workflows like conventional-commit.yml, pr-check-changelog.yml, pr-conflict-checker.yml, labeler.yml, or CODEOWNERS. |
| [pair-programming](https://github.com/ruvnet/claude-flow/tree/main/.claude/skills/pair-programming) | AI-assisted pair programming with multiple modes (driver/navigator/switch), real-time verification, quality monitoring, and comprehensive testing. Supports TDD, debugging, refactoring, and learning sessions. Features automatic role switching, continuous code review, security scanning, and performance optimization with truth-score verification. |
| [reviewing-changes](https://github.com/bitwarden/android/tree/main/.claude/skills/reviewing-changes) | Guides Android code reviews with type-specific checklists and MVVM/Compose pattern validation. Use when reviewing Android PRs, pull requests, diffs, or local changes involving Kotlin, ViewModel, Composable, Repository, or Gradle files. Triggered by "review PR", "review changes", "check this code", "Android review", or code review requests mentioning bitwarden/android. Loads specialized checklists for feature additions, bug fixes, UI refinements, refactoring, dependency updates, and infrastructure changes. |
| [pr-create-from-body](https://github.com/VisActor/VChart/tree/develop/.trae/skills/pr-create-from-body) | Creates a GitHub Pull Request for the VChart project using a local markdown file as its body. This skill exclusively uses a logged-in `gh` CLI environment to operate. |
| [loki-mode](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/loki-mode) | Multi-agent autonomous startup system for Claude Code. Triggers on "Loki Mode". Orchestrates 100+ specialized agents across engineering, QA, DevOps, security, data/ML, business operations, marketing, HR, and customer success. Takes PRD to fully deployed, revenue-generating product with zero human intervention. Features Task tool for subagent dispatch, parallel code review with 3 specialized reviewers, severity-based issue triage, distributed task queue with dead letter handling, automatic deployment to cloud providers, A/B testing, customer feedback loops, incident response, circuit breakers, and self-healing. Handles rate limits via distributed state checkpoints and auto-resume with exponential backoff. Requires --dangerously-skip-permissions flag. |
| [pr-review-reply](https://github.com/stacklok/toolhive/tree/main/.claude/skills/pr-review-reply) | Reply to and resolve GitHub PR review comments using the GitHub CLI and GraphQL API. |
| [swiftui-performance-audit](https://github.com/steipete/agent-scripts/tree/main/skills/swiftui-performance-audit) | Audit and improve SwiftUI runtime performance from code review and architecture. Use for requests to diagnose slow rendering, janky scrolling, high CPU/memory usage, excessive view updates, or layout thrash in SwiftUI apps, and to provide guidance for user-run Instruments profiling when code review alone is insufficient. |
| [alignment-review](https://github.com/meta-pytorch/OpenEnv/tree/main/.claude/skills/alignment-review) | Review code changes for bugs and alignment with OpenEnv principles and RFCs. Use when reviewing PRs, checking code before commit, or when asked to review changes. Implements two-tier review model. |
| [windsurf-known-pitfalls](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/saas-packs/windsurf-pack/skills/windsurf-known-pitfalls) | Identify and avoid Windsurf anti-patterns and common integration mistakes. Use when reviewing Windsurf code for issues, onboarding new developers, or auditing existing Windsurf integrations for best practices violations. Trigger with phrases like "windsurf mistakes", "windsurf anti-patterns", "windsurf pitfalls", "windsurf what not to do", "windsurf code review". |
| [vercel-known-pitfalls](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/saas-packs/vercel-pack/skills/vercel-known-pitfalls) | Execute identify and avoid Vercel anti-patterns and common integration mistakes. Use when reviewing Vercel code for issues, onboarding new developers, or auditing existing Vercel integrations for best practices violations. Trigger with phrases like "vercel mistakes", "vercel anti-patterns", "vercel pitfalls", "vercel what not to do", "vercel code review". |
| [clay-known-pitfalls](https://github.com/jeremylongshore/claude-code-plugins-plus-skills/tree/main/plugins/saas-packs/clay-pack/skills/clay-known-pitfalls) | Identify and avoid Clay anti-patterns and common integration mistakes. Use when reviewing Clay code for issues, onboarding new developers, or auditing existing Clay integrations for best practices violations. Trigger with phrases like "clay mistakes", "clay anti-patterns", "clay pitfalls", "clay what not to do", "clay code review". |
| [octocode-pr-review](https://github.com/bgauryy/octocode-mcp/tree/main/packages/octocode-cli/skills/octocode-pr-review) | PR review for bugs, security & quality (requires PR URL) |
| [fix-pr](https://github.com/agentfront/frontmcp/tree/main/.claude/skills/fix-pr) | Review a CodeRabbit PR comment and produce an action plan when prompted to analyze a review comment. |
| [code-quality-analysis-with-pmat](https://github.com/paiml/paiml-mcp-agent-toolkit/tree/master/.claude/skills/pmat-quality) | Analyzes code quality, complexity, and technical debt using PMAT (Pragmatic AI Labs MCP Agent Toolkit). Use this skill when: - User mentions "code quality", "complexity", "technical debt", or "maintainability" - Reviewing code or conducting code review - Modifying or refactoring existing code files - Creating pull requests or preparing commits - Investigating performance or quality issues Supports 25+ languages including Rust, Python, TypeScript, JavaScript, Go, C++, Java, Ruby, PHP, Swift, and more. Provides cyclomatic complexity, cognitive complexity, maintainability index, dead code detection, and technical debt annotations (SATD: TODO, FIXME, HACK comments). |



-----

## FAQ: Agent Skills

### What are Agent Skills?
Agent Skills are instruction files that teach AI agents how to perform specific tasks. You can think of them as practical guides that the agent reads and follows when it needs to solve a problem. They are only loaded when relevant, so the agent stays fast and focused.

---

### How do Agent Skills work in practice?
The agent initially reads only the name and description of all available skills. When it identifies that a skill is relevant to the current task, it loads the full content and follows those instructions to execute the work.

This allows you to teach new behaviors without changing the model, retraining anything, or adding complexity to the setup.

---

### Are Agent Skills the same as saved prompts?
No.

A saved prompt is just text that you manually paste or reuse. Agent Skills are structured instructions with context, rules, examples, workflows, and sometimes supporting assets. They become part of how the agent works, not just reusable text.

---

### What’s the difference between Agent Skills and fine-tuning?
- **Fine-tuning** permanently changes how the model behaves. It’s expensive, slow to iterate, and hard to roll back.  
- **Agent Skills** are runtime instructions. You can create, edit, test, version, swap, or remove them at any time without touching the model.

In practice: skills give you flexibility. Fine-tuning gives you rigidity.

---

### What’s the difference between Agent Skills and MCP?
They solve different problems and work extremely well together:

- **Agent Skills** define *how the agent should think and act* → workflows, best practices, rules, checklists, patterns  
- **MCP (Model Context Protocol)** defines *how the agent accesses the outside world* → APIs, databases, tools, and services  

In short:  
Skills teach **how to work**.  
MCP provides **access to tools**.

---

### Can skills run code or automations?
Depending on the platform, yes. Many allow attaching scripts and commands. This makes skills far more powerful, but also requires caution. Treat skills as executable code: review them carefully and only run what you trust.

---

### How to create a good Agent Skill?

1. **Clear scope**  
   Each skill should solve one well-defined problem.

2. **Objective description**  
   Name and description must clearly state when the skill should be used.

3. **Practical step-by-step instructions**  
   Explain exactly how the agent should reason, analyze, and respond.

4. **Explicit output format**  
   Define how the final answer must be structured.

5. **Real examples**  
   Good examples are more valuable than long explanations.

## Agent Skill Template

Use this template as a starting point for building your own skills.

```md
---
name: my-skill-name
description: A clear description of what this skill does.
---

# My Skill Name

Detailed description of the skill’s purpose.

## When to Use This Skill

- Use case 1  
- Use case 2  

## Instructions

[Detailed instructions for the agent on how to execute this skill]

## Examples

[Real-world examples]

```

-----
## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

If you’ve created an Agent Skill or have a suggestion for one that should be listed here, feel free to open a PR.

-----
## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
