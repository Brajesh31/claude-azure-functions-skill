# claude-azure-functions-skill

A Claude Code skill for designing, implementing, deploying, and operating event-driven applications with Azure Functions.

## Overview

Azure Functions provides managed execution for event-driven code. This skill focuses on reliable function design across .NET isolated worker, Node.js, and Python programming models, including HTTP triggers, background processing, durable orchestration, and production operations.

## Main Capabilities

- Build HTTP-triggered functions and API endpoints.
- Process queue, timer, and event-based triggers.
- Implement Durable Functions orchestration and activities.
- Use supported .NET isolated worker patterns.
- Work with the Node.js v4 programming model.
- Use the Python v2 decorator-based programming model.
- Improve cold-start and execution performance.
- Configure identity, secrets, logging, and monitoring.
- Prepare deployment and production-readiness checks.

## Supported Runtime Areas

The skill includes guidance for:

- .NET isolated worker.
- Node.js and TypeScript.
- Python.
- Durable Functions orchestration patterns.

Check the actual project runtime and extension versions before changing function configuration.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-azure-functions-skill.git ~/.claude/skills/azure-functions
```

## Usage

Invoke the skill for Azure Functions development tasks:

```text
/azure-functions
```

Provide the language, runtime version, trigger type, hosting plan, deployment target, and expected execution behavior.

## Recommended Workflow

1. Inspect the function app configuration and runtime.
2. Identify triggers, bindings, and dependencies.
3. Choose the appropriate programming model.
4. Keep handlers focused and non-blocking.
5. Configure retries, timeouts, and idempotency.
6. Separate configuration from code.
7. Apply managed identity or secure secret storage where appropriate.
8. Add structured logging and meaningful monitoring.
9. Test local execution and integration behavior.
10. Validate deployment settings before release.

## Anti-Patterns to Avoid

- Blocking asynchronous operations.
- Creating expensive clients repeatedly inside hot execution paths.
- Using outdated programming models for new projects without a compatibility reason.
- Assuming a function invocation runs exactly once.
- Storing secrets in source code.
- Omitting retry and failure handling.
- Treating local success as proof of production readiness.

## Production Checklist

- Trigger and binding configuration is correct.
- Runtime and extension versions are supported.
- Timeouts and memory settings fit the workload.
- Duplicate event handling is safe.
- Retry and dead-letter behavior is understood.
- Identity permissions follow least privilege.
- Secrets are not committed.
- Logs and alerts cover meaningful failures.
- Deployment and rollback procedures are documented.

## Repository Contents

- `SKILL.md`: Main Azure Functions guidance and patterns.
- `README.md`: Runtime coverage, workflow, and production checklist.

## Important Note

Azure Functions behavior depends on runtime, hosting plan, extension, and programming model versions. Verify version-specific configuration before applying examples to a production application.
