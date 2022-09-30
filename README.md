# Ansible EE Builds 

login to registry.redhat.io

'podman login registry.redhat.io'
'Username: steve.paynter'  
'Password:              '
'Login Succeeded!  '


Build the container

ansible-builder build --tag network_ee -v 3



structure

[stephenpaynter@aap Ansible]$ ls -al
total 4
drwxr-xr-x.  6 stephenpaynter stephenpaynter   59 Sep 30 13:56 .  
drwx------. 18 stephenpaynter stephenpaynter 4096 Sep 30 13:54 ..  
drwx------.  3 stephenpaynter stephenpaynter   23 Sep 30 13:56 ee   
drwxr-xr-x.  2 stephenpaynter stephenpaynter   21 Sep 30 13:31 env   
drwxr-xr-x.  2 stephenpaynter stephenpaynter   23 Sep 30 13:30 inventory   
drwxrwxr-x.  4 stephenpaynter stephenpaynter   90 Sep 30 13:30 project  
[stephenpaynter@aap Ansible]$  


  
  
ansible-runner run  -p helloworld.yml .   from within directory where project is. 


ansible-runner run -p helloworld.yml . --container-image=network_ee  to change image from one specified in env.  


