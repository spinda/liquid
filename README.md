* Clone Repository 

 1. Clone the repository: `git clone git://github.com/spinda/liquid.git`
 2. `cd` to the directory: `cd liquid`
 3. Switch to the `gsoc2015` branch: `git checkout gsoc2015 && git submodule sync && git submodule update --init`

* Stack Build

 1. Build everything: `stack build`
 2. Switch to the `liquidhaskell-core` directory: `cd liquidhaskell-core`
 3. Run a test (currently a bit complicated, will get better): `stack ghc -- -fplugin=LiquidHaskell.Plugin -fplugin-opt=LiquidHaskell.Plugin:verbose,no-prune,no-termination benchmarks/gsoc15/neg/test3.hs`

* Cabal Build
 
 1. Switch to the `liquidhaskell-core` directory: `cd liquidhaskell-core`
 2. Initialize the Cabal sandbox: `cabal sandbox init`
 3. Add sources to your sandbox: `cabal sandbox add-source ../liquid-fixpoint ../liquidhaskell ../liquidhaskell-std`
 4. Build everything: `cabal install`
 5. Configure environment: `cabal exec bash`
 6. Run a test: `ghc -fplugin=LiquidHaskell.Plugin -fplugin-opt=LiquidHaskell.Plugin:verbose,no-prune,no-termination benchmarks/gsoc15/neg/test3.hs`

* For now, make sure to clean up the `.hi`, `.o`, `.lqhi` files etc. between test runs.
