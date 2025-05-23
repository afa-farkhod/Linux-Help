# Linux-help
### Linux useful commands and links


## Command List:
| Command | Description |
| --- | --- |
| `pwd & pbcopy` | copy current path in terminal |
| `cat /etc/os-release` | shows OS related information |
| `lsb_release -a` | shows OS related information |
| `bash_profile`, `profile` and `zshrc` | are important configuration files |
| `psql -d postgres -U postgres` | postgres start command in terminal |
| `sudo dmidecode -t memory` | shows linux hardware info |
| `ps -x` | linux server process status |
| `ps -uxww` | linux server process status by user |
| `ps -aux` | process list |
| `nohup $CMD start` | run service in background |
| `uname -a` | terminal OS check command |
| `pwd` | terminal shows current folder directory path |
| `whoami` | Linux Terminal Username checking |
| `lz4 -d FILE_NAME.lz4` | used to decompress lz4 archive files |
| `tar -xvf FILE_NAME.tar` | used to extract tar archive file |
| `tar -cvf archive.tar /path/to/folder` | used to make archive file |  
| `free -h` | Displays overall memory and swap usage in a human-readable format |
| `sha256sum filename` | checks the file authenticity |
| `vimdiff file1.txt file2.txt` | compare two files |
| `wget https://example.com/file.zip` | download files from web | 
| `screen -S <NAME>` | creates session on the current terminal |
| `screen -ls` | shows sessions list |
| `screen -X -S <PID_NUMBER> kill` | kills the session |
| `Ctrl+A+D` | while inside the screen session, exits the session without stopping the session itself |
| `screen -r` | goes back to the running session |
| `netstat -tunlp grep USER` | shows network related information |
| `du -sh *` | used to display disk usage statistics |
| `df -h` | displays information about disk space usage on the system | 
| `tree -d` | shows current folder tree structure |
| `sudo netstat -tulnp grep 20302` | checks the particular port usage | 
| `curl ifconfig.me` | shows current ip address |
| `ln -sf file1.txt link_to_file1.txt` | used to create a symbolic link |
| `ssh-add ~/.ssh_keys/test-20231020` | adds key |
| `sudo ufw status` | shows firewall status |
| `sudo ufw allow PORT_NUMBER/tcp` | adds the particular port number to firewall rules |
| `sudo ufw delete allow PORT_NUMBER/tcp` | deletes the particular port number from firewall rules |
| `ss -tuln / grep PORT_NUMBER` | checks the whether port is open or not | 
| `lsof -i :PORT_NUMBER` | checks connected services to port |
| `sudo chown -R  <USER_NAME>:staff  <FOLDER_NAME>` | changes the folder ownership type e.g. from root to username |
| `scp -P 60006 -i /Users/.ssh_keys/test.key /Users/Downloads/test.zip test@3434.1232323.187.2323:/home/test/` | copy file from local to remote server |
| `scp testnet-sentry-14:~/test.txt testnet-sentry-13:~/` | copies the file from one remote server to another remote server |  
| `sudo lsof -i :343434` | check address in use? | 
| `nslookup grpc-test.io` | check the grpc endpoint availability |
| `free -m` | shows total memory |
| `lscpu` | cpu specs |
| `nproc` | number of processing units available |
| `wget -q -O - test.tar / tar -xvf -` | following command downloads the *.tar file and at the same time unarchives the file |
| `lspci / grep VGA` | shows graphics card information |
| `sudo iptables -L` | shows ufw firewall rules |
| `ldd ${FILE_NAME}` | used to find out the shared libraries required by a program |
| `objdump ${FILE_NAME}` | displays information about binary files |
| `uptime` | shows number of users, for how long the server is up and load average details |
| `vmstat` | The vmstat command, short for "virtual memory statistics", is a built-in Linux utility that provides information about system activity, including memory, processes, paging, interrupts, block I/O, disk, and CPU scheduling |
| `dmesg` | The dmesg command in Linux displays messages from the kernel ring buffer, which contains information about hardware, device drivers, and kernel modules during system startup. The name "dmesg" is derived from "display message" |
| `compgen -c` | will list all the commands you could run. |
| `pv -L 20m < archive.tar.gz / tar xvzf -` | limits the unarchiving speed |
| `sudo apt-key list` | Displays a list of public keys stored on your system that are used by the APT package manager to verify the authenticity of software packages. | 
| `last reboot` | This command will list all the reboot entries, showing you the date and time of each reboot |
| `uptime --since` | The command outputs a single line showing the last boot time in a readable format |
| `gzip -d test.gz` | to unarchive the *.gz archive files |
| `wget https://node.tar.gz --limit-rate=10m` | limits bandwidth speed for downloading particular file |
| `iostat -d -x 1` | disk i/o checking |
| `pgrep -u USERNAME` | finds running processes by username |
| `aria2c -x16 -s16 <URL LINK>`| aria2c is better when compareed to wget/curl because it tries to utilize your maximum download bandwidth |
| `crontab` | Unix command that creates a list of commands to be executed by the operating system (OS) at a specified time |
| `lsblk` | in Linux lists block devices, such as hard drives and solid state drives, connected to your computer. It displays information about these devices in a tree-like format, including disk partitions and their sizes|
| `ifconfig -a` | used to display detailed information about all the network interfaces on the system, both active and inactive. |
| `ps -ef / grep idea => kill -9 PID` | find process of IDEA and kill the process, used when IDEA is not responding | 
| `sudo snap install --channel=1.22/stable --classic` | to install particular go version using snap |
| `sudo iotop -o -b -n 10 -d 1 -u evmos-testnet / awk '{readSum+=$4; writeSum+=$6; count++} END {print "Average Read: " readSum/count " kB/s, Average Write: " writeSum/count " kB/s"}'` | Output: Average Read: 0.362923 kB/s, Average Write: 79.4283 kB/s |
| `sudo ufw allow from IP_ADDRESS comment "test-server"` | adds the particular IP_ADDRESS to ufw rule, opens the firewall from the ip |
| `sudo userdel -f USER_NAME` | orce the removal of a user |
| `sudo certbot --nginx -d <DOMAIN_NAME> -m <EMAIL_ADDRESS>` | certificate creation for particular domain name |
| `awk '$0 >= "Sep 25 13:47:00" && $0 <= "Sep 25 13:50:00"' ./cosmovisor.log` | To view logs from a particular time to another time |
| `awk '$0 ~ /dymension_1100-1/ && $0 ~ /Dec 22 12:4[89]:[0-9][0-9]/' ./tenderduty.log` | to veiew logs from a particular time (12:48:02 ~ 12:49:58) of particular keyword |
| `cat /sys/block/nvme0n1/queue/rotational` | To check whether the disk is an SSD or HDD rotational or non-rotational (SSD - 0 and HDD - 1) |
| `cat /proc/mdstat` | List All Active RAID Arrays | 
| `sudo usermod -l NEW_USER_NAME OLD_USER_NAME` | change `uid=1003(cryptoorg)` |
| `sudo groupmod -n NEW_USER_NAME OLD_USER_NAME` | change `gid=1003(cryptoorg)` | 
| `tar -czvf archive-name.tar.gz /path/to/directory` | To archive and compress a directory, you can use the tar command with a compression option to reduce its size. | 
| `ls -lart` | lists all files (including hidden ones) in reverse chronological order, showing the oldest files first and the newest ones last, along with detailed information for each |
| `state <FILE>` | The stat command provides detailed information about files and directories. |
|`cd $(dirname $(which agd))`|finds the to binary and moves to that directory|

