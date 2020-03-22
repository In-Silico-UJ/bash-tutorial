
# Bash tips & tricks

_Prepared for webinar of KNSB In Silico, 2020_

[https://in-silico-uj.github.io/](https://in-silico-uj.github.io/)

## Moving around

* `tree`: Display folder structure
* `ls -l` or `ll`: Display contents of a directory with details (long)
* `ls -lrt`: Display contents of a directory, sorted by date (`-t`), newest at the bottom (`-r`)
* `ls -1`: Display contents, one file per line
    * `ls -1 | wc -l`: Count files in a directory
* `cd ..`: Move to parent directory
    * `cd ~` or `cd`: Move to home directory
    * `cd ~user`: Move to home directory of a specified user
    * `cd -`: Move to previous directory
* Wildcards
    * `*`: Any number of any characters
    * `?`: Any character
    * `[ab]`: a or b (single characters)
    * `{ab,cd}`: ab or cd
    * `Ctrl+X,*`: Expand wildcards

## Inspecting files

* `head, tail`: Display beginning or end of a file
* `tail -f`: Display tail of a file, following appended lines
* `less +F`: Following appended lines in less
* `grep`: Search for a pattern
    * `grep -A 1`: Display 1 line of context after match
    * `grep -B 1`: Display 1 line of context before match
    * `grep -C 1`: Display 1 line of context around match
    * `grep -c`: Count matching lines
    * `grep -m 1`: Stop reading after 1 matching line
* `zcat`, `zless`, `zgrep`: Work on gzipped files
* `cut`: Display columns
* `vd`: [VisiData](https://www.visidata.org/), tool for working with tables in a terminal

## Editing commands

* `Ctrl+arrows`: Move cursor by words
* `Ctrl+Shift+C`, `Ctrl+Shift+V`: Copy/paste in terminal
* `Ctrl+A`, `Ctrl+E`: Move the cursor to the beginning/end
* `Ctrl+U`, `Ctrl+K`: Delete from the cursor position to the beginning/end
* `Ctrl+W`: Delete from the cursor to the beginning of the word
* `Ctrl+_`: Undo
* `Ctrl+X,E`: Edit the command in the editor

### Other shortcuts worth knowing

* `Ctrl+L`: Clear screen
* `Ctrl+S`, `Ctrl+Q`: Freeze/unfreeze output

## Working with history

* `history`: Show history
* `!!`: Last command
* `!<num>`: Command with given number in history
* `Ctrl+R`: Reverse search in history (`Ctrl+G`: abort the search)
* `PageUp, PageDown`: Complete command from history (needs to be activated – [like this](https://electrictoolbox.com/pageup-history-auto-completion-bash-shell/))
* `^x^y^`: Replace the first occurrence of x in the previous command with y

## Long processes
* `Ctrl+C`: Kill a running job
* `Ctrl+Z`: Stop (suspend) a running job
* `fg`, `bg`: Move a running job to the foreground/background
* `ps`: See currently active processes
* `top`: See processes with updates
* `htop`: See processes with updates, nicer
* `nohup`: No hang up – keep command running even if terminal closes


