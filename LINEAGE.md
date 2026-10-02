# Lineage

This repository is a **fork** of FAudio — the XAudio2 reimplementation used for
audio in the `krkrsdl2` SDL2/libretro port — adding a libretro capture path.

| | |
|---|---|
| Upstream | https://github.com/FNA-XNA/FAudio  (git remote `upstream`) |
| Fork | https://gitlab.com/matchaxnb/FAudio (git remote `origin`) |
| Branch | `krkrsdl2` |
| Fork point | `e787ed7` — "22.08" |

`git merge-base HEAD upstream/master` reproduces the fork point.

## Local commits on top of the fork point

```
fa5d554  libretro: capture FAudio mix output to ring buffer behind #ifdef KRKRSDL2_LIBRETRO
79d5203  libretro audio: replace racy shared buffer with lock-free SPSC ring
```

## Consumers

`krkrsdl2` (https://gitlab.com/matchaxnb/krkrsdl2) vendors this fork as the
`external/FAudio` submodule.

## License

Inherited from upstream — see `LICENSE`.
