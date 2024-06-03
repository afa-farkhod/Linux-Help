# Linux-help
### Linux useful commands and links


## Command list:
| Command | Description |
| --- | --- |
| `pwd & pbcopy` | copy current path in terminal |
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
- ss -tuln | grep PORT_NUMBER (checks the whether port is open or not)
- lsof -i :PORT_NUMBER (checks connected services to port)
- sudo chown -R  <USER_NAME>:staff  <FOLDER_NAME> (changes the folder ownership type e.g. from root to username )
- scp -P 60006 -i /Users/.ssh_keys/education2.key /Users/Downloads/mintstation.zip test@3434.1232323.187.2323:/home/test/  (copy file from local to remote server)
- scp testnet-sentry-14:~/test.txt testnet-sentry-13:~/
- sudo lsof -i :343434 ( check address in use?)
- nslookup grpc-evmos.test.io
- free -m (shows total memory)
- lscpu (cpu specs)
- nproc (number of processing units available.)
- lspci | grep VGA (graphics card)
- sudo iptables -L (firewall rules)
- ldd ${FILE_NAME} (used to find out the shared libraries required by a program)
- objdump ${FILE_NAME} (displays information about binary files.)
- uptime
- vmstat
- dmesg
- compgen -c will list all the commands you could run.
- pv -L 20m < archive.tar.gz | tar xvzf - (limits the unarchiving speed)
- wget https://node.tar.gz --limit-rate=10m (limits bandwidth speed)
- iostat -d -x 1 (disk i/o checking)
- pgrep -u USERNAME (finds running processes by username!)
- crontab (Unix command that creates a list of commands to be executed by the operating system (OS) at a specified time)
- lsblk (disk usage)
- ps -ef | grep idea -> kill -9 PID
- sudo iotop -o -b -n 10 -d 1 -u evmos-testnet | awk '{readSum+=$4; writeSum+=$6; count++} END {print "Average Read: " readSum/count " kB/s, Average Write: " writeSum/count " kB/s"}'
Output:
Average Read: 0.362923 kB/s, Average Write: 79.4283 kB/s

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
- While Server-A node is running and we want to copy the data of Server-A to Server-B, in this case we can use `rsync`.
  - [rsync](https://linux.die.net/man/1/rsync) - Rsync is a fast and extraordinarily versatile file copying tool. It can copy locally, to/from another host over any remote shell, or to/from a remote rsync daemon.
   ```
   # current command is run from Server-A location. So we run the following command serveral times untill all data is copied, and finally to make the data as similar to original one, we run the command by stopping Server-A node.
   rsync -e 'ssh -i /path/to/remote/access/ssh-key' --partial-dir=.rsync-partial -avv /path/to/copy/folder [Server-B-username]@[Server-B-ipaddress]:/path/to/copy/folder
   ```

## Useful terminology

- `SSL` (Secure Sockets Layer) certificate is a digital certificate that authenticates the identity of a website and encrypts information sent between the server and the client. If you run a cloud instance and build a Linux-based server, you will need an SSL/TLS certificate to secure any sensitive data transmitted between your server and its clients. It can free and paid

## Reference

- [YouTube](https://www.youtube.com/watch?v=07JOqKOBRnU&list=PLT98CRl2KxKHKd_tH3ssq0HPrThx2hESW&index=8) - Linux Crash Course (Learn Linux TV channel)
