# k8s_coaching

To setup labs please follow below instructions:

1] Install choco in windows -> open powershell using admin permission

run below command to install:
 > Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

After that check  installed choco by running "choco" in terminal, you should be getting some output.

2] Disable hyper-v in windows 11/10 please check if it is enabled: This is prerequisite for VM/virtualbox to work.
https://www.makeuseof.com/windows-11-disable-hyper-v/

3] Install virtualbox: we are using last stable version provided link for the same.
https://www.virtualbox.org/wiki/Download_Old_Builds_6_1

4] Install mobaxterm, k9s, cygwin, vagrant, kubernetes-cli using "choco install", using admin previledge.

By running below command you can install above tools:
> choco install mobaxterm
> choco install k9s
> choco install cygwin
> choco install vagrant 
> choco install kubernetes-cli

5] Git clone this repo.
git clone https://github.com/gauravkhedekar/k8s_coaching.git

5.1] Please keep  virtualbox app open in the background running. Please disable/pause antivirus.

6] After that please run "vagrant up" in the folder where we have this cloned repo/where you can see Vagrantfile. It should create 1 master and 2 worker node for you.

7] You can go ahead and get ssh session from mobaxterm/putty/cmd/gitbash to the servers
  master - 172.16.16.100 
 slaves 1- 172.16.16.101 
 slave 2 -  172.16.16.102
 
For all servers:
Username: vagrant
Password: vagrant
