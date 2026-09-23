Act as a senior Java BDD automation engineer and analyze the selected requirement document, OpenAPI specification, or REST API source code.
Identify the endpoint path, HTTP method, request DTO, response DTO, validation rules, authentication requirements, exception handling, and expected HTTP responses.
Generate executable Cucumber feature files covering applicable positive, negative, boundary, authentication, authorization, malformed-request, unsupported-content-type, resource-not-found, and business-error scenarios.
Use REST Assured to invoke the REST API and validate the HTTP status code, response headers, content type, response body, JSON paths, JSON schema, error code, error message, and correlation identifier.
Generate reusable Java step definitions, a REST API client, scenario context, request-payload utilities, response assertions, Cucumber hooks, configuration, and a JUnit 5 test runner.
Use Scenario Outline and Examples for field validation and boundary cases, and store complex request payloads in reusable JSON files instead of embedding large JSON strings in Java code.
Analyze existing feature files and step definitions before generating code, reuse existing steps and utilities, and create only the missing scenarios and implementation.
Do not validate MySQL, GemFire, Kafka producers, Kafka consumers, database records, cache entries, or Kafka messages in this initial version.
Read base URLs, authentication details, timeouts, and environment-specific values from environment variables or external test configuration, and never hardcode credentials, tokens, or production URLs.
Compile and execute the relevant tests when the environment is available, correct generation-related errors, and provide a final report listing changed files, scenario coverage, requirement traceability, assumptions, compilation results, and test-execution results.

Start with the selected REST API only and do not analyze unrelated APIs or downstream MySQL, GemFire, and Kafka implementation classes.
