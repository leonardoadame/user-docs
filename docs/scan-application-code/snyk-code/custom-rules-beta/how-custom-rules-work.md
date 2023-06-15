# How custom rules work

## Query language

Snyk Code custom rules use a proprietary declarative query language based on logic programming, more specifically, Datalog.&#x20;

The goal is to create useful queries that will surface valuable and actionable results, helping security teams and developers focus on the most important vulnerabilities within their code.

## Components

### Query templates

The templates are abstract pre-built constructs created to provide a quicker and easier way to build queries.

<figure><img src="../../../.gitbook/assets/query templates.png" alt="Overview of Query Templates."><figcaption><p>Query Templates</p></figcaption></figure>

### Query predicates

The predicate is a symbolic representation of a relationship between objects or properties that evaluates true or false. Snyk provides an exhaustive list of predefined predicates.&#x20;

For example, all cross-site scripting (XSS) sinks as `PRED:XssSink`. You can extend these or define your own.&#x20;

<figure><img src="../../../.gitbook/assets/query predicates.png" alt="Overview of Query Predicates."><figcaption><p>Query Predicates</p></figcaption></figure>

### Source

Sources are entry points for data input and can potentially be controlled by a user or an environment. In many cases, the source should be assumed as tainted.&#x20;

### Sanitizer

Sanitizers are used to sanitize data input from users or environments, ensuring the data is not tainted. By performing this sanitization, you remove the risk of tainted data being consumed by a sink.&#x20;

### Sink

Sinks are points where data is consumed. If the consumed data is tainted it could result in a vulnerability within your application.&#x20;

## Hosting rules

Custom rules will utilize the `.snyk` file - whenever a repository is imported, this file will be picked up as part of the regular caching process.&#x20;

Given a `.snyk` file has custom rules within it, whenever a scan is run - these rules will run adjacent to the regular Snyk in-house rules and provide results as any other rules would.

## Custom rules behavior&#x20;

Snyk Code custom rules work as any other rule. Snyk Code parses your code to create an Abstract Syntax Tree (AST), which is analyzed to create an Event Graph_._&#x20;

_A_ll Snyk Code rules, including custom rules, run against the Event Graph, where any match is considered a vulnerability and surfaced to your developers or security teams.

A vulnerability is removed and added to the resolved issues section within the reporting tab when it has been addressed.

:link: [The .snyk file](../../../snyk-cli/test-for-vulnerabilities/the-.snyk-file.md)

## Suggestive AI support

Snyk Code offers a user-friendly development environment that uses AI technology to simplify the process of defining and testing rules. The AI acts as an intuitive assistant, providing helpful suggestions for queries based on the code you are testing.

For example, you can use the  `DataFlowsInto` [query template](how-custom-rules-work.md#query-templates) if you need to locate a method that data flows into. The AI will then suggest methods within your code where data flows into them based on the Event Graph. This streamlines the process of creating rules and may also spark new query ideas.

<figure><img src="../../../.gitbook/assets/suggestive_ai_support (1).gif" alt="Suggestive AI support"><figcaption><p>Suggestive AI support</p></figcaption></figure>



