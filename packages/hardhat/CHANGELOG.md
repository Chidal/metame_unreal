# @typechain/hardhat

## 9.1.0

### Minor Changes

- da71c45: Allow passing node16Modules flag to TypeChain

### Patch Changes

- Updated dependencies [3469800]
  - typechain@8.3.2
  - @typechain/ethers-v6@0.5.1

## 9.0.0

### Patch Changes

- Updated dependencies [04ebda9]
- Updated dependencies [64d18f7]
  - @typechain/ethers-v6@0.5.0

## 8.0.3

### Patch Changes

- Updated dependencies [9107713]
  - typechain@8.3.1
  - @typechain/ethers-v6@0.4.3

## 8.0.2

### Patch Changes

- Updated dependencies [c4720b9]
  - typechain@8.3.0
  - @typechain/ethers-v6@0.4.2

## 8.0.1

### Patch Changes

- c2b3f1b: Support for the newest hardhat-ethers version
- Updated dependencies [c2b3f1b]
- Updated dependencies [cd4bb0f]
  - @typechain/ethers-v6@0.4.1
  - typechain@8.2.1

## 8.0.0

### Major Changes

- 2380a8f: Added support for ethers v6 in @typechain/hardhat

### Patch Changes

- Updated dependencies [2380a8f]
  - @typechain/ethers-v6@0.4.0

## 7.0.0

### Patch Changes

- Updated dependencies [3eb6ed6]
- Updated dependencies [15541e4]
  - @typechain/ethers-v5@11.0.0
  - typechain@8.2.0

## 6.1.6

### Patch Changes

- Updated dependencies [5b0759d]
- Updated dependencies [a036651]
  - @typechain/ethers-v5@10.2.1

## 6.1.5

### Patch Changes

- Updated dependencies [31e6957]
  - @typechain/ethers-v5@10.2.0

## 6.1.4

### Patch Changes

- Updated dependencies [bbc9656]
  - typechain@8.1.1
  - @typechain/ethers-v5@10.1.1

## 6.1.3

### Patch Changes

- dc5ede9: Reduce the time it takes to load the plugin by importing every library only when needed

## 6.1.2

### Patch Changes

- ed6f85b: Don't autodisable overrides for js projects
- 1663b98: Respect the `--quiet` flag

## 6.1.0

### Minor Changes

- 63691c4: - Expose `TypechainUserConfig` type.
  - Removed `contractName` from interface output see #692 for details.

### Patch Changes

- de656c6: Add `dontOverrideCompile` setting
- Updated dependencies [63691c4]
- Updated dependencies [015abb2]
  - typechain@8.1.0
  - @typechain/ethers-v5@10.1.0

## 6.0.0

### Major Changes

- 3a8a99a: Directory tree in generated types now reflects the directory tree in the inputs. Also, only the main contract
  type is reexported from each file.

  This change solves a number of name clashing problems. All generated code can still be imported after updating the
  import path.

- 978490f: ## What's breaking:

  We are not emitting `contractName` fields on contracts and factories anymore.

  ## Why?

  `contractName` breaks polymorphism for example: exact token implementation is not assignable to token interface.

  ## What do to?

  We are adding optional flag `--discriminate-types` to continue emitting `contractName`.

### Minor Changes

- a59ae6e: Prefer `import type` in generated files when possible

### Patch Changes

- Updated dependencies [3a8a99a]
- Updated dependencies [5b9a7fb]
- Updated dependencies [d86d048]
- Updated dependencies [2395289]
- Updated dependencies [e447bfb]
- Updated dependencies [978490f]
- Updated dependencies [a59ae6e]
- Updated dependencies [47ab651]
- Updated dependencies [975a9dc]
- Updated dependencies [e1f832c]
  - @typechain/ethers-v5@10.0.0
  - typechain@8.0.0

## 5.0.0

### Major Changes

- fd3a524: Update internal task name to match hardhat convention

## 4.0.0

### Patch Changes

- Updated dependencies [92939ea]
- Updated dependencies [d244e41]
  - typechain@7.0.0

## 3.1.0

### Minor Changes

- 5f81ca9: Using `--ts-nocheck` (`config.tsNocheck`) flag, you can now add `// @ts-nocheck` comment in case where code
  generated by TypeChain doesn't pass typechecking.

  Read more in [TypeScript docs][tsdocs].

  [tsdocs]:
  (https://www.typescriptlang.org/docs/handbook/release-notes/typescript-3-7.html#-ts-nocheck-in-typescript-files)

## 3.0.0

### Major Changes

- 99fafbe: Change default output directory to "typechain-types"
- 0e555af: Generate types to `.ts` files instead of `.d.ts` in Ethers v5 and Web3.js targets

### Patch Changes

- aacdcb0: Export EventFilter type along with Event type
- Updated dependencies [0ac4921]
- Updated dependencies [95517e9]
- Updated dependencies [33ee803]
  - typechain@6.0.0

## 2.3.1

### Patch Changes

- c93a1e7: Fixed generated contract factory constructors to accept 3 parameters when called from ContractFactory methods
  (`this.constructor(interface, bytecode, signer)`).

  Fixes https://github.com/dethcrypto/TypeChain/issues/487

## 2.3.0

### Minor Changes

- 99ce3e3: Move type generation to Hardhat subtask for easier third-party integration

## 2.2.0

### Minor Changes

- 21a5062: Always use hardhat project root as cwd while generating types. All paths in the config are now always
  relative to the project root as well.

## 2.1.2

### Patch Changes

- 5ed62e4: Ensure that `type-extensions.ts` is always imported

## 2.1.1

### Patch Changes

- 5980201: Expose `TASK_TYPECHAIN` constant

## 2.1.0

### Minor Changes

- 22134ac: Support compilation of external artifacts (from node_modules)

## 2.0.2

### Patch Changes

- e552df9: Add missing dependency on `fs-extra`

## 2.0.1

### Patch Changes

- b705685: Fix bug which caused targets not supporting incremental generation to misbehave when editing files
- 30c4565: Add ability to run custom targets with hardhat

## 2.0.0

### Minor Changes

- 62b9e08: Type `getContractFactory` calls
- 62b9e08: Support incremental generation

### Patch Changes

- Updated dependencies [d60a343]
- Updated dependencies [5a60d00]
- Updated dependencies [d60a343]
  - typechain@5.0.0

## 1.0.1

### Patch Changes

- 23faae4: Accept underscores in contract names

## 1.0.0

### Major Changes

- cd8b04b: Initial release