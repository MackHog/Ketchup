# GIT

## Add another git account with SSH
### Step 1: Create new SSH key
open bash
```
 ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
``` 
save file to 
```
/c/Users/YOU/.ssh/id_rsa_{new name}
``` 

### Step 2: Upload SSH key to your github account
Copy public key from ```id_rsa_{new name}.pub``` and go to https://github.com/settings/keys and create new key

### Step 3: Add SSH config file to your user
Go to ```C:\Users\{your user}\.ssh\``` and create a config file with following content

```
Host github.com-Company
    HostName github.com
    User git
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/id_rsa
    IdentitiesOnly yes
Host github.com-MackHog
    HostName github.com
    User git
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/idx_rsa
    IdentitiesOnly yes
```

### Step 4: Point your repo to the ssh-key
Go to ```.git\config``` in your repository.

To point out which Host to use, use the value after ```-```. <br>
For example: ```github.com-MackHog``` ==> ```MackHog```

Then replace the host-name ```git@github.com-{host-name}:MackHog/PROJECT.git``` with that value

Result
```
[remote "origin"]
    url = git@github.com-{host-name}:MackHog/PROJECT.git
    fetch = +refs/heads/*:refs/remotes/origin/*
```

### Step 5: Ensure the correct user is used for the commit
Go to the repo and set the user.email

```git config user.email {email}```
