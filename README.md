# David Tenreiro

[![Marquee SVG](https://marquee.datf.net/?width=850&duration=55000&content=++++%E2%80%A2++++DAVID+TENREIRO++++%E2%80%A2++++PHP+%E2%80%A2+PYTHON+%E2%80%A2+C/C%2b%2b+%E2%80%A2+GO+%E2%80%A2+JAVASCRIPT+%E2%80%A2+SVELTE+%E2%80%A2+CI/CD+%E2%80%A2+GITHUB%20ACTIONS%20AND%20TEMPLATES+%E2%80%A2+DOCKER+%E2%80%A2+LINUX+%E2%80%A2+BASH+%E2%80%A2+VIM)](https://github.com/datf)

## What I build

- Backend and systems software with a focus on reliability and performance.
- Cloud and container-based infrastructure for development, deployment and scale.
- CI/CD workflows and internal tooling that improve developer velocity.
- Architecture decisions that keep products maintainable as they grow.
- Mods and tooling for videogames.

## Featured repositories

### [SVG Marquee Generator](https://github.com/datf/svgmarquee)
A fast, dynamic Go application that generates seamlessly looping, animated SVG marquees for GitHub READMEs as can be seen at the top of this page. With [automated](https://github.com/datf/svgmarquee/actions) [github actions](https://github.com/datf/svgmarquee/blob/main/.github/workflows/main.yml) to build and upload the latest [release binaries](https://github.com/datf/svgmarquee/releases).

### Rocket League [mods](https://github.com/datf/SpectatorReplaySkip) and a [repository template](https://github.com/datf/BakkesmodPluginTemplateV2)
Archived now as BakkesMod is no longer maintained, the [repository template](https://github.com/datf/BakkesmodPluginTemplateV2) lets you create a new git repository configured to build a mod with all the msbuild tooling setup to the latest SDK, project settings, boilerplate and configuration so you can build it locally and release automatically with a zip file that meets all the specs for the project.

### [Calc LLC](https://github.com/datf/calc-llc)
Svelte SPA deployed to [github pages](https://datf.github.io/calc-llc) to optimize gameplay in Coal LLC using dynamic programming to calculate the optimal strategy, featuring:
* Automated [CI](https://github.com/datf/calc-llc/blob/master/.github/workflows/ci.yml) and [CD](https://github.com/datf/calc-llc/blob/master/.github/workflows/deploy.yml) pipelines with [integration tests](https://github.com/datf/calc-llc/blob/master/src/lib/optimizer.test.js).
* Contained development environment using [podman/docker containers](https://github.com/datf/calc-llc/blob/master/docker-compose.yml).
* Husky [hooks](https://github.com/datf/calc-llc/tree/master/.husky) to run formatter, linter, checks and tests before committing and pushing to the origin repository.
