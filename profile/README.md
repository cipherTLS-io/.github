# CipherTLS

**CipherTLS** makes real OpenSSL verifiable, version-accurate, and safe for both humans and AI
agents — without hiding the binary, hallucinating flags, or handing secrets to a model.

Upstream OpenSSL moves fast, host machines routinely carry multiple conflicting TLS stacks (such as
macOS LibreSSL beside Homebrew OpenSSL, Python, Node, and `curl`), and unbounded AI agents in a
shell hallucinate flags, confuse inspection with trust validation, and leak private keys into
transcripts. CipherTLS separates **deterministic grounding** (immutable upstream manual snapshots,
exact binary probes, shell-free typed execution, and selective drift detection) from **optional
natural-language routing** (`aitls`) and **graded human labs** (`openssl-workshop`).

## Repositories

| Repo | What it does | Status |
|---|---|---|
| [core](https://github.com/cipherTLS-io/core) | Ground-truth Go engine — version-pinned OpenSSL docs, host stack probe, typed command bridge (`companion-result/v1`), drift detection, and program PRD | Public · scaffold + `M6.0` spike validated |
| `aitls` | AI-grounded companion CLI (`v0.1` `M6`/`M7`) and later operator inspection workbench (`M0`–`M3`) over unmodified OpenSSL | Private until `M6` preview |
| [openssl-workshop](https://github.com/cipherTLS-io/openssl-workshop) | Hands-on OpenSSL lessons graded on real artifacts against pinned releases, with drift revalidation | Public · scaffold (later scope after `M6`) |

## Status

Pre-0.1. **No working product release is published yet.** `core M6.0` (spike validation against
real OpenSSL 4.1.0, LibreSSL 3.3.6, and upstream `openssl-4.1.0` manuals) is validated; `M6.1`–`M6.4`
implementation is next. Independent, clean-room open source — no sponsorship or endorsement by the
OpenSSL Foundation is claimed. One maintainer (`veronaimars`).

## Where to start

- [Program map](https://github.com/cipherTLS-io/core/blob/main/docs/program.md) and
  [PRD](https://github.com/cipherTLS-io/core/blob/main/docs/PRD.md) — unified mission, requirements,
  and repository boundaries.
- [M6.0 spike findings](https://github.com/cipherTLS-io/core/blob/main/docs/findings-m6.md) — real
  measurements, frozen resource limits, and `companion-result/v1` schema.
- [Limitations](https://github.com/cipherTLS-io/core/blob/main/docs/user/limitations.md) — what
  CipherTLS deliberately does not do and has not built yet.
- [Contributing](https://github.com/cipherTLS-io/core/blob/main/CONTRIBUTING.md),
  [governance](https://github.com/cipherTLS-io/core/blob/main/GOVERNANCE.md), and
  [security reporting](https://github.com/cipherTLS-io/core/blob/main/SECURITY.md).

## License

Apache-2.0. Copyright The CipherTLS Authors. See [LICENSE](../LICENSE).
