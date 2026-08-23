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

The Joshternet is an open, decentralized way for people who identify as Josh to declare their Joshness, connect their websites, and make it easier to discover other Joshes around the web.

It is intentionally built on boring web standards.

No accounts. No follower counts. No algorithm deciding which Josh is the most engaging Josh. No centralized Josh authority.

Just websites talking to websites.

**Joshness is declared, never derived.**

## How it works

A participating website can publish a Joshternet declaration at:

`/.well-known/josh`

For example:

`https://joshuamorris.info/.well-known/josh`

The file provides a machine-readable declaration that the site participates in the Joshternet.

That does not mean the Joshternet verified that someone is a Josh.

It means that Josh declared their own Joshness.

Important distinction.

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

The Joshternet is currently in the **PRE-JOSH** phase while we figure out what this thing actually needs to become.

RFCs are added when there is something worth specifying.

We are not reserving RFC numbers just to look organized.

## Implementations

[`joshuamorris.info`](https://joshuamorris.info/) is the first known operational implementation of RFC-JOSH-0002.

Its declaration is here:

`https://joshuamorris.info/.well-known/josh`

Being the first implementation does not make me the boss of the Joshternet.

That would be a fairly serious violation of the whole:

**No Josh outranks another Josh.**

thing.

## Participate

If you are a Josh and have a website, you can participate.

If you are not a Josh, you can participate too. You just cannot use the protocol to become a Josh.

That seems like a reasonable boundary.

The specifications are public. Issues and pull requests are welcome.

Build something.

Implement the RFC.

Point out something stupid in the specification.

Propose something better.

This is still an experiment, and the best way to figure out whether it works is for more Joshes to actually use it.

## Repositories

* [`joshternet/spec`](https://github.com/joshternet/spec) - specifications and RFCs
* [`joshternet/.github`](https://github.com/joshternet/.github) - organization profile and shared GitHub configuration

---

<p align="center">
  <strong>A decentralized network of Joshes.</strong>
</p>
