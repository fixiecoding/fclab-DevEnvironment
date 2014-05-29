fc-Lab Developer Env!	{#welcome}
=====================


Easy to setup quickly after fresh installing OS.


----------


Data Tools
---------

**MiniConda** download from xxx

Installation
```
$ chmod +x filename.sh
$ ./filename.sh
```

**Spyder** download from xxx
```
$ sudo apt-get install python-qt4 python-sphinx
$ sudo pip install spyder
$ sudo pip install -U spyder


```

**Git/Vim** download from xxx
```
$ sudo apt-get install git
$ sudo apt-get install vim
```
```
// setup SSH
$ ssh -v
$ ls -a ~/.ssh

// generate new key
$ ssh-keygen

// create a SSH config file and paste the code with a single space indent
$ vim ~/.ssh/config

Host bitbucket.org
 IdentityFile ~/.ssh/id_rsa

// update ~/.bashrc profile with the code

SSH_ENV=$HOME/.ssh/environment
   
# start the ssh-agent
function start_agent {
    echo "Initializing new SSH agent..."
    # spawn ssh-agent
    /usr/bin/ssh-agent | sed 's/^echo/#echo/' > "${SSH_ENV}"
    echo succeeded
    chmod 600 "${SSH_ENV}"
    . "${SSH_ENV}" > /dev/null
    /usr/bin/ssh-add
}
   
if [ -f "${SSH_ENV}" ]; then
     . "${SSH_ENV}" > /dev/null
     ps -ef | grep ${SSH_AGENT_PID} | grep ssh-agent$ > /dev/null || {
        start_agent;
    }
else
    start_agent;
fi

// restart the shell and query SSH agent
$ ssh-add -l

// cat the public key file and add to bitbucket/github
$ cat ~/.ssh/id_rsa.pub
$ ssh -T git@bitbucket.org
$ ssh -T git@github.com

```


----------


Languages
---------

**Julia** download from xxx.
```
$ sudo apt-get update
$ sudo apt-get install julia
```



  [1]: http://linuxaria.com/howto/use-vim-at-its-best-to-edit-your-puppet-manifests?lang=en
  [2]: https://confluence.atlassian.com/display/BITBUCKET/Set+up+SSH+for+Git
