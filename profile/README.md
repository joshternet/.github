<p align="center">
  <img
    src="../assets/joshternet-logo.png"
    alt="Joshternet logo"
    width="760"
  />
</p>

<p align="center">
  <strong>Open standards for connecting Joshes across the web.</strong>
</p>

<p align="center">
  <strong>Network status: PRE-JOSH</strong>
</p>

# The Joshternet

There are a surprising number of Joshes on the internet.

A lot of them have interesting personal websites.

So naturally, we needed a protocol.

The Joshternet is an open, decentralized network for people who identify as Josh and the independent websites they call home.

It lets independently operated sites declare participation and, optionally, Josh identity without moving everyone onto another platform.

It is intentionally built on boring web standards.

No accounts. No follower counts. No algorithm deciding which Josh is the most engaging Josh. No centralized Josh authority.

Just websites talking to websites.

**Joshness is declared, never derived.**

Project website: [joshternet.org](https://joshternet.org/)

## How it works

A participating origin publishes a Joshternet declaration at:

`/.well-known/josh`

For example:

`https://joshuamorris.info/.well-known/josh`

The minimum version 1 declaration is:

```json
{
  "version": 1
}
```

Publishing a valid declaration establishes participation for that origin.

Josh identity is separate and optional:

```json
{
  "version": 1,
  "josh": true
}
```

- `josh: true` means **Affirmed Josh Identity**.
- `josh: false` means **Declined Josh Identity**.
- omitting `josh` means **Undeclared Josh Identity**.

Participation does not imply Josh identity, and the protocol does not infer Joshness from a person's name, domain, biography, or website content.

**Joshness is declared, never derived.**

## The rules

There are not many.

* Joshness is declared, never derived.
* Participation is voluntary.
* Identity and participation are separate.
* A Josh controls their own website and infrastructure.
* No Josh gets to declare somebody else a Josh.
* No Josh outranks another Josh.
* Participation does not imply trust.
* The network should work without JavaScript.
* Open web standards are preferred over proprietary infrastructure.
* Running a personal website should be enough to participate.

The goal is to keep this simple enough that someone with a static HTML page can participate just as easily as someone running an unnecessarily complicated Kubernetes cluster.

## Specifications

The Joshternet is being defined through RFCs in the [`joshternet/spec`](https://github.com/joshternet/spec) repository.

Current drafts:

| RFC                                                                                        | Title               | Status |
| ------------------------------------------------------------------------------------------ | ------------------- | ------ |
| [RFC-JOSH-0000](https://github.com/joshternet/spec/blob/main/rfcs/0000-the-joshternet.md)  | The Joshternet      | Draft  |
| [RFC-JOSH-0001](https://github.com/joshternet/spec/blob/main/rfcs/0001-josh-identity.md)   | Josh Identity       | Draft  |
| [RFC-JOSH-0002](https://github.com/joshternet/spec/blob/main/rfcs/0002-well-known-josh.md) | `/.well-known/josh` | Draft  |

Nothing has been accepted yet.

RFCs are added when there is something worth specifying.

We are not reserving RFC numbers just to look organized.


## Current state

The Joshternet is currently **PRE-JOSH**.

All three current RFCs are Drafts. None have been Accepted.

Known operational RFC-JOSH-0002 version 1 implementations include:

- [`joshuamorris.info`](https://joshuamorris.info/) — Affirmed Josh Identity
- [`joshternet.org`](https://joshternet.org/) — Undeclared Josh Identity

Their declarations are available at:

- `https://joshuamorris.info/.well-known/josh`
- `https://joshternet.org/.well-known/josh`

These implementations demonstrate that participation and Josh identity are separate. Neither implementation is an authority or privileged node.

[JoshBot](https://github.com/joshternet/joshbot) is the Joshternet discovery, verification, and public registry crawler. Its first supported release is [v1.0.0](https://github.com/joshternet/joshbot/releases/tag/v1.0.0).

JoshBot can discover candidate origins, verify their declarations, and produce public registry data. It is implementation infrastructure; it does not define participation or Josh identity.

## Participate

If you are a Josh and have a website, you can participate and affirm Josh identity.

If you are not a Josh, you can participate without being represented as a Josh.

You may also participate while leaving Josh identity undeclared.

The [implementation guide](https://joshternet.org/implement/) explains how to publish a version 1 declaration.

The specifications are public. Issues and pull requests are welcome.

Build something.

Implement the RFC.

Point out something stupid in the specification.

Propose something better.

This is still an experiment, and the best way to figure out whether it works is for more Joshes to actually use it.

## Repositories

* [`joshternet/spec`](https://github.com/joshternet/spec) - canonical specifications and RFCs
* [`joshternet/joshbot`](https://github.com/joshternet/joshbot) - discovery, verification, and public registry crawler
* [`joshternet/joshternet.github.io`](https://github.com/joshternet/joshternet.github.io) - source for [joshternet.org](https://joshternet.org/)
* [`joshternet/.github`](https://github.com/joshternet/.github) - organization profile and shared GitHub configuration

---

<p align="center">
  <strong>A decentralized network of Joshes.</strong>
</p>
