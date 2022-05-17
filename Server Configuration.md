# SSH and User settings

## Creating SSH Key

```bash
cd ~/.ssh  #move to ssh directory
ssh-keygen  #Generate ssh key

ssh -I ~/.ssh/$ssh_key_file_name $username@$ip_address  #Log into the server using ssh
ssh-add -K ~/.ssh/$ssh_key_file_name  #Add private key to the keychain
```

## Update applications

```bash
sudo apt update  #update application
```

## User Management

```bash
adduser $user_name  #add new suer
usermod -aG sudo $user_name  #add user to the "sudo" group
su $user_name  #log in to the user

mkdir -p ~/.ssh  #create ssh directory
vi ~/ssh/authorized_keys  #Create authorized keys file and paste public key

chmod 644 ~/.ssh/$ssh_key_file_name  #change ssh file permissions
```

```bash
sudo vi /etc/ssh/sshd_config  #disable root access
```

```bash
sudo service sshd restart #Restart ssh daemon
```