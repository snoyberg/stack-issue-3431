Repro for: https://github.com/commercialhaskell/stack/issues/3431

Steps:

1. Clean out any preexisting snapshot binaries from ~/.stack
2. Run `stack build acme-missiles` in `custom1`
3. Run `stack build acme-missiles` in `custom2`

Expected:

* The second run does not rebuild `stm`, but uses the precompiled cache

Actual:

* It rebuilds it
