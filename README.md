Download Link: https://assignmentchef.com/product/solved-cs139-homework-5-command-line-interpreter
<br>
Design, implement, document, test and run a simple shell, known here as a <strong><em>command-line interpreter</em></strong> (<strong><em>cli</em></strong>). This tool is invoked via the <strong><em>cli</em> </strong>command plus possible arguments. Commands are operating system commands to be executed under the Unix (or Linux) OS. Multiple commands are separated from one another by commas, and each may in turn have arguments. <em>Cli</em> ‘knows’ a list of commands a-priori (predefined). When invoked, <em>cli</em> checks, whether the first argument is an included, <strong><em>predefined</em></strong> command. If so, cli confirms this via a brief message. If not, a contrary message is emitted, stating this is not one the <em>predefined</em> commands. After the message, <em>cli</em> executes all commands in the order listed. After executing the last command, <em>cli</em> prints the current working directory, i.e. it acts as if the <strong><em>pwd</em></strong> command had been executed. Sample runs are shown further below.




Multiple commands of <em>cli</em> must be separated from one another by commas. Possible parameters of any one command are separated from the command itself (and from possible further parameters) by <strong><em>white space</em></strong>. <em>White space</em> consists of blanks, tabs, or a combination, but at least 1 blank space. Here some sample runs with single and multiple commands; outputs are not shown here:




./cli pwd

./cli rm –f temp, mv temp ../temp1

./cli ls –la

./cli rm a.out, gcc sys.c, cp a.out cli




The output of the <em>cli </em>command “cli pwd” or “./cli pwd” should be as shown below. Here is the output of a sample run with a single command line argument:




herbertmayer$ ./cli <strong>pwd </strong>hgm cli 4/12/2020

Legal commands:  cd exec exit gcc ls man more mv rm pwd sh touch which $path

2 strings passed to argv[] next string is ‘pwd’ new string is ‘pwd ‘

1st cmd ‘pwd’ is one of predefined.

/Users/herbertmayer/herb/academia/classes_Sac_State/csc139

Here the output of another sample run, also with a single cli:

herbertmayer$ ./cli <strong>ls</strong> hgm cli 4/12/2020

Legal commands:  cd exec exit fork gcc ls man more mv rm pwd sh touch which $PATH

2 strings passed to argv[] next string is ‘ls’ new string is ‘ls ‘

1st cmd ‘ls’ is one of predefined.

admin               cli.c         sac_state_yyy

backup_1_24_2020 docs            sac_state_hw

backup_3_9_2020 grades           sac_state_xxx

cli                 l_notes

/Users/herbertmayer/herb/academia/classes_Sac_State/csc139



















1

<strong>List of all commands supported by your cli</strong>:




char * cmds[ ] = {

“cd”,

“exec”,

“exit”,

“gcc”,

“ls”,

“man”,

“more”,

“mv”,

“rm”,

“pwd”,

“sh”,

“touch”,

“which”,

“$path”

};

<strong>To Do</strong>:

<ol>

 <li>Code for CLI in one single file.</li>

 <li>About four progressively more complex executions of your correctly working <strong><em>cli </em></strong>program, showing all user input and output.</li>

</ol>

2