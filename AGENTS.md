# Working on Parsley.js

This is the legacy 1.x form validator. Core/extension JavaScript lives at the
root, translations in `i18n/`, tests in `tests/`, and generated bundles in `dist/`.
Per README, add new validators in `parsley.extend.js`; use the French translation
as the reference for localization. Add/update coverage in `tests/tests.js`.

README setup uses `bower install jquery` and `bower install bootstrap`.
Browser tests run through `tests/index.html`; with mocha-phantomjs installed,
`./bin/test-suite.sh` checks the standard, minified-jQuery, Zepto, minified-Zepto,
and standalone variants. Historical CI uses Node 0.6; report legacy-tool blockers
instead of silently migrating the toolchain.

`./bin/build.sh <version>` requires Ruby and closure-compiler and writes `dist/`.
Use the requested development version for intentional bundle updates; do not
invent a release version. No package-based lint/typecheck script is present.

## Completing changes

Follow existing patterns and carry authorized work through the relevant checks,
repairing failures caused by the change. Choose routine implementation details
directly; ask only when missing information materially changes scope or outcome.
For documentation-only edits, check the diff, referenced paths, and command
accuracy rather than starting application runtimes. If a prerequisite blocks a
check, report the exact blocker and continue independent authorized work. Close
with changed paths, checks actually run and results, and remaining unverified
behavior; distinguish commands inspected from commands executed.
