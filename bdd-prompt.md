Create reusable GitHub Copilot custom-agent definition files for this repository, but do not analyze, test, or modify any application source code at this stage.

Create the following files under the .github/agents directory:
1. bdd-orchestrator.agent.md
2. rest-response-bdd.agent.md
3. kafka-producer-bdd.agent.md
4. kafka-consumer-bdd.agent.md
5. bdd-reviewer.agent.md

Each file must be a valid GitHub Copilot custom-agent definition containing YAML frontmatter with name, description, target set to vscode, user-invocable set to true, and appropriate tools, followed by detailed Markdown instructions defining the agent’s responsibilities.

Configure the REST Response BDD Agent to analyze selected requirements, OpenAPI specifications, controllers, DTOs, validation annotations, authentication configuration, and exception handlers, and generate Cucumber-JVM, REST Assured, and JUnit 5 tests that validate only REST status codes, headers, content types, JSON bodies, JSON schemas, error responses, and correlation identifiers.

Configure the Kafka Producer BDD Agent to generate tests for application-produced Kafka events, including topic, key, headers, payload, schema, correlation ID, retries, serialization errors, SSL configuration, and JKS keystore and truststore handling.

Configure the Kafka Consumer BDD Agent to generate tests for incoming Kafka events, including successful processing, invalid payloads, duplicates, idempotency, retries, dead-letter topics, deserialization errors, SSL configuration, and observable processing results.

Configure the BDD Orchestrator Agent to inspect a selected business flow and coordinate REST-response, Kafka-producer, and Kafka-consumer testing capabilities when multiple patterns are involved, while keeping MySQL and GemFire validation disabled until explicitly requested.

Configure the BDD Reviewer Agent to detect duplicate scenarios and step definitions, validate Gherkin quality, check test isolation, prevent fixed sleeps and hardcoded secrets, compile generated tests, and report coverage gaps.

All agents must reuse existing feature files, step definitions, scenario context, REST clients, Kafka utilities, assertions, hooks, configuration, and runners before creating new components.

All agents must use configurable polling for asynchronous behavior, read environment-specific values and JKS paths from external configuration or environment variables, never expose credentials, never connect to production systems, and never modify production code unless explicitly requested.

For this request, create only the five .agent.md files, show the files created, and stop without reading or changing src/main, src/test, pom.xml, build.gradle, requirements, OpenAPI files, or any other application files.
