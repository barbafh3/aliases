# aliases

The script uses base files to generate both aliases for zsh and abbreviations for fish.

## Installation

To clone the repository use the following command:

```git clone https://github.com/barbafh3/aliases.git```

After that just add the script to your PATH.

## Usage

aliases [-h][-g][--fish][--zsh][-e <type>] -- generates aliases for zsh and fish  
usage:&ensp;&ensp;&ensp;&ensp;aliases [arguments]  
&ensp;&ensp;&ensp;&ensp;or:&ensp;&ensp;&ensp;&ensp;aliases [arguments] [type]  
  
Arguments:  
&ensp;&ensp;&ensp;&ensp;-h or --help&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Prints help instructions  
&ensp;&ensp;&ensp;&ensp;-g or --generate&ensp;&ensp;&ensp;&ensp;Generates aliases for both zsh and fish  
&ensp;&ensp;&ensp;&ensp;--fish&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Generates abbreviations for fish only  
&ensp;&ensp;&ensp;&ensp;--zsh&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Generates aliases for zsh only  
&ensp;&ensp;&ensp;&ensp;-e or --edit [type]&ensp;&ensp;&ensp;&ensp;Edits the specified alias base-file  
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;based on its type: folder, config  
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;or command  
                        
This script uses four base-files: folder-base for folder aliases,  
config-base for config editing aliases and command-base for custom command  
aliases. All files should be located in the same folder as the script file.  

The base files are layed out as follows:

    Desired alias&ensp;&ensp;&ensp;&ensp;folder/file/command&ensp;&ensp;&ensp;&ensp;argument (in case of command base)  

The aliases are generated as follows (fish shell used as example):  

    Folder - uses cd command. E.g. abbr <alias> 'cd <folder>'  
    Config - uses vim. E.g. abbr <alias> 'vim <file>'  
    Command - uses specified command. E.g. abbr <alias> '<command> <arguments>'  

Alias/Abbreviation files are the following:  

    $HOME/.config/zsh/aliases  
    $HOME/.config/fish/abbreviations  

Each file is included in their respective shell config file, zshrc or config.fish  
