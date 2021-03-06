
# NFDI4Chem Ontology Lookup Service 2.0 - Vagrant Box


**Installs the different software components which make up NFDI4Chem Ontology Lookup Service 2.0 in a Vagrant virtual box**, namely:
* [ts-fronted-2.0-nfdi4chem](https://github.com/NFDI4Chem/ts-fronted-2.0-nfdi4chem)
* [ts-backend-2.0-common ](https://github.com/NFDI4Chem/ts-backend-2.0-common)



## Requirements to run box
* [Git](https://git-scm.com/downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)


## Start box

Run the following steps in Terminal (Linux/macOS) or GitBash (Windows):
```bash
git clone https://github.com/NFDI4Chem/ts-box-2.0-nfdi4chem.git
cd ts-box-2.0-nfdi4chem
vagrant up
```
`vagrant reload --provision` will re-run the Ansile playbook in the created Vagrant box


## Stop and Restart box

It is possible to shut down the virtual box and restart it again in order to save CPU and RAM.

```bash
# shut down
vagrant halt

# restart
vagrant reload --provision
```

In order to suspend the virtual box (save the state) use suspend and resume.

```bash
# save the state to disc
vagrant suspend

# resume from disc
vagrant resume
```

## Access
* BOX IP: http://192.168.100.100
    * Frontend: http://192.168.100.100:5000/
    * Backend: http://192.168.100.100:8000/
* source code directory (to which git repos are cloned): `/usr/local/src/`
* monitor services: `vagrant ssh --command "sudo pm2 list"`

`curl -I  http://192.168.100.100/ts/ `
