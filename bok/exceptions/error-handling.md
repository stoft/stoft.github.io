# Principles

This document makes no real distinction between exceptions and errors.

* Errors SHOULD be classified as close to the source as possible.
* Errors SHOULD be re-thrown to a higher level of abstraction/context and handled there.
* Errors SHOULD never be used to handle normal flows.
