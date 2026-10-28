# Custom HGSS modding workspace

This is the working development branch for our custom Pokémon HeartGold/SoulSilver project.

## Repositories and branches

- Original upstream: https://github.com/ClickingMaster/pokeheartgold-single-screen
- Our fork: https://github.com/Scraxemas/pokeheartgold-single-screen
- `main`: preserve as a clean upstream-aligned baseline.
- `modding-dev`: our integration and experimental work. Prefer feature branches and PRs for substantial changes.

## First milestone: baseline verification

1. Clone this fork and check out `modding-dev`.
2. Read upstream [README.md](../README.md) and [INSTALL.md](../INSTALL.md) before installing anything.
3. Obtain **your own legally acquired USA SoulSilver ROM**, compatible Metrowerks `mwccarm` and Nitro SDK. None of these may be uploaded to the repository.
4. On Windows, follow upstream's supported setup path and record tool versions. The single-screen build's documented/tested target is **SoulSilver USA**.
5. Reproduce an unmodified build and run it before making gameplay modifications.
6. Record build issues and the verified setup in a separate guide, without publishing proprietary materials.

This is a source project and is **not** a ready-to-run native PC game. The upstream `ssrecomp` project is a separate recompilation frontend and has its own constraints.

## Modding roadmap

- **Phase 1 — Baseline:** repeatable build; Windows startup test; input, saves, audio, graphics sanity checks.
- **Phase 2 — Small source changes:** one text change, one trainer/battle data change, one basic encounter edit; check save compatibility.
- **Phase 3 — Data pipelines:** document assets, maps, sprites, events, species, moves and trainers; identify editable formats and suitable tooling.
- **Phase 4 — Larger gameplay changes:** maps and events, new characters, encounters, UI, and custom mechanics after code paths are verified.
- **Phase 5 — PC experience (optional):** investigate recompilation/frontend support separately; do not assume changes automatically carry over.

## Working conventions

- Keep source credits, license/attribution files and original repository history intact.
- Do not commit ROMs (`.nds`), extracted copyrighted assets, proprietary SDKs, compiler binaries or credentials.
- Prefer small commits, descriptive change logs and reproducible tests.
- When a build step is not verified, label it as **unverified** rather than treating it as working.

## Clone locally

```powershell
git clone https://github.com/Scraxemas/pokeheartgold-single-screen.git
cd pokeheartgold-single-screen
git switch modding-dev
```

To check for upstream changes later:

```powershell
git remote add upstream https://github.com/ClickingMaster/pokeheartgold-single-screen.git
git fetch upstream
```

Do not merge upstream into the development branch without checking conflicts and testing the build.
