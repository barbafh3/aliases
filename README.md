# aliases

The script uses base files to generate both aliases for zsh and abbreviations for fish.

## Installation

To clone the repository use the following command:

```git clone https://github.com/barbafh3/aliases.git```

After that just add the script to your PATH.

## Usage

aliases [-h][-g][--fish][--zsh][-e <type>] -- generates aliases for zsh and fish \n
usage:    aliases [arguments]\n
   or:    aliases [arguments] [type]
Arguments:
    -h or --help        Prints help instructions
    -g or --generate    Generates aliases for both zsh and fish
    --fish              Generates abbreviations for fish only
    --zsh               Generates aliases for zsh only
    -e or --edit [type] Edits the specified alias base-file
                        based on its type: folder, config
                        or command 
This script uses four base-files: folder-base for folder aliases, 
config-base for config editing aliases, command-base for custom command
aliases and log-base for log based command aliases. All files should be 
located in the same folder as this script file.
The base files are layed out as follows:
Desired alias      folder/file/command       argument (in case of command base)
The aliases are generated as follows (fish shell used as example):
Folder - uses cd command. E.g. abbr <alias> 'cd <folder>'
Config - uses vim. E.g. abbr <alias> 'vim <file>'
Command - uses specified command. E.g. abbr <alias> '<command> <arguments>'
Alias/Abbreviation files are the following:
$HOME/.config/zsh/aliases
$HOME/.config/fish/abbreviations
Each file is included in their respective shell config file, zshrc or config.fish
