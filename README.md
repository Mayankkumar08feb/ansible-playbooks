# ansible-playbooks
Download this playbook in your Ansible machine.
This playbook has been written as role base Apache configuration.
Please complete the pre-request steps before excuting main playbook.

Pre-Request:

Steps:-
        This playbook has been written base on SSL configuration. Need to plase your Certificate on Below mention Path and define it on variable file. steps are mention below.
        
       
Step1:-  Place you certificate on location 
         
         Apache_rolebase_script/files/certs/STAR_crashmeal_com_key
         Apache_rolebase_script/files/certs/STAR_crashmeal_com.crt
         Apache_rolebase_script/files/certs/COMODO_DV_SHA-256_bundle.crt
         
Use Command to copy Certificate in you machine:-
         
         #cp <Certificate location>  <pull path >/Apache_rolebase_script/files/certs/
 
Note:   Below mention files are Dummy file which place in location for reference.

          STAR_crashmeal_com_key
          STAR_crashmeal_com.crt
          COMODO_DV_SHA-256_bundle.crt


Step2:- Define New SSL-certificate file  Name in Varible file under "files_SSLname:" (Some Name has been already added in, Please remove it and Add your certificate Name as mention)"


files_SSLname:
  - COMODO_DV_SHA-256_bundle.crt    ---> Replace the Name with New SSL-certificate's file 
  - STAR_crashmeal_com.crt
  - STAR_crashmeal_com_key
  
  
Use Command to Edit Varible file in you machine:-

          #vi < Full path>/Apache_rolebase_script/vars/main.yml


Step3:- Define website Name in Varible file under "documents_filename:" (Some Name has been already added in, Please remove it and Add your website Name as mention)" 
        
 
Use Command to Edit Varible file in you machine:-

          #vi < Full path>/Apache_rolebase_script/vars/main.yml
 
 Note: Replace the Value of documents_filename as mention below. 
    
    documents_filename:
  - www.crashmeal.com           --> www.yourwebsite1.com
  - admin.crashmeal.com         --> www.yourwebsite2.com
  - api.crashmeal.com           --> www.yourwebsite3.com
  - auth.crashmeal.com
  - copycrashmeal.com
  - crashmeal.com
  - driver.crashmeal.com
  - partner.crashmeal.com
  - www.noqcart.com
  - testwww.crashmeal.com

Use Command to Edit Varible file in you machine:-

          #vi < Full path>/Apache_rolebase_script/defult/main.yml

 Note: Replace servername Value of apache_vhosts as mention below. 

- servername: "www.crashmeal.com"   --> www.yourwebsite1.com

- servername: "admin.crashmeal.com" --> www.yourwebsite2.com
    
# ansible-playbook is ready with pre-request changes.

Define your Host machince invenstory file ( defult path /etc/Ansiable/hosts or, you wanns to seperate ---> Choose as you wise)

Gohead and Hit the Command

# ansible-playbook Apache_web_playbook

      
