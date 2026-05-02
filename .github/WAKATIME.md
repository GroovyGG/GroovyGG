# WakaTime + Weekly Coding Breakdown

The **Weekly Coding Breakdown** block in `README.md` is filled by [waka-readme-stats](https://github.com/anmol098/waka-readme-stats). Do not edit the content between `<!--START_SECTION:waka-->` and `<!--END_SECTION:waka-->` manually.

## Secrets (repo → Settings → Secrets and variables → Actions)

| Name | Value |
|------|--------|
| `WAKATIME_API_KEY` | From [wakatime.com/settings/account](https://wakatime.com/settings/account) |
| `GH_TOKEN` | GitHub PAT with `repo` + `user` (fine-grained: **Contents** read/write on this repo) |

## Run

**Actions** → **Waka Readme** → **Run workflow**. Also runs daily (see cron in `.github/workflows/waka-readme.yml`).

## Cursor

Install the **WakaTime** extension and set **WakaTime: Api Key** in settings so coding time is recorded.

## Flags

Edit `.github/workflows/waka-readme.yml` → `with:` — set any `SHOW_*` to `"False"` to hide that section. `SHOW_LOC_CHART` controls the Timeline chart.
