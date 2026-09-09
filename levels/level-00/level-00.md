# **LEVEL 0**
<img width="326" height="294" alt="image" src="https://github.com/user-attachments/assets/169e6d9d-ce92-4c19-8716-387d23bda147" />

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
