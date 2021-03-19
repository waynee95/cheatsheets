# Nix

## Run temporary fhsChrootEnv

Runs FHS-compatible lightweight sandbox.

See https://nixos.org/nixpkgs/manual/#sec-fhs-environments

```bash
$ nix-build -E '(import <nixpkgs> {}).buildFHSUserEnv {name = "fhs"; targetPkgs = pkgs: (with pkgs; []); }'
$ ./result/bin/fhs
```

## Uninstall package

```bash
$ nix-env --uninstall firefox
$ nix-collect-garbage
```

## Install package from unstable while running stable

```bash
$ nix-channel --add https://nixos.org/channels/nixos-unstable unstable
$ nix-channel --update
$ nix-channel --list
```

And then install via `nix-env -iA unstable.<package_name>`.

## Search for package

```bash
nix-env -qaP | grep gitea
nixos.gitea                   gitea-1.9.4
unstable.gitea                gitea-1.9.5
```

## Upgrade NixOS

```bash
[root] nixos-rebuild switch --upgrade
```

Run as root or use sudo.

## Nix environment file

See https://maybevoid.com/posts/2019-01-27-getting-started-haskell-nix.html

```nix
{ nixpkgs ? import <nixpkgs> {} }:
let
  inherit (nixpkgs) pkgs;
  inherit (pkgs) haskellPackages;

  haskellDeps = ps: with ps; [
    base
    lens
    mtl
  ];

  ghc = haskellPackages.ghcWithPackages haskellDeps;

  nixPackages = [
    ghc
    pkgs.gdb
    haskellPackages.cabal-install
  ];
in
pkgs.stdenv.mkDerivation {
  name = "env";
  buildInputs = nixPackages;
}
```

## References

- [Nix Manual](https://nixos.org/manual/nix/stable/)
