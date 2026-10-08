# Security Policy

This policy covers every repository of the TUWA organization, the `@tuwaio` npm packages, Quasar Cloud (`api.tuwa.io`, `quasar.tuwa.io`) and Quasar Community Edition.

## Reporting a Vulnerability

Please **do not open a public issue, discussion or pull request** for a vulnerability. Email **[security@tuwa.io](mailto:security@tuwa.io)** instead, with:

- the affected package and version, or the service and endpoint;
- the steps to reproduce the issue, or a proof of concept;
- the impact you see (for example, which data or funds are at risk).

You will get a reply at the address you wrote from. The fix is released first, and the details are published after it, with credit to you if you want it.

## Supported Versions

Fixes are released for the latest version of each `@tuwaio` package and of Quasar Community Edition. Quasar Cloud is always on the latest version.

## Scope Notes

- TUWA packages never ask for, receive or store private keys. A report that a package leaks a key or signs something the user did not approve is always in scope.
- Third-party services (RPC providers, wallets, WalletConnect, Gelato, Pimlico) are out of scope; report their issues to them.
