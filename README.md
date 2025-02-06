# Tools

# Cheatsheets

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

### RPC - Remote Procedure Call

Access RPC anonymously:
> rpcclient -U "" -N <TARGET_IP>

after connecting try:
> serverinfo
> lsaenumsid
> netshareenumall
