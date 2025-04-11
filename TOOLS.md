# Tools

## Linux PrevEsc
Use linPEASS to get information:
> wget https://github.com/peass-ng/PEASS-ng/releases/latest/download/linpeas.sh

Use pspy when there are weird processes to monitor them.

## SMB File Shares

List all shares on SMB Share:
> smbclient -L {ip-address}

Access a speific share:
> smbclient //{host}/{share}

## LDAP

Get some general information:
> ldapsearch -x -h <ip> -b "" -s base "(objectclass=*)"

Perform Username enumeration:
> kerbrute userenum -d <ip-address> --dc <domain-controller> <wordlist>

Does most of the heavy lifting:
> python3 enum4linux-ng.py -As 10.10.11.35 -oY out > ../out.txt

Bruteforce RID's using Guest Authentication
> netexec smb <DOMAIN/TARGET_IP> -u zaa -p "" --rid-brute

### RPC - Remote Procedure Call

Access RPC anonymously:
> rpcclient -U "" -N <TARGET_IP>

after connecting try:
> serverinfo
> 
> lsaenumsid
> 
> netshareenumall

## Web

Get different sites:
> feroxbuster -u http://<IP_OF_TARGET> -w <PATH_TO_DIRECTORY_LIST>

Directory Search/Traversal:
> python3 dirsearch.py -e php,html,js -u http://<TARGET_IP> -w <WORDLIST>

# Links
Some very usefull sites I found:

Very usefull for Linux Security and PrivEsc:
> https://book.hacktricks.wiki/
and
> https://gtfobins.github.io/#
