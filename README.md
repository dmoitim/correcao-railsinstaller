# Fixing RailsInstaller 3.2.0

Unfortunately, for those of us on Windows, it looks like the newest version of Rails Installer has a bug! There are [great minds on the job](https://github.com/railsinstaller/railsinstaller-windows/issues/70#issuecomment-208663716), but we need to get going right now, so we'll have to fix it ourselves manually.

If when you type `rails -v` in your Command Prompt with Ruby and Rails, you get the message

    The system cannot find the path specified.

then follow these steps:

 1. In Atom, from the **File** menu, **Open folder...**
 1. Locate and open the folder `C:\RailsInstaller\Ruby2.2.0\bin`
 1. From the **Find** menu, **Find in Project**
 1. In the "Find in project" field that appears at the bottom of the screen, paste the following (be careful not to select the trailing or leading spaces before you copy):
 
        C:\Users\emachnic\GitRepos\railsinstaller-windows\stage\Ruby2.2.0\bin\

 1. Click "Find". It should locate ~26 matches across ~13 files.
 1. Leave the "Replace in project" field blank.
 1. Click "Replace All" and confirm.
 1. In the "Find in project" field that appears at the bottom of the screen, paste the following (be careful not to select the trailing or leading spaces before you copy):

        C:/Users/emachnic/GitRepos/railsinstaller-windows/stage/Ruby2.2.0/bin/

 1. Click "Find". It should locate ~16 matches across ~8 files.
 1. Leave the "Replace in project" field blank.
 1. Click "Replace All" and confirm.
 1. Quit Atom, restart the Command Prompt with Ruby and Rails, and retry `rails -v`. It should now work.
 
 Copy of: https://gist.github.com/raghubetina/131da36439842fe33106f1aa5be40554
