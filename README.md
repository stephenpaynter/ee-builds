# ee-builds


login to registry.redhat.io

[stephenpaynter@aap ee-network]$ podman login registry.redhat.io  
Username: steve.paynter  
Password:  
Login Succeeded!  


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

[stephenpaynter@aap Ansible]$ cd project
[stephenpaynter@aap project]$ ls -al
total 8
drwxrwxr-x. 4 stephenpaynter stephenpaynter   90 Sep 30 13:30  .
drwxr-xr-x. 6 stephenpaynter stephenpaynter   59 Sep 30 13:56  ..
drwxrwxr-x. 8 stephenpaynter stephenpaynter 4096 Sep 30 13:58  artifacts
-rw-rw-r--. 1 stephenpaynter stephenpaynter  131 Sep 30 13:00  helloworld.yml
drwx------. 3 stephenpaynter stephenpaynter   23 Sep 30 13:20 'inventory--container-image=network_ee'


ansible-runner run project -p project/helloworld.yml 

ansible-runner run project -p helloworld.yml --container-image=network_ee


