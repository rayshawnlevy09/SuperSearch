# SuperSearch (susearch)

**IMPORTANT NOTE**: SuperSearch is only available for *Linux x86_64* systems

A terminal program built for both relative and system-wide searches.
*SuperSearch*, was built with simplicity and control in mind. SuperSearch has the ability to 
search for filenames and directories, and outputting the paths associated with either or. 
Though, anything containing the name, be it a filename or directory, will be found if it / they exist. 
For example, given the filename **test.txt**, if there are files such as: *help_test.txt* or *new_test.txt*, 
they will be shown as **Found** in the output.

An example of how this will look is shown below:
``` html

<DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title> SuperSearch Output </title>
    <style>
        body {
            background-color: darkgray;
        }
        #main_frame {
            height: 280px;
            border-width: 1px;
            border-radius: 12px;
            margin-top: 200px;
            margin-left: 400px;
            margin-right: 400px;
            background: black;
            padding-top: 0px;
            padding-bottom: 15px;
            padding-left: 8px;
            padding-right: 8px;
            font-family: monospace;
        }
        #prompt {
            color: lightgrey;
        }
        #command {
            color: yellow;
        }
        .output {
            color: cyan;
        }
        .path {
            color: royalblue;
        }
        .done {
            color: white;
        }
        .found {
            color: limegreen;
        }
        .blink {
          animation: blinker 1s linear infinite;
          color:  white;
          font-weight: bold;
        }
        @keyframes blinker {
            50% {
              opacity: 0;
            }
        }
    </style>
  </head>
  <body>
    <div id="main_frame">
        <div style="color: black; text-align: center; border: 5px; border-radius: 10px; background: whitesmoke; margin-left: 40%; margin-right: 40%;">
          <p>Terminal</p>
        </div>
        <p style="color: white;">
            <span style="color: royalblue;">user</span>@<span style="color: royalblue;">linux</span>
            <span id="prompt">~$</span>
            <span id="command"> susearch -f test.txt </span>
        </p>
        <br>
        <span class="output"><em>Searching</em></span>
        <span style="color: white;">:</span>
        <span class="path"><strong>/path/to/directory</strong></span>
        <br><br>
        <span class="output"><em>Searching</em></span>
        <span style="color: white;">:</span>
        <span class="path"><strong>/path/to/directory</strong></span>
        <br><br>
        <span class="done">--------------------</span>
        <span style="color: limegreen;">Done!</span>
        <span class="done">--------------------</span>
        <br><br>
        <span class="found"><em>Found</em></span>
        <span style="color: white;">:</span>
        <span class="path"><strong>/path/to/directory/filename</strong></span>
        <br><br>
        <p style="color:white;">
            [<span style="color: red"><strong>root</strong></span>]
            [<span style="color:mediumpurple;">susearch</span>]
            <span class="found">Found</span>
            <span class="output">1/1000</span>
            <span class="done">paths in</span>
            <span style="color: limegreen;">0.01</span>
            <span class="done">seconds</span>
        </p>
        <br>
        <p style="color: white;">
            <span style="color: royalblue;">user</span>@<span style="color: royalblue;">linux</span>
            <span id="prompt">~$</span>
            <span class="blink" class="done">|</span>
        </p>
    </div>
  </body>
</html>
```

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
