Web-serverices yml script

Pre-steps:-

Note:- Need to complete below mention step before Running this script.

STEP1:-

Copy SSL certificate, Web-code and latest SSL.conf placed it on Ansible-controller Machine.Upadate the New path in script

make changes in script and update the New path
 (Line no 22) (src: ~mayank/ssl/29-June-2019/)


Place Web-code in Ansible-controller Machine
Make changes in Line no.28 
src: /home/mayank/test.html


Update the latest SSL.conf and place it in Ansible-Controller Machine. Upadate the New path in script. 
Line no.36 
src: /home/mayank/ssl.conf


$vi crashmeal_web.yml

In Command Mode Press "ESC" and type below command to get line no.

a.) 	ESC { to sure, you are in command mode}

b.) 	:set nu { Type this command to get line number}

c.) 	Press " I " or "Insert" Button to move, edit mode.

d.) 	Make above mention changes

e.)	ESC { to sure, you are in command mode}

f.)	:wq or :wq! { save and quite}

g.)	Validate the changes with below mention command 

$ansible-playbook crashmeal_web.yml --syntax-check

Note:- No Error should be found, If in case of any error contact to SysAdmin.






STEP2:-

STEP3:-


