# **LEVEL 02 TO LEVEL 03**

## **Objective**

Find the password for the next level. The password is stored in a file called `--spaces in this filename--`, located in the home directory.

This level requires the use of basic Linux commands, particularly `ls`, `cd`, and `cat`.

## **Initial Information**

1. The password for the next level is stored in a file called `--spaces in this filename--`.
2. The file is located in the home directory.
3. The filename contains spaces and begins with two hyphens (`--`), which can cause problems when using standard command-line syntax.

## **Enumeration or Analysis**

The first step was to list the contents of the home directory in order to identify the target file.

```bash
ls
```

The command showed the following file:

```text
--spaces in this filename--
```

The target file contains spaces in its name and starts with `--`. These characteristics can cause the shell to interpret parts of the filename incorrectly when the file is accessed directly.

The home directory can also be verified with:

```bash
pwd
```

The current directory is:

```text
/home/bandit2
```

To access the file correctly, the filename was enclosed in single quotation marks:

```bash
cat '--spaces in this filename--'
```

Alternatively, the absolute path can be used:

```bash
cat /home/bandit2/'--spaces in this filename--'
```

## **Approach**

The approach was based on simple file enumeration and identification of the target file.

1. Identify the current working directory using `pwd`.
2. List the files in the home directory using `ls`.
3. Identify the file containing spaces and special characters in its name.
4. Use `cat` to read the file.
5. Enclose the filename in single quotation marks to ensure that the shell interprets the complete filename as a single argument.

## **Commands Used**

### Check the current directory

```bash
pwd
```

### List the contents of the directory

```bash
ls
```

### Read the file

```bash
cat '--spaces in this filename--'
```

or:

```bash
cat /home/bandit2/'--spaces in this filename--'
```

## **Solution**

The password was obtained by reading the contents of the file with:

```bash
cat '--spaces in this filename--'
```

The command successfully accessed the file and displayed the password for the next level.

## **Explanation**

The main challenge in this level is not the `cat` command itself, but correctly handling the filename.

The filename contains spaces:

```text
--spaces in this filename--
```

In the Linux shell, spaces normally separate different arguments. Therefore, if the filename is entered without being properly handled, the shell may interpret it as several separate arguments.

For example:

```bash
cat --spaces in this filename--
```

could be interpreted as multiple arguments rather than as one filename.

By enclosing the filename in single quotation marks:

```bash
cat '--spaces in this filename--'
```

the entire string is treated as a single argument.

The quotation marks are interpreted by the shell and are not considered part of the actual filename.

This technique is useful when working with filenames that contain spaces or other characters that have a special meaning to the shell.

## **Concepts Learned**

### 1. Linux file enumeration

The `ls` command can be used to inspect the contents of a directory and identify files that may be relevant to an investigation.

### 2. Handling spaces in filenames

Filenames containing spaces should be enclosed in quotes or otherwise escaped when used as command-line arguments.

For example:

```bash
cat 'file with spaces.txt'
```

### 3. Shell interpretation

The shell interprets spaces as argument separators. Quoting a string prevents the shell from splitting it into multiple arguments.

### 4. Absolute and relative paths

The file can be accessed using either its relative name:

```bash
cat '--spaces in this filename--'
```

or its absolute path:

```bash
cat /home/bandit2/'--spaces in this filename--'
```

Understanding paths is essential when navigating and analyzing Linux systems.

## **Conclusion**

This level demonstrated how filenames containing spaces and special characters can affect command-line operations in Linux.

The challenge was solved by enumerating the home directory, identifying the target file, and using quotation marks to ensure that the complete filename was interpreted as a single argument.

Although this is a simple technique, correctly handling filenames is an important skill when performing Linux administration, system analysis, and cybersecurity investigations.