# **LEVEL 0 TO LEVEL 1**
# **English version**
 
## **Objective**
Find the password for the next level. It is stored in a file called `readme` located in the home directory.
 
## **Initial Information**
- The password is stored in a file called `readme` located in the home directory.
- **Commands you may need:** `ls`, `cd`, `cat`, `file`, `du`, `find`.
## **Enumeration or Analysis**
1. List the files and directories in the home directory to locate the target file.
2. Open the file, because that is where the password is stored.
## **Approach**
1. Identify your current directory.
2. List the files and directories inside the home directory.
3. Read the content of the `readme` file.
## **Commands Used**
- **pwd:** To know the current path.
- **ls:** To list the files and directories in the home directory.
- **ls -a:** To list all files and directories, including hidden ones (optional here, since `readme` is not hidden).
- **cd:** To move into a directory.
- **cat:** To read the content of a file.
## **Solution**
1. After logging in through SSH, you land directly in the home directory. Run `pwd` to confirm the current location, which is `/home/bandit0`.
2. Run `ls` to list the files and directories inside. The `readme` file is visible (it is not hidden, so `ls -a` is not required).
```bash
ls
```
 
3. Read the content of the file with `cat` to reveal the password. The password is hidden here on purpose, following good practice.
```bash
cat readme
```
 
4. Use the retrieved password to log into the next level over SSH on port 2220:
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
 
## **Explanation**
The `readme` file sits directly in the home directory and is not hidden, so a plain `ls` reveals it. Using `cat readme` prints its content, which is the password for the next level.
 
The commands `file`, `du`, and `find` were not needed for this level, but `find` could locate the file by name as an alternative: `find ~ -name readme`.
 
## **Concepts Learned**
- Basic Linux commands (`pwd`, `ls`, `cd`, `cat`).
- Navigating and inspecting a home directory.
- Reading file contents from the command line.
## **Conclusion**
The password was found in a visible (non-hidden) file named `readme`, located directly in the home directory, and read using the `cat` command.

# **Versión en español**

**Objetivo**
**Información inicial**
**Enumeración o Análisis**
**Estrategia**
**Comandos utilizados**
**Solución**
**Explicación**
**Conceptos aprendidos**
**Conclusión**

# **Version en français**

**Objectif**
**Informations initiales**
**Énumération ou Analyse**
**Approche**
**Commandes utilisées**
**Solution**
**Explication**
**Concepts appris**
**Conclusion**