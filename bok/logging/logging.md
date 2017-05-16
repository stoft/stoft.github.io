# Principles

* Logging MUST include **what** happened.
* Logging MUST include **when** it happened.
* Logging MUST include **where** it happened.
* Logging SHOULD include **why** it happened.
* Logging SHOULD include **what** will happen **next**.
* Logging SHOULD include **with what** it happened.
* Logging SHOULD include to **whom** it happened.
* Logging MAY include in **which context** it happened.


# Description

| ?        | Description     |
| :-------:|-------------    |
| What     | Log message<br/>Error message<br/> |
| When     | Timestamp (UTC or with TZ) |
| Where    | Host machine/instance<br/>Service.Module.function[.line] |
| Why      | Some background info |
| What Next | What the code will attempt to do now |
| With What | A blob containing e.g. the data being processed |
| Whom     | The carbon based lifeform that was cause and affected by the event |
| Which Context | The overall context of the log, if possible/available.|

# Examples

## Combined Log Format

Nginx:

`123.65.150.10 - - [23/Aug/2010:03:50:59 +0000] "POST /wordpress3/wp-admin/admin-ajax.php HTTP/1.1" 200 2 "http://www.example.com/wordpress3/wp-admin/post-new.php" "Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10_6_4; en-US) AppleWebKit/534.3 (KHTML, like Gecko) Chrome/6.0.472.25 Safari/534.3"`

| ?   | Log |
|:---:| --- |
| What | `"POST /wordpress3/wp-admin/admin-ajax.php HTTP/1.1" 200 2` |
| When | `[23/Aug/2010:03:50:59 +0000]` |
| Where | (This would be gotten from the hostname where the log was generated.) |
| Why | - |
| What Next | - |
| With What | (The request body was not logged.) |
| Whom | `123.65.150.10 - -` |
| Which Context | Referrer and browser agent in this case: <br/>`"http://www.example.com/wordpress3/wp-admin/post-new.php" "Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10_6_4; en-US) AppleWebKit/534.3 (KHTML, like Gecko) Chrome/6.0.472.25 Safari/534.3"`  |
