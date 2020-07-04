# [SSH: Secure Shell](https://en.wikipedia.org/wiki/Secure_Shell)

SSH is a __cryptographic network protocol for operating network services securely over an unsecured network__. Typical applications include remote command-line, login, and remote command execution, but any network service can be secured with SSH, through standard TCP port 22.

This protocol provides a __secure channel__ over an unsecure network by using a __client-server architecture__, connecting an SSH client application with an SSH server. The protocol specification distinguishes between two major versions (SSH-1, SSH2).

The encryption used by SSH is intended to provide confidentiality and integrity of data over an unsecured network, such as the Internet.

## How it works

SSH uses public-key cryptography to authenticate the remote computer and allow it to authenticate the user, if necessary.

The most common one to use SSH es to use automatically generated public-private key pairs to simple encrypt a network connection, and then use password authentication to log on. Another is to use a manually generated public-private key pair to perform the authentication, allowing users or programs to log in without having to specify a password. Public key is placed on all computers that must allow access to the owner of the matching private key, that is kept in secret. SSH only verifies whether the same person offering the public key also owns the matching private key.

## Usage

Typically, used to log into a remote machine and execute commands, but it also supports __tunneling, forwarding TCP ports, and X11 connections__, it can __transfer files__ using the associated __SH File Transfer (SFTP)__ or __Secure Copy (SCP)__ protocols.
