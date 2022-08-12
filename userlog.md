> :information_source: this log lists user most visible changes

> :warning: to find all changes use [changelog.txt](https://github.com/andry81-devops/gh-action--accum-gh-stats/blob/master/changelog.txt) file in a directory

## 2022.08.12:
* new: action.yml: flush print annotations at the last always executed step

## 2022.08.09:
* new: action.yml: print commit reference url to the log

## 2022.05.11:
* new: action.yml: added `commit_msg_entity` optional input parameter as replacement of `stat_entity` in the commit message
* changed: action.yml: renamed `stat_entity_path` to `stat_entity` to select implementation
* changed: action.yml: removed `stats_list_key` input parameter
* changed: action.yml: swapped `COMMIT_MESSAGE_PREFIX` and `COMMIT_MESSAGE_SUFFIX` in all scripts to further improve readability in case of GitHub commit message truncation

## 2022.05.06:
* fixed: action.yml: `CHANGELOG_FILE` must be always not empty

## 2022.05.05:
* new: bash: curl stderr print on error

## 2022.05.04:
* new: action.yml: added `COMMIT_MESSAGE_PREFIX` to split an automated user commit message into prefix and suffix parts

## 2022.04.16:
* fixed: action.yml: `mkdir` in a working copy moved after git checkout instead of before to avoid accidental remove on cleanup
* changed: action.yml: added `mkdir-p` parameter usage

## 2022.04.15:
* changed: action.yml: switched to use `andry81-devops/gh-action--git-checkout` action instead of `actions/checkout`

## 2022.04.02:
* changed: action.yml: switch to use `actions/checkout@v3` action

## 2022.03.31:
* changed: action.yml: `COMMIT_MESSAGE_DATE_TIME_PREFIX` variable usage

## 2022.03.23:
* new: action.yml: `env` input parameter to explicitly declare global environment variables
* new: action.yml: `changelog_dir` variable usage is added

## 2022.01.13:
* new: action.yml: workflow script execution time in the Automated Update commit message

## 2022.01.01:
* new: action.yml: added `deps_repo_branch` parameter to use specific repository branch as dependency
* new: action.yml: added `deps_repo_read_token` parameter to use specific read token for repository as dependency

## 2022.01.01:
* new: action.yml: use `GH_WORKFLOW_ROOT` variable to include `gh-workflow` shell scripts as dependencies
* changed: action.yml: removed relative paths usage

## 2021.12.31:
* changed: action.yml: head annotations workaround through `gh-workflow` script

## 2021.12.30:
* new: action.yml: print stat repository url and output repository directory url into pipeline

## 2021.12.30:
* changed: action.yml: removed print statistics change into pipeline as bugged in the current GitHub implementation (breaks notification prints from a script)
* changed: action.yml: moved `COMMIT_MESSAGE_SUFFIX` variable creation into workflow scripts

## 2021.12.30:
* new: action.yml: additionally print statistics change into pipeline

## 2021.12.15:
* changed: action.yml: commit message suffix with changes in statistic

## 2021.12.05:
* changed: action.yml: removed usage of the `write_error_to_file` and `write_warning_to_file` environment variables as not required anymore

## 2021.11.27:
* changed: action.yml: added `deps_repo_owner` parameter to specifically address dependent repositories
