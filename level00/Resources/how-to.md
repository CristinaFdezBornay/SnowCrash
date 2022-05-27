# LEVEL 00

## 💡 Explanation

In this level we have to:
1. Find the files from the user 'flag00' which are not /proc
2. Decode the content of the files using caesar encoding (offset of 11)

## 👾 Commands

```
scp -P 4242 level02@192.168.56.3:/home/user/level02/level02.pcap ./level02/Resources/level02.pcap
find / -user flag00 2> /dev/null
cat /usr/sbin/john
```

## 🔍 Resources

- [Linux find command](https://linux.die.net/man/1/find)
- [Dcode Caesar](https://www.dcode.fr/chiffre-cesar)

## 🔥 Password
`nottoohardhere`
