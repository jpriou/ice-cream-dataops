# Cognite Data Fusion Bootcamp

This repo contains all the material created during the bootcamp session.
- `ice-cream-dataops`: all the toolkit manifests
- `grafana`: grafana dashboard (`json` format)

## Usage

Clone repo:
```sh
$ git clone https://github.com/jpriou/ice-cream-dataops.git
$ cd ice-cream-dataops
```

Install dependencies:
```sh
$ poetry install
```

Use `cdf-toolkit`:

```sh
$ cdf-tk build --env=<test/prod>
$ cdf-tk deploy --dry-run
$ cdf-tk deploy
```

## Automated deployment

2 workflows are available for automated deployment:
- `deploy-test`: deploys to the `test` project on pull request (to `main`)
- `deploy-prod`: deploys to the `prod` project when merging to `main` (approval required)


2 environments are also created. Each environment contains the necessary secrets to deploy to each project (`test`/`prod`). All deployment parameters common to both environments are available as repository secrets.