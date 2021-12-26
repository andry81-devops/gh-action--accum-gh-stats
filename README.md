<p align="center">
  <a href="#"><img src="https://img.shields.io/github/repo-size/andry81/gh-action--accum-gh-stats" valign="middle" alt="GitHub repo size in bytes" /></a>
• <a href="https://github.com/XAMPPRocky/tokei"><img src="https://tokei.rs/b1/github/andry81/gh-action--accum-gh-stats?category=lines" valign="middle" alt="lines of text by tokei.rs" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/commits/master/traffic/views">
    <img src="https://img.shields.io/badge/dynamic/json?color=success&label=Github%20views|all&query=count&url=https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/raw/master/traffic/views/latest-accum.json?raw=True&logo=github" valign="middle" alt="GitHub views|any|total" />
    <img src="https://img.shields.io/badge/dynamic/json?color=success&label=14d&query=count&url=https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/raw/master/traffic/views/latest.json?raw=True" valign="middle" alt="GitHub views|any|14d" /></a>
• <a href="https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/commits/master/traffic/views">
    <img src="https://img.shields.io/badge/dynamic/json?color=success&label=Github%20views|unq&query=uniques&url=https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/raw/master/traffic/views/latest-accum.json?raw=True&logo=github" valign="middle" alt="GitHub views|unique per day|total" />
    <img src="https://img.shields.io/badge/dynamic/json?color=success&label=14d&query=uniques&url=https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/raw/master/traffic/views/latest.json?raw=True" valign="middle" alt="GitHub views|unique per day|14d" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/commits/master/traffic/clones">
    <img src="https://img.shields.io/badge/dynamic/json?color=success&label=Github%20clones|all&query=count&url=https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/raw/master/traffic/clones/latest-accum.json?raw=True&logo=github" valign="middle" alt="GitHub clones|any|total" />
    <img src="https://img.shields.io/badge/dynamic/json?color=success&label=14d&query=count&url=https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/raw/master/traffic/clones/latest.json?raw=True" valign="middle" alt="GitHub clones|any|14d" /></a>
• <a href="https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/commits/master/traffic/clones">
    <img src="https://img.shields.io/badge/dynamic/json?color=success&label=Github%20clones|unq&query=uniques&url=https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/raw/master/traffic/clones/latest-accum.json?raw=True&logo=github" valign="middle" alt="GitHub clones|unique per day|total" />
    <img src="https://img.shields.io/badge/dynamic/json?color=success&label=14d&query=uniques&url=https://github.com/andry81/gh-action--accum-gh-stats--gh-stats/raw/master/traffic/clones/latest.json?raw=True" valign="middle" alt="GitHub clones|unique per day|14d" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81/gh-action--accum-gh-stats/commits">
    <img src="https://img.shields.io/github/commits-since/andry81/gh-action--accum-gh-stats/latest?sort=semver&label=Github%20commits%20since%20latest" valign="middle" alt="GitHub commits since latest version" /></a>
  <a href="https://github.com/andry81/gh-action--accum-gh-stats/releases">
    <img src="https://img.shields.io/github/v/release/andry81/gh-action--accum-gh-stats?include_prereleases&label=latest" valign="middle" alt="latest release name" /></a>
</p>

---

<p align="center">
  <a href="https://github.com/andry81/gh-action--accum-gh-stats/blob/master/userlog.md">Userlog</a>
• <a href="https://github.com/andry81/gh-action--accum-gh-stats/blob/master/changelog.txt">Changelog</a>
• <a href="#dependecies">Dependencies</a>
• <a href="#known_issues">Known issues</a>
• <a href="#copyright-and-license"><img src="https://github.com/andry81/andry81/raw/master/badges/mit-license.svg" valign="middle" alt="copyright and license" />&nbsp;Copyright and License</a>
</p>

<h4 align="center">GitHub composite action to request and accumulate a repository clones and/or views statistic.<br/>
<br/>
Tutorial to use with: https://github.com/andry81/github-accum-stats</h4>

##

# gh-action--accum-gh-stats@master

**Features**:

* Repository to track and repository to store traffic statistic can be different, and you may directly point the statistic as commits list:
  `https://github.com/{{REPO_OWNER}}/{{REPO}}--gh-stats/commits/master/traffic/clones` or
  `https://github.com/{{REPO_OWNER}}/{{REPO}}--gh-stats/commits/master/traffic/views`

