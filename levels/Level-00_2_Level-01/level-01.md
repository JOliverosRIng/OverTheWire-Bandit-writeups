# **LEVEL 0 TO LEVEL 1**
<img width="479" height="439" alt="image" src="https://github.com/user-attachments/assets/f3f99c05-8a56-46bd-b4e8-18a7bef18b5f" />

## **English version**
 
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

**NIVEL 0 AL NIVEL 1**
# **Versión en español**

## **Objetivo**
Encontrar la contraseña del siguiente nivel. Está almacenada en un archivo llamado `readme` ubicado en el directorio home.

## **Información Inicial**
- La contraseña está almacenada en un archivo llamado `readme` ubicado en el directorio home.
- **Comandos que podrías necesitar:** `ls`, `cd`, `cat`, `file`, `du`, `find`.

## **Enumeración o Análisis**
1. Listar los archivos y directorios del directorio home para localizar el archivo objetivo.
2. Abrir el archivo, porque ahí es donde está almacenada la contraseña.

## **Enfoque**
1. Identificar el directorio actual.
2. Listar los archivos y directorios dentro del directorio home.
3. Leer el contenido del archivo `readme`.

## **Comandos Utilizados**
- **pwd:** Para conocer la ruta actual.
- **ls:** Para listar los archivos y directorios del directorio home.
- **ls -a:** Para listar todos los archivos y directorios, incluidos los ocultos (opcional aquí, ya que `readme` no está oculto).
- **cd:** Para entrar en un directorio.
- **cat:** Para leer el contenido de un archivo.

## **Solución**
1. Después de iniciar sesión mediante SSH, llegas directamente al directorio home. Ejecuta `pwd` para confirmar la ubicación actual, que es `/home/bandit0`.
2. Ejecuta `ls` para listar los archivos y directorios que hay dentro. El archivo `readme` es visible (no está oculto, por lo que `ls -a` no es necesario).

```bash
ls
```

3. Lee el contenido del archivo con `cat` para revelar la contraseña. La contraseña se oculta aquí de forma intencional, siguiendo buenas prácticas.

```bash
cat readme
```

4. Usa la contraseña obtenida para iniciar sesión en el siguiente nivel mediante SSH en el puerto 2220:

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

## **Explicación**
El archivo `readme` se encuentra directamente en el directorio home y no está oculto, por lo que un simple `ls` lo muestra. Al usar `cat readme` se imprime su contenido, que es la contraseña del siguiente nivel.

Los comandos `file`, `du` y `find` no fueron necesarios para este nivel, pero `find` podría localizar el archivo por su nombre como alternativa: `find ~ -name readme`.

## **Conceptos Aprendidos**
- Comandos básicos de Linux (`pwd`, `ls`, `cd`, `cat`).
- Navegación e inspección de un directorio home.
- Lectura del contenido de archivos desde la línea de comandos.

## **Conclusión**
La contraseña se encontró en un archivo visible (no oculto) llamado `readme`, ubicado directamente en el directorio home, y se leyó utilizando el comando `cat`.

# **Version en français**

# **Version française**
 
## **Objectif**
Trouver le mot de passe du niveau suivant. Il est stocké dans un fichier appelé `readme` situé dans le répertoire home.
 
## **Informations Initiales**
- Le mot de passe est stocké dans un fichier appelé `readme` situé dans le répertoire home.
- **Commandes dont vous pourriez avoir besoin :** `ls`, `cd`, `cat`, `file`, `du`, `find`.
## **Énumération ou Analyse**
1. Lister les fichiers et répertoires du répertoire home pour localiser le fichier cible.
2. Ouvrir le fichier, car c'est là qu'est stocké le mot de passe.
## **Approche**
1. Identifier le répertoire courant.
2. Lister les fichiers et répertoires à l'intérieur du répertoire home.
3. Lire le contenu du fichier `readme`.
## **Commandes Utilisées**
- **pwd :** Pour connaître le chemin actuel.
- **ls :** Pour lister les fichiers et répertoires du répertoire home.
- **ls -a :** Pour lister tous les fichiers et répertoires, y compris les fichiers cachés (facultatif ici, puisque `readme` n'est pas caché).
- **cd :** Pour entrer dans un répertoire.
- **cat :** Pour lire le contenu d'un fichier.
## **Solution**
1. Après vous être connecté via SSH, vous arrivez directement dans le répertoire home. Exécutez `pwd` pour confirmer l'emplacement actuel, qui est `/home/bandit0`.
2. Exécutez `ls` pour lister les fichiers et répertoires présents. Le fichier `readme` est visible (il n'est pas caché, donc `ls -a` n'est pas nécessaire).
```bash
ls
```
 
3. Lisez le contenu du fichier avec `cat` pour révéler le mot de passe. Le mot de passe est masqué ici volontairement, conformément aux bonnes pratiques.
```bash
cat readme
```
 
4. Utilisez le mot de passe obtenu pour vous connecter au niveau suivant via SSH sur le port 2220 :
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
 
## **Explication**
Le fichier `readme` se trouve directement dans le répertoire home et n'est pas caché, donc un simple `ls` le fait apparaître. En utilisant `cat readme`, son contenu s'affiche, à savoir le mot de passe du niveau suivant.
 
Les commandes `file`, `du` et `find` n'étaient pas nécessaires pour ce niveau, mais `find` pourrait localiser le fichier par son nom comme alternative : `find ~ -name readme`.
 
## **Concepts Appris**
- Commandes Linux de base (`pwd`, `ls`, `cd`, `cat`).
- Navigation et inspection d'un répertoire home.
- Lecture du contenu de fichiers depuis la ligne de commande.
## **Conclusion**
Le mot de passe a été trouvé dans un fichier visible (non caché) appelé `readme`, situé directement dans le répertoire home, et lu à l'aide de la commande `cat`.
