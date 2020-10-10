# Cmder Configuration

1. Add some alias

   > note that ${CMDER_HOME} represents your cmder installation dictionary

   ```
   vim ${CMDER_HOME}/config/user_aliases.cmd
   ```
   My configuration:
   ```
   ;= @echo off
   ;= rem Call DOSKEY and use this file as the macrofile
   ;= %SystemRoot%\system32\doskey /listsize=1000 /macrofile=%0%
   ;= rem In batch mode, jump to the end of the file
   ;= goto:eof
   ;= Add aliases below here
   e.=explorer .
   gl=git log --oneline --all --graph --decorate  $*
   ls=ls --show-control-chars -F --color $*
   pwd=cd
   clear=cls
   history=cat "%CMDER_ROOT%\config\.history"
   unalias=alias /d $1
   vi=vim $*
   cmderr=cd /d "%CMDER_ROOT%"
   
   # configurations added
   l=ls -l --color
   clear=cls
   ```
   
2. Change Styles

   - download or git clone [AmrEldib/cmder-powerline-prompt](https://github.com/AmrEldib/cmder-powerline-prompt)
   - download `powerline` fonts and install your favorite font

   - put all the `lua` file into `${CMDER_HOME}/config`
   - restart cmder, use settings to choose your powerline font

3. Add to your context menue: https://github.com/cmderdev/cmder/wiki/Context-menu-integration

4. Prevent cursor fault like: https://github.com/microsoft/vscode/issues/48988; Find the 51 line of `${CMDER_HOME}/vendor/clink.lua`, change "λ" to "#" or else...
