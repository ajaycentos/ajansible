# ajansible
My ansible codes

To copy private key to all nodes
ansible all -i /home/ajay/inventory -m copy -a "src=/home/ajay/.ssh/id_rsa dest=/home/ajay/.ssh/id_rsa mode=600 owner=ajay group=ajay" --become

To copy /etc/hosts in all nodes
ansible -i ../../inventory all -m copy -a "src=/etc/hosts dest=/etc/hosts" --become
