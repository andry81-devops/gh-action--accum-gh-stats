<p align="center">
  <a href="#">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/metrics/shields-repo-size.svg" valign="middle" alt="GitHub repo size in bytes" /></a>
<!-- -- >
• <a href="#">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/metrics/shields-code-size.svg" valign="middle" alt="code size in bytes" /></a>
<!-- -->
• <a href="https://github.com/XAMPPRocky/tokei">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/metrics/tokei-lines-of-code.svg" valign="middle" alt="lines of code by tokei.rs" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81-stats/gh-action--accum-gh-stats--gh-stats/commits/master/traffic/views">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/traffic/views/all.svg" valign="middle" alt="GitHub views|any|total" />
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/traffic/views/all-14d.svg" valign="middle" alt="GitHub views|any|14d" /></a>
• <a href="https://github.com/andry81-stats/gh-action--accum-gh-stats--gh-stats/commits/master/traffic/views">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/traffic/views/unq.svg" valign="middle" alt="GitHub views|unique per day|total" />
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/traffic/views/unq-14d.svg" valign="middle" alt="GitHub views|unique per day|14d" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81-stats/gh-action--accum-gh-stats--gh-stats/commits/master/traffic/clones">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/traffic/clones/all.svg" valign="middle" alt="GitHub clones|any|total" />
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/traffic/clones/all-14d.svg" valign="middle" alt="GitHub clones|any|14d" /></a>
• <a href="https://github.com/andry81-stats/gh-action--accum-gh-stats--gh-stats/commits/master/traffic/clones">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/traffic/clones/unq.svg" valign="middle" alt="GitHub clones|unique per day|total" />
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/traffic/clones/unq-14d.svg" valign="middle" alt="GitHub clones|unique per day|14d" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81-devops/gh-action--accum-gh-stats/commits">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/metrics/commits-since-latest.svg" valign="middle" alt="GitHub commits since latest version" /></a>
  <a href="https://github.com/andry81-devops/gh-action--accum-gh-stats/releases">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/metrics/latest-release-name.svg" valign="middle" alt="latest release name" /></a>
• <a href="https://github.com/andry81-devops/gh-action--accum-gh-stats/releases">
    <img src="https://github.com/andry81-cache/andry81-devops--gh-content-cache/raw/master/repo/andry81-devops/gh-action--accum-gh-stats/badges/metrics/github-all-releases.svg" valign="middle" alt="GitHub all releases" /></a>
</p>

<p align="center">
  <a href="https://github.com/andry81/donate"><img src="https://github.com/andry81-cache/gh-content-static-cache/raw/master/common/badges/donate/donate.svg" valign="middle" alt="donate" /></a>
</p>

---

<p align="center">
  <a href="https://github.com/andry81-devops/gh-action--accum-gh-stats/tree/HEAD/userlog.md">Userlog</a>
• <a href="https://github.com/andry81-devops/gh-action--accum-gh-stats/tree/HEAD/changelog.txt">Changelog</a>
• <a href="#dependencies">Dependencies</a>
• <a href="#known-issues">Known issues</a>
• <a href="#copyright-and-license"><img src="https://github.com/andry81-cache/gh-content-static-cache/raw/master/common/badges/license/mit-license.svg" valign="middle" alt="copyright and license" />&nbsp;Copyright and License</a>
</p>

<h4 align="center">GitHub composite action to request and accumulate a repository clones/views statistic.<br />
<br />
Tutorial to use with: https://github.com/andry81-devops/github-accum-stats</h4>

All tutorials: https://github.com/andry81/index#tutorials

##

# gh-action--accum-gh-stats@master

## Features:

* Repository to track and repository to store traffic statistic can be different, and you may directly point the statistic as commits list:
  `https://github.com/{{REPO_OWNER}}/{{REPO}}--gh-stats/commits/master/traffic/clones` or
  `https://github.com/{{REPO_OWNER}}/{{REPO}}--gh-stats/commits/master/traffic/views`

