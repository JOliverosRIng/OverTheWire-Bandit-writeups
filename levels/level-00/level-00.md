# **LEVEL 0**
<img width="326" height="294" alt="image" src="https://github.com/user-attachments/assets/169e6d9d-ce92-4c19-8716-387d23bda147" />

# **English version**

## **Objective**

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

## **Initial Information**
- **Commands you may need to solve this level:** shh
- **Host:** bandit.labs.overthewire.org
- **Port:** 2220
- **username:** bandit0
- **password:** bandit0
  
## **Enumeration or Analysis**
**SSH** stands for Secure Shell. It is a network protocol that allows you to securely access and manage a remote computer or server over a network.

## **What does “Secure Shell” mean?**
- **Secure:** The communication is protected through encryption.
- **Shell** It provides a command-line interface through which you can interact with the remote system.

In simple terms, SSH allows you to connect to another computer remotely and interact with its operating system through a terminal.

## **What happens when you use SSH?**
1. Your computer connects to the remote server.
2. The server authenticates your identity.
3. An encrypted connection is established.
4. You can interact with the remote system through a command-line interface.

## **What is SSH used for?**

SSH is commonly used to:

- Remotely administer servers.
- Execute commands on remote Linux systems.
- Transfer files securely.
- Manage cloud infrastructure.
- Access virtual machines and remote systems.
- Perform system administration tasks.
- Security provided by SSH.

## **Approach**

First, I will use SSH to establish a secure connection to the Bandit server using the host, port, and credentials provided.

After successfully authenticating, I will verify that I have access to the remote system and inspect the available resources to understand how to proceed to the level 1.

## **Commands Used**

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## **Solution**

First, open the command-line terminal. Then, establish an SSH connection to the Bandit server using the following command:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

The server will ask you to verify its authenticity. If this is your first time connecting to the server, you will be prompted to confirm whether you want to continue with the connection. Type yes and press Enter.

The server will then ask for the password. Enter the password provided in the challenge:

```bash
bandit0
```

Once the password is accepted, the SSH connection is established and you are logged in as the bandit0 user.

## **Explanation**

The ssh command is used to establish a secure connection to a remote server.

The command used in this level is:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Each part of the command has a specific purpose:

- **ssh →** starts an SSH connection.
- **bandit0 →** specifies the username used to authenticate to the remote server.
- **@ →** separates the username from the server address.
- **bandit.labs.overthewire.org →** specifies the hostname of the remote server.
- **-p 2220 →** specifies the port where the SSH service is running.

After executing the command, the server asks the user to verify its authenticity. This is part of the SSH process used to establish trust between the client and the remote server.

Once the connection is accepted, the server requests the password associated with the bandit0 account. After successful authentication, an SSH session is established and the user gains access to the remote system.

## **Concepts Learned**

- **SSH (Secure Shell):** Protocol used to securely connect to a remote computer or server.
- **Remote Access:** Connecting to and interacting with a computer located on another system or network.
- **SSH Authentication:** The process of verifying the user's identity using credentials such as a username and password.
- **Hostnames:** Human-readable names used to identify remote servers on a network.
- **Network Ports:** Logical endpoints used by network services to receive connections. In this level, SSH is running on port 2220 instead of the default port 22.
- **Command-Line Interface (CLI):** A text-based interface used to interact with a computer by entering commands.
- **SSH Host Key Verification:** The mechanism SSH uses to verify the identity of a remote server when connecting to it for the first time.

## **Conclusion**
The SSH connection was successfully established, and access to the Bandit server was obtained using the bandit0 account.

## **Next Level**
[Level 00 to Level 01](levels/level-00/level-00.md)


# **Versión en español**

## **Objetivo**
 
El objetivo de este nivel es que inicies sesión en el juego mediante SSH. El host al que necesitas conectarte es bandit.labs.overthewire.org, en el puerto 2220. El nombre de usuario es bandit0 y la contraseña es bandit0. Una vez que hayas iniciado sesión, dirígete a la página del Nivel 1 para descubrir cómo superarlo.
 
## **Información Inicial**
- **Comandos que podrías necesitar para resolver este nivel:** ssh
- **Host:** bandit.labs.overthewire.org
- **Puerto:** 2220
- **usuario:** bandit0
- **contraseña:** bandit0
## **Enumeración o Análisis**
**SSH** significa Secure Shell (Intérprete de Comandos Seguro). Es un protocolo de red que te permite acceder y administrar de forma segura una computadora o servidor remoto a través de una red.
 
## **¿Qué significa "Secure Shell"?**
- **Secure (Seguro):** La comunicación está protegida mediante cifrado.
- **Shell (Intérprete de comandos):** Proporciona una interfaz de línea de comandos a través de la cual puedes interactuar con el sistema remoto.
En términos simples, SSH te permite conectarte a otra computadora de forma remota e interactuar con su sistema operativo a través de una terminal.
 
