You will need these files to run exercise

1) 'hosts' is a file that contains data for authorization on ansible-served hosts. For example:
[ansible1]
192.168.10.10

2) ssh keys 'id_rsa' and 'id_rsa.pub'
'id_rsa.pub' Public key to publish on a remote server in order to connect to it from the ansible-served host
id_rsa is a private key which will be encrypted in this exercise

3) 'pass_vault' - is a password of encrypted 'id_rsa'
command to create it:
ansible-vault encrypt --vault-password-file pass_vault id_rsa

To start the exercise, you need to make sure that all these files are present and run the command
ansible-playbook -v create_user.yml --vault-password-file pass_vault