* Workflow is used [accum-stats.sh](https://github.com/andry81/gh-workflow/blob/master/bash/github/accum-stats.sh) bash script to accumulate traffic statistic

* The script accumulates statistic both into a single file and into a set of files grouped by year and allocated per day:
  `traffic/clones/by_year/YYYY/YYYY-MM-DD.json` or
  `traffic/views/by_year/YYYY/YYYY-MM-DD.json`

* The script does compensate statistic interpolation issue (from inner GitHub resolution like per hour basis into per day basis) for the last records by calculation of the min and max values per day fluctuation and does use the maximum value instead of an interpolated value for all being removed outdated records (after 14'th day).

* The script does detect residual changes in the `latest.json` file has generated by the github to avoid excessive commits while a day with empty or has no effect changes except those changes which is a removal of outdated records (after 14'th day).

# USAGE

> :warning: You must replace all placeholder into respective values:

* `{{REPO_OWNER}}` -> repository owner
* `{{REPO}}` -> your repository

## Examples:

`.github/workflows/accum-gh-clone-stats.yml`:

```yml
name: GitHub clones counter for 14 days at every 8 hours and clones accumulator

on:
  schedule:
    - cron: "0 */8 * * *"
  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

jobs:
  accum-gh-clone-stats:
    runs-on: ubuntu-latest

    steps:
      - uses: {{REPO_OWNER}}/gh-action--accum-gh-stats@master
        with:
          deps_repo_owner:          {{REPO_OWNER}}

          stat_repo_owner:          {{REPO_OWNER}}
          stat_repo:                {{REPO}}
          stat_entity_path:         traffic/clones
          stat_repo_read_token:     ${{ secrets.READ_STATS_TOKEN }}
          stats_list_key:           clones

          curl_flags: >-
            -H 'Cache-Control: no-cache'

          output_repo_owner:        {{REPO_OWNER}}
          output_repo:              {{REPO}--gh-stats
          output_repo_branch:       master
          output_repo_dir:          traffic/clones
          output_repo_write_token:  ${{ secrets.WRITE_STATS_TOKEN }}
```

`.github/workflows/accum-gh-view-stats.yml`:

```yml
name: GitHub views counter for 14 days at every 8 hours and views accumulator

on:
  schedule:
    - cron: "0 */8 * * *"
  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

jobs:
  accum-gh-view-stats:
    runs-on: ubuntu-latest

    steps:
      - uses: {{REPO_OWNER}}/gh-action--accum-gh-stats@master
        with:
          deps_repo_owner:          {{REPO_OWNER}}

          stat_repo_owner:          {{REPO_OWNER}}
          stat_repo:                {{REPO}}
          stat_entity_path:         traffic/views
          stat_repo_read_token:     ${{ secrets.READ_STATS_TOKEN }}
          stats_list_key:           views

          curl_flags: >-
            -H 'Cache-Control: no-cache'

          output_repo_owner:        {{REPO_OWNER}}
          output_repo:              {{REPO}--gh-stats
          output_repo_branch:       master
          output_repo_dir:          traffic/views
          output_repo_write_token:  ${{ secrets.WRITE_STATS_TOKEN }}
```

> :information_source: You can use `secrets.READ_STATS_TOKEN` instead of `secrets.WRITE_STATS_TOKEN` as long as both repositories under the same repository owner.

> :warning: You must use different values for `deps_repo_owner`, `stat_repo_owner` and `output_repo_owner` if respective repositories actually under different repository owners.

> :information_source: See <a href="https://github.com/andry81/github-accum-stats/blob/master/README.md#reuse">REUSE</a> section for details if you have multiple repositories and want to store all workflow scripts in a single repository.

## Dependencies<a name="dependecies"></a>

* https://github.com/andry81/gh-workflow

## Known Issues<a name="known_issues"></a>

The action has supported not all features of a generic GitHub action: https://github.com/actions/runner/issues/646

> **What does Composite Run Steps Not Support**
>
> We don't support setting conditionals, continue-on-error, timeout-minutes, "uses", and secrets on individual steps within a composite action right now.
>
> (Note: we do support these attributes being set in workflows for a step that uses a composite run steps action)

## Copyright and License<a name="copyright-and-license"></a>

Code and documentation copyright 2021 Andrey Dibrov. Code released under [MIT License](https://github.com/andry81/gh-action--accum-gh-stats/blob/master/license.txt)