## **¿Qué ocurre cuando usas SSH?**
1. Tu computadora se conecta al servidor remoto.
2. El servidor autentica tu identidad.
3. Se establece una conexión cifrada.
4. Puedes interactuar con el sistema remoto a través de una interfaz de línea de comandos.
## **¿Para qué se usa SSH?**
 
SSH se utiliza comúnmente para:
 
- Administrar servidores de forma remota.
- Ejecutar comandos en sistemas Linux remotos.
- Transferir archivos de forma segura.
- Gestionar infraestructura en la nube.
- Acceder a máquinas virtuales y sistemas remotos.
- Realizar tareas de administración de sistemas.
- Seguridad proporcionada por SSH.
## **Enfoque**
 
Primero, usaré SSH para establecer una conexión segura con el servidor Bandit utilizando el host, el puerto y las credenciales proporcionadas.
 
Después de autenticarme correctamente, verificaré que tengo acceso al sistema remoto e inspeccionaré los recursos disponibles para entender cómo avanzar hacia el Nivel 1.
 
## **Comandos Utilizados**
 
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
 
## **Solución**
 
Primero, abre la terminal de línea de comandos. Luego, establece una conexión SSH con el servidor Bandit utilizando el siguiente comando:
 
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
 
El servidor te pedirá que verifiques su autenticidad. Si es la primera vez que te conectas al servidor, se te solicitará confirmar si deseas continuar con la conexión. Escribe yes y presiona Enter.
 
A continuación, el servidor te pedirá la contraseña. Ingresa la contraseña proporcionada en el desafío:
 
```bash
bandit0
```
 
Una vez que se acepta la contraseña, se establece la conexión SSH y quedas conectado como el usuario bandit0.
 
## **Explicación**
 
El comando ssh se utiliza para establecer una conexión segura con un servidor remoto.
 
El comando usado en este nivel es:
 
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
 
Cada parte del comando tiene un propósito específico:
 
- **ssh →** inicia una conexión SSH.
- **bandit0 →** especifica el nombre de usuario utilizado para autenticarse en el servidor remoto.
- **@ →** separa el nombre de usuario de la dirección del servidor.
- **bandit.labs.overthewire.org →** especifica el nombre de host del servidor remoto.
- **-p 2220 →** especifica el puerto en el que se ejecuta el servicio SSH.
Después de ejecutar el comando, el servidor le pide al usuario que verifique su autenticidad. Esto forma parte del proceso SSH utilizado para establecer confianza entre el cliente y el servidor remoto.
 
Una vez que se acepta la conexión, el servidor solicita la contraseña asociada a la cuenta bandit0. Tras una autenticación exitosa, se establece una sesión SSH y el usuario obtiene acceso al sistema remoto.
 
## **Conceptos Aprendidos**
 
- **SSH (Secure Shell):** Protocolo utilizado para conectarse de forma segura a una computadora o servidor remoto.
- **Acceso Remoto:** Conectarse e interactuar con una computadora ubicada en otro sistema o red.
- **Autenticación SSH:** El proceso de verificar la identidad del usuario mediante credenciales como un nombre de usuario y una contraseña.
- **Nombres de Host (Hostnames):** Nombres legibles por humanos utilizados para identificar servidores remotos en una red.
- **Puertos de Red:** Puntos finales lógicos utilizados por los servicios de red para recibir conexiones. En este nivel, SSH se ejecuta en el puerto 2220 en lugar del puerto predeterminado 22.
- **Interfaz de Línea de Comandos (CLI):** Una interfaz basada en texto utilizada para interactuar con una computadora mediante la introducción de comandos.
- **Verificación de la Clave del Host SSH (SSH Host Key Verification):** El mecanismo que SSH utiliza para verificar la identidad de un servidor remoto al conectarse a él por primera vez.
## **Conclusión**
La conexión SSH se estableció correctamente y se obtuvo acceso al servidor Bandit utilizando la cuenta bandit0.
 
## **Siguiente Nivel**
[Nivel 00 al Nivel 01](levels/level-00/level-00.md)

# **Version en français**

## **Objectif**

L'objectif de ce niveau est de vous connecter au jeu à l'aide de SSH. L'hôte auquel vous devez vous connecter est bandit.labs.overthewire.org, sur le port 2220. Le nom d'utilisateur est bandit0 et le mot de passe est bandit0. Une fois connecté, rendez-vous sur la page du Niveau 1 pour découvrir comment le réussir.

## **Informations Initiales**
- **Commandes dont vous pourriez avoir besoin pour résoudre ce niveau :** ssh
- **Hôte :** bandit.labs.overthewire.org
- **Port :** 2220
- **utilisateur :** bandit0
- **mot de passe :** bandit0

