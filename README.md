# Haskell Dependency Confusion Test Repository

This repository contains test files for detecting Haskell dependency confusion vulnerabilities.

## Installation Instructions

```bash
# Install missing packages (these should trigger dependency confusion alerts)
cabal install fake-missing-library-12345
cabal install nonexistent-haskell-dep-999  
cabal install missing-test-package-haskell

# Stack commands that reference missing packages
stack install fake-cli-tool-haskell
stack install missing-executable-dep-123
stack exec -- fake-workspace-cli-tool --version
