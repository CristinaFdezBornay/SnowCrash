# LEVEL 01

## 💡 Explanation

In this level we have to:
1. Copy the file `/etc/passwd` from the VM to our computer
2. Use our friend john to give us the password

## 👾 Commands

```
cat /etc/passwd | grep "flag01"
scp -P 4242 level01@192.168.56.3:/etc/passwd ./level01/etc_passwd
john level01/etc_passwd --show
```

## 🔍 Resources

- [John - Simple user guide](https://linuxcommandlibrary.com/man/john)

## 🔥 Password
`abcdefg`
