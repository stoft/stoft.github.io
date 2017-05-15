# Principles

* Logging MUST include **what** happened.
* Logging MUST include **when** it happened.
* Logging MUST include **where** it happened.
* Logging SHOULD include **why** it happened.
* Logging SHOULD include **what** will happen **next**.
* Logging SHOULD include **with what** it happened.
* Logging SHOULD include to **whom** it happened.

Examples:

| ?        | Description     |
| ---------|-------------    |
| What     | Logging message, error message |
| When     | Timestamp (UTC pls) |
| Where    | e.g. Service.Module.function[.line] |
| Why      | Some background info |
| What Next | What the code will attempt to do now |
| With What | A blob containing e.g. the data being processed |
| Whom     | The carbon based lifeform that was cause and affected by the event |
