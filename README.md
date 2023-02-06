# Shell Scripting
some training and useful files for shell scripting


## To make simple hello world bash script writ the following commands
<b>create the file with:</b></br>
<i>touch hello_world.sh</i> </br>
<b>decide the shell with:</b></br>
<i>echo "#! /bin/bash" >> hello_world.sh</i> </br>
<i>echo "echo 'hello world'" >> hello_world.sh</i> </br>
<b>then we have to change the permissions with:</b> </br>
> <b>NOTE:</b> it's not good to add a permission to all users you may use <i>'chmod u+x'</i> to change for the user only </br>

<i>chmod +x ./hello_world.sh</i> </br>
<b>then call the file in the terminal with:</b> </br>
<i>./hello_world.sh</i> </br>


## Piplines
pipelines are where the input of a state is the output of the previous one and so on. </br>
<b>you can use the pipeline as follows</b> <i> cmd1 | cmd2 </i> </br>
so imagin we have a file and want to get the unique values of it we can do this </br>
<i>sort [file name] | uniq </i></br>

<b>Some commands, such as tr, only accept "standard input" as input (not strings or filenames)</b></br>
we use pipline for them as follows:</br>
<i>echo "Linux and shell scripting are awesome\!" | tr "aeiou" "_"</i></br>
<b>OUTPUT: </b> <i>L_n_x _nd sh_ll scr_pt_ng _r_ _w_s_m_!</i></br>

It's also pretty useful filtering text or o/p of curl commands with grep as follows: </br>
<i>curl -s --location --request GET https://www.example.com | grep -oE "\"price\":\s*[0-9]*?\.[0-9]*"</i></br>

## Metacharacters
\# for comments</br>
; for ending one command to start another in the same line</br>
\* indicates any number of charecters as in 'ls /bin/bas*'</br>
? indicates 1 character as in 'ls /bin/?ash'</br>
\ this is used before metacharactes to interpret them as text</br>
"" must use \ before metacharacters while '' interpret all text as text</br>

\> redirect output to file and create one if not existed and override if it exists</br>
\>> append output to file</br>
2> catchs error and writes them to a file</br>
2>> catchs error and apend it to a file</br>
< to pass file content to a standard i/p command</br>

&(command) or \`command\` is used for replacing command with its o/p as in $ variable=$(pwd)</br>
./random_file arg1 arg2  passing arguments to shell script</br>

; runs commands sequentially</br>
& runs commands parrelel</br>


## Scheduling jobs
cron allows u to do that</br>
crond is the cron deamon which checks 'crontab files' every minute and submits job to cron</br>
crontab is a table contains jobs and scedule data
<i>crontab -e</i> opens the editor</br>
<b>U add commands describing jobs as follows:</b></br>
<i>m h dom mon dow command</i></br>
all 5 position must have numeric or * for any</br>
> dow 0:sunday and so on</br>

<i>crontab -l</i> gets the jobs and scedules
