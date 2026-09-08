# **English version**

**Objective**

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

**Initial Information**
- **Commands you may need to solve this level:** shh
- **Host:** bandit.labs.overthewire.org
- **Port:** 2220
- **username:** bandit0
- **password:** bandit0
  
**Enumeration or Analysis**
**SSH** stands for Secure Shell. It is a network protocol that allows you to securely access and manage a remote computer or server over a network.

**What does “Secure Shell” mean?**
- **Secure:** The communication is protected through encryption.
- **Shell** It provides a command-line interface through which you can interact with the remote system.

In simple terms, SSH allows you to connect to another computer remotely and interact with its operating system through a terminal.

**What happens when you use SSH?**
1. Your computer connects to the remote server.
2. The server authenticates your identity.
3. An encrypted connection is established.
4. You can interact with the remote system through a command-line interface.

**What is SSH used for?**

SSH is commonly used to:

- Remotely administer servers.
- Execute commands on remote Linux systems.
- Transfer files securely.
- Manage cloud infrastructure.
- Access virtual machines and remote systems.
- Perform system administration tasks.
- Security provided by SSH.

**Approach**

First, I will use SSH to establish a secure connection to the Bandit server using the host, port, and credentials provided.

After successfully authenticating, I will verify that I have access to the remote system and inspect the available resources to understand how to proceed to the level 1.

**Commands Used**

ssh bandit0@bandit.labs.overthewire.org -p 2220

**Solution**


**Explanation**
**Concepts Learned**
**Conclusion**

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