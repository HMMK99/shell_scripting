# shell_scripting
some training and useful files for shell scripting


## To make simple hello world bash script writ the following commands
<b>create the file with:</b></br>
<i>touch hello_world.sh</i> </br>
<b>decide the shell with:</b></br>
<i>echo "#! /bin/bash" >> hello_world.sh</i> </br>
<i>echo "echo 'hello world'" >> hello_world.sh</i> </br>
<b>then we have to change the permissions with:</b> </br>
<b>NOTE:</b> it's not good to add a permission to all users you may use <i>'chmod u+x'</i> to change for the user only </br>
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
