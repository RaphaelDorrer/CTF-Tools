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
