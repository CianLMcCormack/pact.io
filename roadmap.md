# Roadmap

Pact is an open source initiative and relies on the personal contributions of many individuals. This means that providing fixed dates for features is all but impossible.

That being said, although each language will move at a different pace, as a community we are moving in the same direction.

## Table of Contents

* [Specification \[Status: v3\]](roadmap.md#specification-status-v3)
* [Reference Library \[Status: Alpha\]](roadmap.md#reference-library-status-alpha)
* [Python \[Status: v2\]](roadmap.md#python-status-alpha)
* [Node/JS \[Status: v2\]](roadmap.md#nodejs-status-v2)
* [Golang \[Status: v2\]](roadmap.md#golang-status-v2)

## Aggregated development board

Dashboard: [https://huboard.com/pact-foundation/pact-specification](https://huboard.com/pact-foundation/pact-specification)

Pact is comprised of many projects in different languages. Visualising all of the parallel development and the roadmap is challenging.

To ease this, we are experimenting with an aggregated dashboard that brings together multiple projects into a single view.

We hope this helps make our efforts more transparent, and encourages better collaboration across the many Pact authors and contributors.

## Specification \[Status: v3\]

The [Pact Specification](https://github.com/pact-foundation/pact-specification/) outlines the features each major version of a release should contain for interoperability between languages. The most current approved version is v3.

## Reference Library \[Status: Alpha\]

One of the key advantages of Pact is that its DSL is native to each language, resulting in seamless toolchain integration. This is also its biggest challenge - with any change to the specification, each language has to implement the complex matching and verification logic for the Consumer and Provider DSLs.

The Pact Community has come together to solve this problem. Our plan is to create a native, [embedded library](https://github.com/pact-foundation/pact-reference/) in Rust with a well-defined native interface that each language can pull in to perform common functions such as:

* Running a Mock Service
* Performing matching logic
* Verifying Pacts

This project is well underway with proof-of-concepts in JS and Golang, v3 matching and consumer lib complete.

## Python \[Status: Alpha\]

We've had a large amount of interest from the community in a Python version of Pact, and it now has its beginnings at the [Pact Python](https://github.com/pact-foundation/pact-python) GitHub repository.

Two contributors - Matthew Belvanz and Jose Salvatierra - will be leading this initiative.

Our current plan to a `v1.0.0` release looks as follows:

* Review DSL for compatibility / consistency with other official implementations
* Remove the requirement for Docker, pulling in the Mock Server and Verifier Ruby libraries instead \(as per JS/Golang implementations\) until such time as the native library becomes viable
* Implement Provider side verification
* Release v1.0.0 🎉

## Node/JS \[Status: v2\]

## Golang \[Status: v2\]

Golang is in the same boat as the JavaScript community in that it uses Ruby 'binaries' under the hood. We are working toward a release where we remove this dependency in favour of the reference library above. Whilst it is currently functional to v2 of the specification, the API is subject to change.