## Troubleshooting

- Libwasms mistmach error type: `Error: libwasmversion mismatch. got: 1.2.3; expected: v1.5.0`
  - to solve the problem, we need to show the path of the `libwasmvm.x86_64.so` binary
  - In Linux set the path in profile:
    ```
    vim ~/.profile
    export LD_LIBRARY_PATH="$LD_LIBRARY_PATH:/path/to/libwasmvm.x86_64.so"
    source ~/.profile
    ```
  - also if you are running service file then you should also set the library path in service file in Linux OS as following:
    ```
    sudo vim /etc/systemd/system/<SERVICE_FILE_NAME>.service
    # add following:
    Environment="LD_LIBRARY_PATH=/path/to/libwasmvm.x86_64.so"
    sudo systemctl daemon-reload
    ```
--------------------------------------------------------------------------------------------------------
- While Server-A node is running and we want to copy the data of Server-A to Server-B, in this case we can use `rsync`.
  - [rsync](https://linux.die.net/man/1/rsync) - Rsync is a fast and extraordinarily versatile file copying tool. It can copy locally, to/from another host over any remote shell, or to/from a remote rsync daemon.
   ```
   # current command is run from Server-A location. So we run the following command serveral times untill all data is copied, and finally to make the data as similar to original one, we run the command by stopping Server-A node.
   rsync -e 'ssh -i /path/to/remote/access/ssh-key' --partial-dir=.rsync-partial -avv /path/to/copy/folder [Server-B-username]@[Server-B-ipaddress]:/path/to/copy/folder
   ```
--------------------------------------------------------------------------------------------------------
- To extract the `executable binary` from Docker image follow this:
  - pull the docker image file:
```
docker pull ghcr.io/unionlabs/uniond-release:v${TAG}
```
  - then search for binary uniond in nix store with following command
```
sudo find /var/lib/docker/ -name "uniond" | grep $(uname -m)
```
  - then copy the executable binary to your destination (ready for use)
--------------------------------------------------------------------------------------------------------
- When `rustup` isn't installed on your system
  ```
  # install rustup
  curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

  # set environment in .profile:
  source $HOME/.cargo/env

  # run, it should be good now
  rustc --version
  ```
--------------------------------------------------------------------------------------------------------
- To broadcast the message in remote server so that everyone on that server at the same time could see the message:
  ```
  sudo wall "This is a broadcast message to all users"

  wall -help

  Usage:
   wall [options] [<file> | <message>]

  Write a message to all users.

  Options:
   -g, --group <group>     only send message to group
   -n, --nobanner          do not print banner, works only for root
   -t, --timeout <timeout> write timeout in seconds

   -h, --help              display this help
   -V, --version           display version
  ```  
--------------------------------------------------------------------------------------------------------
- When we try to do in Linux server sometimes we get similar error as following:
  ```
  usermod: user cryptoorg is currently used by process 1228221

  # in this case simply run the following command to see for full process:
  ps -p 1228221 -o pid,user,cmd

  # and we can get the result as following:
      PID USER     CMD
      1228221 cryptoo+ /home/cryptoorg/go/bin/cosmovisor run start --home /data/node/.chain-maind
  ```
--------------------------------------------------------------------------------------------------------
- To ensure that the `grep` command shows the next two lines following each match of `grpc-web`, we can use the `-A` option, which stands for "after" and specifies the number of lines to include after each match.
```
grep -rn "grpc-web" -A 2
```
  - This will search recursively (-r), show line numbers (-n), and include the three lines following each match (-A 2).
--------------------------------------------------------------------------------------------------------
- While installing some go related modules or packages, sometimes we see following type of error:
  ```
  go: creating work dir: mkdir /tmp/go-build1127798198: permission denied

  # Check Permissions on /tmp: Make sure the /tmp directory is writable by your user. You can check this by running:
  ls -ld /tmp

  # The output should show permissions like drwxrwxrwt (the t at the end is crucial for shared temp directories).
  # If permissions are different, you may need to adjust them:
  sudo chmod 1777 /tmp
  ```
--------------------------------------------------------------------------------------------------------
- Sometimes we need to watch education related videos which can't be skipped, in this case simply use the following method:
  ```
  # just type the code in console
  교육시작 > F12 >  parent[0].next_click('9.html', "Y"); 입력 > 교육종료
  ```

--------------------------------------------------------------------------------------------------------

- To check if remote server is `bare metal` or `virtual machine` use DMI (Desktop Management Interface) Linux only method
  ```
  # run following command:
  sudo dmidecode -t system

  # Look for the Manufacturer and Product Name fields:
  # For bare metal servers, these fields typically indicate a hardware vendor like Dell, HP, Supermicro, etc.
  # For virtual machines, these fields might show virtualization providers like VMware, QEMU, VirtualBox, or Microsoft Corporation.

  # Example outcome
  # dmidecode 3.5
  Getting SMBIOS data from sysfs.
  SMBIOS 3.6.0 present.
  # SMBIOS implementations newer than version 3.5.0 are not
  # fully supported by this version of dmidecode.
  
  Handle 0x0001, DMI type 1, 27 bytes
  System Information
  	Manufacturer: Supermicro
  	Product Name: AS -3015MR-H8TNR
  	Version: 01234xxxx
  	Serial Number: E89xxxx
  	UUID: 00000000-0000-0000-0000-7cxxxxx
  	Wake-up Type: Power Switch
  	SKU Number: To be filled by O.E.M.
  	Family: Family
  
  Handle 0x000D, DMI type 32, 20 bytes
  System Boot Information
  	Status: No errors detected
  ```
--------------------------------------------------------------------------------------------------------
```
# set swap memory (ex: 64GB)
swapon --show
sudo dd if=/dev/zero of=/swapfile bs=1G count=64 status=progress
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
swapon --show
free -h

# remove swap memory
sudo swapoff /swapfile
sudo rm -f /swapfile
swapon --show
free -h
```
--------------------------------------------------------------------------------------------------------
- Manual `data` copy from the old host to new host:
  
```
#before proceeding further, check the old server for 22 port firewall 
sudo ufw status
22/tcp (v6)                ALLOW       Anywhere (v6)

#if you don't see that, run following command:
sudo ufw allow 22/tcp

#Log into the new host
#Need to have ssh key in authorized_keys which allows to ssh access the new old server from new server.
#then run as an example:

rsync -avz --progress -e "ssh -i ~/.ssh_key/test-key" $OLD_HOST_USER_NAME@$OLD_HOST_IP:/data/db /data/db

#after, stop the related services on the old host and on the new host do a second rsync with the --delete option (to only keep files that exist on the old host):

rsync -avz --delete --progress -e "ssh -i ~/.ssh_key/test-key" $OLD_HOST_USER_NAME@$OLD_HOST_IP:/data/db /data/db
```

--------------------------------------------------------------------------------------------------------

## Useful terminology

- `SSL` (Secure Sockets Layer) certificate is a digital certificate that authenticates the identity of a website and encrypts information sent between the server and the client. If you run a cloud instance and build a Linux-based server, you will need an SSL | TLS certificate to secure any sensitive data transmitted between your server and its clients. It can be free and paid.

## Reference

- [YouTube](https://www.youtube.com/watch?v=07JOqKOBRnU&list=PLT98CRl2KxKHKd_tH3ssq0HPrThx2hESW&index=8) - Linux Crash Course (Learn Linux TV channel)
