# SuperSearch (susearch)

**IMPORTANT NOTE**: SuperSearch is only available for *Linux x86_64* systems

A terminal program built for both relative and system-wide searches.
*SuperSearch*, was built with simplicity and control in mind. SuperSearch has the ability to 
search for filenames and directories, and outputting the paths associated with either or. 
Though, anything containing the name, be it a filename or directory, will be found if it / they exist. 
For example, given the filename **test.txt**, if there are files such as: *help_test.txt* or *new_test.txt*, 
they will be shown as **Found** in the output.

An example of how this will look is shown given in the link: [SuperSearch-Output](https://rayshawnlevy09.github.io/SuperSearch_Output/)

To combat the number of files being found containing a given name, SuperSearch has a **--limit** 
option which will only find the specified number of paths, and limits the output based on those 
paths that are **Found**, but it **doesn't** limit the output when searching.

The help (**-h**) flag can be used to search for a specific **section** based on the usage of the 
susearch command, such as: *options*, *common*, *limits*, *output* and *limit/output*. These are 
all of the usage patterns available for the command. The *-h* flag can also be used on its own 
revealing all of the named sections.
<br><br>

<h1 align="center"><strong>Getting Started</strong></h1><br><br>

<h2 align="center"><strong>Binary File</strong></h2>
<ol>
  <li> Download the binary file </li><br>
  <li> In the same directory enter the commands <code>sudo chown root ./susearch</code> - changes the owner of the file to root </li><br>
  <li> Next, you'll change the permissions of the file:
    <ul>
      <br><li> Common: enter the command <code> sudo chmod u+x ./susearch </code> - gives the current user permission to execute the file </li><br>
      <li> Reccomended: enter the command <code> sudo chmod ug+rws ./susearch </code> - allows the file to be executed with the permissions of its owner regardless of what user is executing the file if that is what you prefer</li><br>
    </ul>
  </li>
  <li> Then, enter the commands <code>sudo mv ./susearch ~/.local/bin</code> - move the file into the /home/your_username/.local/bin directory </li><br>
  <li> Then, enter the commands <code>sudo update-alternatives --install /usr/bin/susearch susearch ~/.local/bin/susearch 1</code> - create an alternative link </li>
</ol>

<br>The 5 steps above will allow you to run the file with root privileges and use the command from within any directory or location in the terminal.<br><br><br>

<h2 align="center"><strong>Archive tar.gz</strong></h2>
<ol>
  <li> Download the archive </li><br>
  <li> In the current directory, enter the commands <code>tar -xzvf susearch-x86_64-linux.tar.gz</code> - extract the file from the archive </li><br>
  <li> Then, perform steps 2-5 as shown above for the binary file. </li><br>
</ol>
<br><br>
Finally, to change the directory to your home directory enter the command <code>cd ~</code> and type the command shown below 
<code>susearch -h common</code> - shows the common susearch usage patterns
