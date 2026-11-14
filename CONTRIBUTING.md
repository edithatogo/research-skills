# Contributing to research-skills

Contributions should make the documented research automation skills clearer, reproducible, and consistent with what is actually available in this repository.

## Before you start

Start with the [README](README.md). It describes literature search, evidence synthesis, writing, analysis, and collaboration capabilities. The current tree is a documentation scaffold: confirm that referenced adapters, integrations, and commands exist before describing them as implemented.

Search existing issues and pull requests to avoid duplicating work. Describe substantial proposals before implementation, and use repository issue or pull request templates when available. Small corrections can go directly into a focused pull request.

For bug reports, include the affected version or commit, environment, minimal reproduction, expected and actual behavior, and sanitized diagnostics. For feature requests, explain the use case and intended outcome.

## Development and validation

For documentation changes, preview the Markdown, check links and paths, and verify each example against the files available in the proposed change. The current repository has no checked-in package manifest or executable test suite. Do not report README examples as passing tests when their implementation is absent.

When adding an implementation, include its setup instructions, dependencies, bounded example, and reproducible validation in the same change. Use public or synthetic research fixtures with provenance. Keep search retrieval, screening decisions, statistical analysis, and manuscript claims distinguishable; a generated citation or synthesis is not evidence of source verification.

Update affected documentation and examples alongside behavior changes. Add a focused regression case for a bug fix where executable tests are appropriate. Record checks that were not run and the reason.

## Submitting a pull request

Create a focused branch from the current `main` branch and open a pull request back to it. Keep unrelated formatting, refactoring, and dependency changes separate.

Include:

- The problem, proposed change, and resulting behavior.
- Related issues or existing track references.
- Exact validation commands or inspection steps, results, and limitations.
- Compatibility implications and any data or dependency provenance.

Inspect the complete diff before submission. Required automated checks must pass before merge. Follow the existing repository and account policies; this guide does not introduce a second-person approval requirement or relax existing checks.

## Security and sensitive information

Follow the [account security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md). Report vulnerabilities privately through GitHub's **Report a vulnerability** option if available. Otherwise request a private reporting contact without disclosing the vulnerability publicly. Keep credentials, personal data, and unredacted logs out of commits, issues, and examples.

## Licensing and conduct

Preserve existing attribution and applicable source or package terms. This guide does not grant a new license. Submit only material you are entitled to contribute, and document unclear permissions before adding third-party content. Follow the [account code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md). This guide adds no CLA, mandatory sign-off, or relicensing condition.

## Reference guidance

- [GitHub contributor guidelines](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)
- [OpenSSF Best Practices criteria](https://www.bestpractices.dev/en/criteria)