* Workflow is used [accum-stats.sh](https://github.com/andry81-devops/gh-workflow/tree/HEAD/bash/github/accum-stats.sh) bash script to accumulate traffic statistic

* The script accumulates statistic both into a single file and into a set of files grouped by year and allocated per day:
  `traffic/clones/by_year/YYYY/YYYY-MM-DD.json` or
  `traffic/views/by_year/YYYY/YYYY-MM-DD.json`

* The script does compensate statistic interpolation issue (from inner GitHub resolution like per hour basis into per day basis) for the last records by calculation of the min and max values per day fluctuation and does use the maximum value instead of an interpolated value for all being removed outdated records (after 14'th day).

* The script does detect residual changes in the `latest.json` file has generated by the github to avoid excessive commits while a day with empty or has no effect changes except those changes which is a removal of outdated records (after 14'th day).


## Functionality of the script:

* `CONTINUE_ON_INVALID_INPUT=1`, `CONTINUE_ON_EMPTY_CHANGES=1`, `CONTINUE_ON_RESIDUAL_CHANGES=1`:
  Treats invalid input, empty changes or unexpected/residual changes as not an error as by default.

* `ENABLE_GENERATE_CHANGELOG_FILE=1`, `CHANGELOG_FILE=".../changelog.txt"`:
  Generates a textual changelog file with notes about changes per commit including the changes absence in case of skipped errors.

* `ENABLE_COMMIT_MESSAGE_DATE_WITH_TIME=1`:
  Inserts the time string in format `HH:MMZ` additionally after the date in each commit message (by default inserts only a date for shorter commit messages).

* `ENABLE_COMMIT_MESSAGE_DATE_TIME_WITH_LAST_CHANGED_DATE_OFFSET=1`:
  Inserts the last changed date offset string additionally after the datetime in each commit message in format `-DDT` to note the closest changed date.

* `ENABLE_COMMIT_MESSAGE_WITH_WORKFLOW_RUN_NUMBER=1`:
  Inserts the workflow run number after date/time prefix in each commit message (by default does not insert for shorter commit messages).

* `ENABLE_GITHUB_ACTIONS_RUN_URL_PRINT_TO_CHANGELOG=1`:
  Prints GitHub Actions Run URL (with or without workflow run number) into the changelog file to reference the log on the GitHub from the changelog file.

* `ENABLE_REPO_STATS_COMMITS_URL_PRINT_TO_CHANGELOG=1`:
  Prints Statistic Output Repository commit URL into the changelog file to reference the commit from being committed changelog file.

  > **Note** The actual hash of the commit can not be know on the moment of the commit. So instead of the commit hash, an approximate date of the commit is used (~ +5 min ahead) in format of:
  > `https://github.com/{{REPO_OWNER}}/{{REPO}}--gh-stats/commits?branch={{BRANCH}}&time_zone=utc&until=YYYY-MM-DD`

# USAGE

> **Warning** You must replace all placeholder into respective values:

* `{{REPO_OWNER}}` -> repository owner
* `{{REPO}}` -> your repository
* `{{BRANCH}}` -> your repository branch or reference

## Examples:

<a name="accum-gh-clone-stats-yml">`.github/workflows/accum-gh-clone-stats.yml`</a>:

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
          deps_repo_branch:         master
          deps_repo_read_token:     ${{ github.token }}

          stat_repo_owner:          {{REPO_OWNER}}
          stat_repo:                {{REPO}}
          stat_entity:              clones
          stat_repo_read_token:     ${{ secrets.READ_STATS_TOKEN }}
          stats_list_key:           clones

          #commit_msg_entity:        cl

          curl_flags: >-
            -H 'Cache-Control: no-cache'

          output_repo_owner:        {{REPO_OWNER}}
          output_repo:              {{REPO}}--gh-stats
          output_repo_branch:       master
          output_repo_dir:          traffic/clones
          output_repo_write_token:  ${{ secrets.WRITE_STATS_TOKEN }}

          flags: >-
            ENABLE_PRINT_INITIAL_ENV_INTO_STDOUT=1

          env: >-
            ENABLE_GENERATE_CHANGELOG_FILE=1
            ENABLE_COMMIT_MESSAGE_DATE_WITH_TIME=1                            # insert the time string in format `HH:MMZ` additionally after the date in each commit message
            ENABLE_COMMIT_MESSAGE_DATE_TIME_WITH_LAST_CHANGED_DATE_OFFSET=1   # insert datetime suffix as offset to the last changed date in format `-DDT` to note the closest changed date
            ENABLE_COMMIT_MESSAGE_WITH_WORKFLOW_RUN_NUMBER=1                  # insert the workflow run number after date/time prefix in each commit message
            ENABLE_GITHUB_ACTIONS_RUN_URL_PRINT_TO_CHANGELOG=1
            ENABLE_REPO_STATS_COMMITS_URL_PRINT_TO_CHANGELOG=1
          #  CONTINUE_ON_INVALID_INPUT=1
          #  CONTINUE_ON_EMPTY_CHANGES=1
          #  CONTINUE_ON_RESIDUAL_CHANGES=1
          #  CHANGELOG_FILE=changelog.txt
```

<a name="accum-gh-view-stats-yml">`.github/workflows/accum-gh-view-stats.yml`</a>:

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
          deps_repo_branch:         master
          deps_repo_read_token:     ${{ github.token }}

          stat_repo_owner:          {{REPO_OWNER}}
          stat_repo:                {{REPO}}
          stat_entity:              views
          stat_repo_read_token:     ${{ secrets.READ_STATS_TOKEN }}
          stats_list_key:           views

          #commit_msg_entity:        vi

          curl_flags: >-
            -H 'Cache-Control: no-cache'

          output_repo_owner:        {{REPO_OWNER}}
          output_repo:              {{REPO}}--gh-stats
          output_repo_branch:       master
          output_repo_dir:          traffic/views
          output_repo_write_token:  ${{ secrets.WRITE_STATS_TOKEN }}

          flags: >-
            ENABLE_PRINT_INITIAL_ENV_INTO_STDOUT=1

          env: >-
            ENABLE_GENERATE_CHANGELOG_FILE=1
            ENABLE_COMMIT_MESSAGE_DATE_WITH_TIME=1                            # insert the time string in format `HH:MMZ` additionally after the date in each commit message
            ENABLE_COMMIT_MESSAGE_DATE_TIME_WITH_LAST_CHANGED_DATE_OFFSET=1   # insert datetime suffix as offset to the last changed date in format `-DDT` to note the closest changed date
            ENABLE_COMMIT_MESSAGE_WITH_WORKFLOW_RUN_NUMBER=1                  # insert the workflow run number after date/time prefix in each commit message
            ENABLE_GITHUB_ACTIONS_RUN_URL_PRINT_TO_CHANGELOG=1
            ENABLE_REPO_STATS_COMMITS_URL_PRINT_TO_CHANGELOG=1
          #  CONTINUE_ON_INVALID_INPUT=1
          #  CONTINUE_ON_EMPTY_CHANGES=1
          #  CONTINUE_ON_RESIDUAL_CHANGES=1
          #  CHANGELOG_FILE=changelog.txt
```

> **Note** You can use `secrets.READ_STATS_TOKEN` instead of `secrets.WRITE_STATS_TOKEN` as long as both repositories under the same repository owner.

> **Warning** You must use different values for `deps_repo_owner`, `stat_repo_owner` and `output_repo_owner` if respective repositories actually under different repository owners.

> **Note** See <a href="https://github.com/andry81-devops/github-accum-stats#reuse">REUSE</a> section for details if you have multiple repositories and want to store all GitHub workflow scripts (`.github/workflows/*.yml`) in a single repository.

## Dependencies

* https://github.com/andry81-devops/gh-workflow

## Known Issues

https://github.com/andry81-devops/gh-known-issues#known-issues

## Last known issues updates

https://github.com/andry81-devops/gh-known-issues#last-known-issues-updates

## Copyright and License

Code and documentation copyright 2021 Andrey Dibrov. Code released under [MIT License](https://github.com/andry81-devops/gh-action--accum-gh-stats/tree/HEAD/license.txt)
