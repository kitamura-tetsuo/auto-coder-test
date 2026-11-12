# Auto-Coder disposable acceptance source

This repository is a disposable test fixture for auto-coder PR #2835 / Issue #2608.
It must not be connected to production release or beta workers, production Git
refs, real provider automation, or production management OAuth credentials.

Only these GitHub Actions workflows are included:

- Test Source for Runtime (GitHub-hosted source tests)
- Publish Tested Source (immutable test-repository ref)
- Advance Beta Source (manual, test-repository ref only)
- Promote Accepted Source Release (manual, test-repository ref only)

The source release policy is scoped to `kitamura-tetsuo/auto-coder-test` and
its disposable beta instance. Any missing authenticated producer or policy
proof must be reported as BLOCKED, never represented as an acceptance PASS.
