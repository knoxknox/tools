# Tools

### Utils:
- htop - process viewer
- iftop - network requests
- iotop - i/o usage by process

### Linux:
- ps - processes (`ps aux | grep <pid>`)
- lsof - list open files (`lsof -nPp <pid>`)
- proc - file descriptors (`ls -l /proc/<pid>/fd`)
- ltrace - trace calls by library (`ltrace -ttTp <pid>`)
- strace - trace system calls by os (`strace -ttTp <pid>`)

### Network:
- nc - send/receive packets (`nc -v <host> <port>`)
- dig - domain information (`dig <host>` / `dig -x <ip>`)
- lsof - connections by process (`lsof -i | grep <name>`)
- nmap - show opened network ports (`nmap -sT -O <host>`)
- ngrep - show network requests (`ngrep -d any <sitename>`)
- netstat - info about network connections (`sudo netstat -tunapl`)
- tcpdump - capture network traffic (`tcpdump -i eth0 tcp dst port 8080`)
- wireshark - packet analyzer (`tcpdump port 80 -w http.pcap` / `wireshark http.pcap`)

### CPU/Memory:
- gdb.rb - debugger (`gdb.rb <pid>`)
- memprof - heap visualizer for ruby (see memprof.com)
- perftools.rb - CPU performance tools (`pprof.rb /tmp/somefile -- text`)
