# I wrote this because sometimes I would:

* forget to fork, and would work against the master repo.
* forget to start a branch, and would accidentally work on the master branch
* forget to set my upstream origin, and would have to stop my flow and fix that
* Forget to add my project manager, and they miss out on notifications on my commits
* Run git clone in the wrong directory, and have to delete it, and reclone 

Now I just run `lambdaclone git@github.com:tfolbrecht/lambdaclone.git`

## Getting started

You must fill out the scripts variables inside quotes " with the following

| Bash Variables | Values |
| ----- | :-----|
| email                 | Your GitHub account email address |
| username              | Your GitHub account Username |
| secretkey             | Your [GitHub Token](https://github.com/settings/tokens)|
| branch_name           | The name of the branch you create, I use firstname-lastname |
| TLuser                | Your Primary TL's Username |
| TL5user               | Your 5th Day TL's Username |
| project_parent_path   | The path to the directory you want to clone to. |
| subdir_weeks          | Optional: Set to true if you want to use Week_## subdirectory structure |
| fs_prefix_project     | Optional: Prefix text to prepend at beginning of your local File System repository (Example: 'LS'). |
| fs_week_prefix        | Optional: Prefix text to append after the fs_prefix_project, if both are specified (Example: 'Wk'). Will automatically include separator & Week ##. |
| gh_prefix_project     | Optional: Prefix text to prepend at beginning of your remote GitHub repository (Example: 'LambdaSchool'). |
| gh_week_prefix        | Optional: Prefix text to append after the gh_prefix_project, if both are specified (Example: 'Week'). Will automatically include separator & Week ##. |
| separator             | Optional: Text to put between other optional parameters above (Example: '_'). |
| editor_bin            | Optional: Command to execute your preferred editor and send it the cloned repository path as an argument. |
| debug                 | Set to true to output debugging messages. |
| donowork              | Set to true to prevent any actual changes from happening. Useful for debugging. |

*note,* *not the most secure method of storing api keys lol*

Move/symlink script somewhere in your user execution path like `/usr/local/bin/` or `~/.local/bin`

## Todo

* [x] Check if variables empty
* [x] auto open editor with new repo path
* [ ] make github api only version (fork, add collaborator, set branch)
* [ ] best practice api key storage
* [ ] support non ssh
* [ ] check credential validity
* [ ] test against multiple configurations
* [ ] interactive ncurses menu, options, etc
