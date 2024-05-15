# Linux-help
### Linux useful commands and link

- `pwd` & `pbcopy` - copy current path in terminal
- `lsb_release -a` - shows OS related information

- nano~/.bash_profile OR nano ~/.zshrc (path configuration and addition - terminal)
- psql -d postgres -U postgres (postgres start in terminal)
- postgres terminal command -> \l (list all DBs)
- nohup centaurid start &   (run node in background)
- ps -x (linux server process status)
- ps -uxww (linux server process status by user)
- ps -aux (process list)
- uname -a (Terminal OS check command)
- pwd (Terminal shows current folder directory path)
- whoami (Linux Terminal Username checking)
- lz4 -d FILE_NAME.lz4 (used to decompress lz4 archive)
- tar -xvf FILE_NAME.tar (used to extract tar archive)
- tar -cvf archive.tar /path/to/folder
- free -h (Displays overall memory and swap usage in a human-readable format)
- sha256sum filename (checks the file authenticity)
- vimdiff file1.txt file2.txt (compare to files)
- wget https://example.com/file.zip (linux - downloading files from the web)
- screen -S <NAME> (creates session on the current terminal)
- screen -ls (shows sessions list)
- screen -X -S <PID_NUMBER> kill (kills the session)
- Ctrl+A+D (while inside the session, exits the session without stopping the session itself)
- screen -r (goes back to the running session)
- netstat -tnlp | grep <NODE_NAME> (shows network related information)
- du -sh * (used to display disk usage statistics)
- df -h ( display information about disk space usage on the system)
- tree -d (shows current folder tree structure)
- sudo netstat -tuln | grep 20302 ( checks the port usage)
- curl ifconfig.me (shows current ip address)
- ln -sf file1.txt link_to_file1.txt (used to create a symbolic link )
- ssh-add ~/.ssh_keys/test-20231020  (adds key)
- sudo ufw status (shows firewall status)
- sudo ufw allow PORT_NUMBER/tcp 
- sudo ufw delete allow PORT_NUMBER/tcp            
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
--------------------------------------------------------------------------------------------------------------------------

## Reference

- [YouTube](https://www.youtube.com/watch?v=07JOqKOBRnU&list=PLT98CRl2KxKHKd_tH3ssq0HPrThx2hESW&index=8) - YouTube linux learning material