## **Énumération ou Analyse**
**SSH** signifie Secure Shell (interpréteur de commandes sécurisé). Il s'agit d'un protocole réseau qui vous permet d'accéder à un ordinateur ou un serveur distant et de le gérer de manière sécurisée à travers un réseau.

## **Que signifie « Secure Shell » ?**
- **Secure (Sécurisé) :** La communication est protégée par un chiffrement.
- **Shell (Interpréteur de commandes) :** Il fournit une interface en ligne de commande grâce à laquelle vous pouvez interagir avec le système distant.

En termes simples, SSH vous permet de vous connecter à un autre ordinateur à distance et d'interagir avec son système d'exploitation via un terminal.

## **Que se passe-t-il lorsque vous utilisez SSH ?**
1. Votre ordinateur se connecte au serveur distant.
2. Le serveur authentifie votre identité.
3. Une connexion chiffrée est établie.
4. Vous pouvez interagir avec le système distant via une interface en ligne de commande.

## **À quoi sert SSH ?**

SSH est couramment utilisé pour :

- Administrer des serveurs à distance.
- Exécuter des commandes sur des systèmes Linux distants.
- Transférer des fichiers de manière sécurisée.
- Gérer une infrastructure cloud.
- Accéder à des machines virtuelles et à des systèmes distants.
- Effectuer des tâches d'administration système.
- Sécurité fournie par SSH.

## **Approche**

Tout d'abord, j'utiliserai SSH pour établir une connexion sécurisée avec le serveur Bandit en utilisant l'hôte, le port et les identifiants fournis.

Après m'être authentifié avec succès, je vérifierai que j'ai accès au système distant et j'inspecterai les ressources disponibles afin de comprendre comment progresser vers le Niveau 1.

## **Commandes Utilisées**

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## **Solution**

Tout d'abord, ouvrez le terminal en ligne de commande. Ensuite, établissez une connexion SSH avec le serveur Bandit à l'aide de la commande suivante :

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Le serveur vous demandera de vérifier son authenticité. S'il s'agit de votre première connexion au serveur, il vous sera demandé de confirmer si vous souhaitez poursuivre la connexion. Tapez yes et appuyez sur Entrée.

Le serveur vous demandera ensuite le mot de passe. Saisissez le mot de passe fourni dans le défi :

```bash
bandit0
```

Une fois le mot de passe accepté, la connexion SSH est établie et vous êtes connecté en tant qu'utilisateur bandit0.

## **Explication**

La commande ssh est utilisée pour établir une connexion sécurisée avec un serveur distant.

La commande utilisée dans ce niveau est :

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Chaque partie de la commande a un rôle précis :

- **ssh →** démarre une connexion SSH.
- **bandit0 →** spécifie le nom d'utilisateur utilisé pour s'authentifier auprès du serveur distant.
- **@ →** sépare le nom d'utilisateur de l'adresse du serveur.
- **bandit.labs.overthewire.org →** spécifie le nom d'hôte du serveur distant.
- **-p 2220 →** spécifie le port sur lequel le service SSH s'exécute.

Après l'exécution de la commande, le serveur demande à l'utilisateur de vérifier son authenticité. Cela fait partie du processus SSH utilisé pour établir une relation de confiance entre le client et le serveur distant.

Une fois la connexion acceptée, le serveur demande le mot de passe associé au compte bandit0. Après une authentification réussie, une session SSH est établie et l'utilisateur obtient l'accès au système distant.

## **Concepts Appris**

- **SSH (Secure Shell) :** Protocole utilisé pour se connecter de manière sécurisée à un ordinateur ou un serveur distant.
- **Accès à Distance :** Se connecter à un ordinateur situé sur un autre système ou réseau et interagir avec lui.
- **Authentification SSH :** Le processus de vérification de l'identité de l'utilisateur à l'aide d'identifiants tels qu'un nom d'utilisateur et un mot de passe.
- **Noms d'Hôte (Hostnames) :** Noms lisibles par l'humain utilisés pour identifier les serveurs distants sur un réseau.
- **Ports Réseau :** Points de terminaison logiques utilisés par les services réseau pour recevoir des connexions. Dans ce niveau, SSH s'exécute sur le port 2220 au lieu du port par défaut 22.
- **Interface en Ligne de Commande (CLI) :** Une interface textuelle utilisée pour interagir avec un ordinateur en saisissant des commandes.
- **Vérification de la Clé d'Hôte SSH (SSH Host Key Verification) :** Le mécanisme utilisé par SSH pour vérifier l'identité d'un serveur distant lors de la première connexion.

## **Conclusion**
La connexion SSH a été établie avec succès et l'accès au serveur Bandit a été obtenu à l'aide du compte bandit0.

## **Niveau Suivant**
[Niveau 00 au Niveau 01](levels/Level-00_2_Level-01/level-01.md)
