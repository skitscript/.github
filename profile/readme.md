
<h1 align="center"><img src="../logo.png" alt="Skitscript"></h1>

A simple document format which reads like a stage play and plays like a visual novel.

## Simple Example

```skitscript
Mr. Example enters rapidly.

Mr. Example (excitedly):
  This how you deliver a line!

~ The Start ~

Mr. Example:
  And this is a menu:

> Option A leads to Section A.
> Option B leads to Section B.

~ Section A ~

Mr. Example is ponderous.

Mr. Example:
  You've entered Section A.

Jump to The Start.

~ Section B ~

Mr. Example exits meekly.

Mr. Example:
  You've entered Section B.

Mr. Example enters jubilantly.

Jump to The Start.
```

## Tooling

The language is designed to be implementation-independent, able to be embedded
in other environments (such as existing game engines), so there is not a single
"interpreter" tool like most visual novel engines.

### Specification

A specification for the language itself can be found
[here](https://github.com/skitscript/specification).

### IDE Support

Extensions to add syntax highlighting, error checking, etc. to existing IDEs.

- [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=skitscript.skitscript).

### Parsers

A parser will take a plain text document and transform it into a list of
instructions, but not execute it.  Most error checks are possible at this stage.

- [NodeJS](https://www.npmjs.com/package/@skitscript/parser-nodejs).

### Interpreters

An interpreter will take a previously parsed document and step through it one
"prompt" at a time (e.g. a line or menu).  Some error checks (e.g. infinite
loops) cannot be performed prior to this stage.

- [NodeJS](https://www.npmjs.com/package/@skitscript/interpreter-nodejs).

### Mappers

A mapper will take a previously parsed document and generate a full list of
every possible state the game can be in.  This can be useful in that it can
produce an exhaustive list of every reachable character, emote, background, etc.

- [NodeJS](https://www.npmjs.com/package/@skitscript/mapper-nodejs).

### Test Suites

The test suites are standardized across all platforms to ensure that they remain
consistent with one another.

- [Parser](https://github.com/skitscript/parser-test-suite).
- [Interpreter](https://github.com/skitscript/interpreter-test-suite).
- [Mapper](https://github.com/skitscript/mapper-test-suite).

## Project History/Attribution Complexities

Although this project is currently primarily attributed to
[siliconspecter](https://github.com/siliconspecter), earlier versions were
actually created by a number of developers.

Some of said developers did not want it to be publicly known that they had
contributed, so the project was originally published as though it was the work
of a single developer.

The project since stalled and
[siliconspecter](https://github.com/siliconspecter) took over as maintainer in
2024.  By request of the original developers, their account is now the
"single contributor".
