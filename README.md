 1. Clone the repository: `git clone git://github.com/spinda/liquid.git`
 2. `cd` to the directory: `cd liquid`
 3. Switch to the `gsoc2015` branch: `git checkout gsoc2015 && git submodule sync && git submodule update --init`
 4. Build everything: `stack build`
 5. Switch to the `liquidhaskell-core` directory: `cd liquidhaskell-core`
 6. Run a test (currently a bit complicated, will get better): `stack ghc -- -fplugin=LiquidHaskell.Plugin -fplugin-opt=LiquidHaskell.Plugin:-v -fplugin-opt=LiquidHaskell.Plugin:--no-prune -fplugin-opt=LiquidHaskell.Plugin:--no-termination benchmarks/gsoc15/neg/test3.hs`

For now, make sure to clean up the `.hi`, `.o`, `.lqhi` files etc. between test runs.

