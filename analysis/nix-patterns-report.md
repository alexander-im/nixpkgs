# Nix file corpus analysis

- Total `.nix` files analyzed: **42389**

## Top Nix keywords (token frequency)
- `true`: 67810
- `with`: 52311
- `in`: 30814
- `inherit`: 22451
- `false`: 20017
- `if`: 15459
- `null`: 14307
- `rec`: 13944
- `let`: 13571
- `then`: 11391
- `else`: 9055
- `or`: 8673
- `builtins`: 4265
- `import`: 3142
- `assert`: 2883

## Top function-like call tokens (heuristic)
- `fetchFromGitHub`: 25207
- `callPackage`: 20990
- `mkDerivation`: 19630
- `rec`: 13925
- `stdenv.mkDerivation`: 11730
- `fetchurl`: 11077
- `inherit`: 10050
- `lib.mkOption`: 8793
- `mkOption`: 8049
- `build-asdf-system`: 4709
- `createAsd`: 4689
- `in`: 4482
- `nix-update-script`: 3435
- `fetchPypi`: 3262
- `machine.succeed`: 3197
- `lib.optionalString`: 3157
- `fetchpatch`: 2814
- `lib.optionals`: 2782
- `buildGoModule`: 2553
- `rustPlatform.buildRustPackage`: 2437
- `subtest`: 1978
- `buildVimPlugin`: 1808
- `cfg.enable`: 1651
- `elpaBuild`: 1531
- `lib.optional`: 1521
- `buildPerlPackage`: 1517
- `map`: 1485
- `buildPythonPackage`: 1461
- `fetchFromGitLab`: 1155
- `stdenvNoCC.mkDerivation`: 1070

## Top assigned attribute names
- `version`: 79457
- `description`: 74757
- `pname`: 68208
- `license`: 61604
- `src`: 46172
- `meta`: 44702
- `sha256`: 43354
- `hash`: 39377
- `homepage`: 35878
- `maintainers`: 32184
- `owner`: 27235
- `repo`: 27010
- `url`: 23607
- `type`: 23315
- `platforms`: 22233
- `mainProgram`: 19223
- `nativeBuildInputs`: 18567
- `libraryHaskellDepends`: 17620
- `name`: 17027
- `hydraPlatforms`: 16276
- `default`: 15317
- `rev`: 15065
- `buildInputs`: 14526
- `tag`: 13173
- `changelog`: 11514
- `dependencies`: 9634
- `pyproject`: 8987
- `broken`: 8834
- `pythonImportsCheck`: 8709
- `source`: 8281

## Reusable packaging/configuration patterns (counts)
- `files_with_callPackage`: 1178
- `files_with_fetchFromGitHub`: 22050
- `files_with_function_argset_header`: 40049
- `files_with_meta_attrset`: 35246
- `files_with_mkDerivation`: 15496
- `files_with_stdenv.mkDerivation`: 13355
- `token_occurrences::buildGoModule`: 5693
- `token_occurrences::buildPythonPackage`: 19303
- `token_occurrences::callPackage`: 39118
- `token_occurrences::fetchFromGitHub`: 47484
- `token_occurrences::fetchgit`: 884
- `token_occurrences::fetchurl`: 18734
- `token_occurrences::lib.mkIf`: 3031
- `token_occurrences::lib.mkMerge`: 361
- `token_occurrences::lib.optional`: 22923
- `token_occurrences::lib.optionalAttrs`: 1495
- `token_occurrences::lib.optionals`: 9413
- `token_occurrences::mkDerivation`: 55001
- `token_occurrences::override`: 7154
- `token_occurrences::overrideAttrs`: 1777
- `token_occurrences::runCommand`: 2453
- `token_occurrences::rustPlatform.buildRustPackage`: 2560
- `token_occurrences::stdenv.mkDerivation`: 13756
- `token_occurrences::writeShellScriptBin`: 284

## Notes on method
- Counts are lexical/regex-based heuristics across all `.nix` files.
- Function-like tokens are names followed by `{` or `(`; this includes some non-call constructs and therefore represents practical usage patterns, not an AST-accurate call graph.
- Comment text (`# ...`) was removed for token-level stats to reduce noise.