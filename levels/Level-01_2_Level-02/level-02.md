# **LEVEL 01 TO LEVEL 02**

## **Objective**
Find the password for the next level. It is stored in a file literally named `-` (a single dash) located in the home directory. This level is solved using basic Linux commands (`ls`, `cd`, `cat`, `file`, `du`, `find`).

## **Initial Information**
1. The password for the next level is in a file called `-` (a dash is the actual filename, not a placeholder).
2. The file is located in the home directory.

## **Enumeration or Analysis**
1. List the files and directories in the home directory to locate the target file.
2. Read the file, because that is where the password is stored.
3. Note the difficulty: a filename made only of a dash cannot be read with a plain `cat -`, because `-` is interpreted as standard input (stdin) instead of a filename.

## **Approach**
1. Know your current path with the command `pwd`.
2. List the files and directories to find `-` with the command `ls`.
3. Try to read the file with `cat -` and observe that it does not work (it waits for keyboard input).
4. Read the file correctly by giving it a path so the dash is treated as a filename: `cat ./-`.

## **Commands Used**
- **pwd:** To know the current path.
- **ls:** To list the files and directories in the home directory.
- **cd:** To move into a directory.
- **cat:** To read the content of a file.
- **cat ./-** / **cat /home/bandit1/-**: To read a file whose name starts with a dash, by prefixing a path so `-` is not treated as an option or as stdin.

## **Solution**
1. Confirm the current path with `pwd`. It shows `/home/bandit1` (you land here automatically after logging in through SSH).
2. List the contents with `ls`. The only item shown is the file named `-`.

```bash
ls
```

3. A first attempt with `cat -` fails: the terminal seems to hang, because `-` is read as standard input instead of the file.

```bash
cat -
```

4. Read the file by prefixing `./` so the shell treats `-` as a filename in the current directory. This prints the password.

```bash
cat ./-
```

   An equivalent alternative is to use the full path or an input redirection:

```bash
cat /home/bandit1/-
cat < -
```

5. Use the retrieved password to log into the next level over SSH on port 2220:

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

## **Explanation**
The home directory contains a single file whose name is just a dash (`-`). Most command-line tools, including `cat`, interpret a bare `-` as standard input rather than as a filename, so `cat -` waits for keyboard input instead of reading the file.

To read the file, the shell must be told that `-` is a filename, not an option. This is done by prefixing a path: `./-` (current directory), `/home/bandit1/-` (absolute path), or by redirecting the file into `cat` with `cat < -`. Any of these reveals the password for the next level.

The commands `file`, `du`, and `find` were not required here, although `find` could confirm the file exists (`find . -name '-'`).

## **Concepts Learned**
- Files can have names made of special characters, such as a dash (`-`).
- A bare `-` is commonly interpreted as standard input (stdin), not as a filename.
- Prefixing a path (`./` or an absolute path) forces the shell to treat the name as a file, not an option.

## **Conclusion**
The password was found in a file literally named `-`, located in the home directory. Because a plain `cat -` reads from stdin, the file was read by prefixing a path with `cat ./-`, which revealed the password for the next level.