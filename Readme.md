## Program Design...
This gem will not include a script but will accept a command line argument script name. 
<br>Script name needs to be inside the script or bin folder. (not sure yet).

### example on commands for the program:
gem install LAT; 
<br>LAT script.sh;

simple as that... your script is now executing in a launch agent that will wake from sleep.

## Questions to be answered in the project:
<pre>
Does a ruby Gem need to be programmed in ruby?
I could very rewrite the project in ruby. 
but it would still use the same bash code.
</pre>

<pre>
master branch has implementation ... requiring putting script in folder 
                         and putting folder name as command line arg.
without_gem branch has normal implementation ... requiring rewriting code.
</pre>
## Template from which others can build Launch Agents.
Only for Macintosh Computers, enjoy. 
Make an application or a script a launch agent.

Simple example of a mac app launch agent. People can use as a template. 
<br>Starts and Stops via different bash scripts. 
## Installation(program persists when installed until uninstalled.)
1) clone down project
2) cd project<br>
<pre><b>install and start</b></pre>
3) ./app/install_driver.sh<br>
<pre><b>uninstall and stop</b></pre>
4) ./app/uninstall_driver.sh

## Challenges (why needed)
Launch Agents do not immediately provide output<br>
to where a programmer can immediately see hello world.<br>
install_driver... sets the plist up and runs.

## how install_driver sets the plist up and runs:
app/install_driver allows plist to know your repo location<br>
app/install_driver script gathers "pwd" and injects it into the plist<br>
then install driver gives permission moves to standard location and runs.<br>
uses launchctl...

## Useful links 

https://nathangrigg.com/2012/07/schedule-jobs-using-launchd<br>
https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man5/launchd.plist.5.html

## Large scale implementation:
project abstracted from:<br>
https://github.com/MichaelDimmitt/Aerial_Desktop
