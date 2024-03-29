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

    -h or --help        Prints help instructions
    -g or --generate    Generates aliases for both zsh and fish
    --fish              Generates abbreviations for fish only
    --zsh               Generates aliases for zsh only
    -e or --edit [type] Edits the specified alias base-file
                        based on its type: folder, config
                        or command 
                        
This script uses four base-files: folder-base for folder aliases,  
config-base for config editing aliases and command-base for custom command  
aliases. All files should be located in the same folder as the script file.  

The base files are layed out as follows:

    Desired alias     folder/file/command     argument (in case of command base)  
    
    dbx               ~/Dropbox
    vrc               ~/.vimrc
    ls                ls                      -al

The aliases are generated as follows:

- Fish:

      abbr dbx 'cd ~/Dropbox'
      abbr vrc 'vim ~/.vimrc
      abbr ls 'ls -al'
     
- Zsh:
    
      alias dbx='cd ~/Dropbox'
      alias vrc='vim ~/.vimrc'
      alias ls='ls -al'
  
Alias/Abbreviation files are the following:  

    $HOME/.config/zsh/aliases  
    $HOME/.config/fish/abbreviations  

Each file must be included in their respective shell config file, zshrc or config.fish  
