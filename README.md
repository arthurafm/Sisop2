# Sistemas Operacionais II (PT-BR)

Esse repositório representa o trabalho da matéria de Sistemas Operacionais II durante o período 2024/1 da UFRGS, sob a tutela do Professor Alberto Schaeffer.

### Descrição geral do trabalho

Este projeto consiste na implementação de um serviço semelhante ao Dropbox, para permitir o compartilhamento e a sincronização automática de arquivos entre diferentes dispositivos de um mesmo usuário. A implementação foi feita com a API TCP sockets do Unix e em C++.

### Funcionalidades

A aplicação possui um servidor e um cliente. O servidor é capaz de gerenciar arquivos de diversos usuários remotos. Já o cliente corresponde à parte da aplicação presente na máquina dos usuários, que permite ao usuário acessar remotamente seus arquivos mantidos pelo servidor.

- O servidor é capaz de tratar requisições simultâneas de vários usuários.
- Um usuário pode utilizar o serviço através de até dois dispositivos distintos simultaneamente.
- As estruturas de armazenamento de dados no servidor devem ser mantidas em um estado consistente e protegidas de acessos concorrentes.
- Cada vez que um usuário modifica um arquivo contido no diretório '*sync_dir*' em seu dispositivo, o arquivo é atualizado no servidor e no diretório '*sync_dir*' dos demais dispositivos daquele usuário.
- Diretórios e arquivos de usuários são restabelecidos quando o servidor é reiniciado.
- É possível rodar o servidor em replicação passiva, com um servidor primário e diversos backups.
- Para o processo de escolha de servidor primário em caso de falha, é utilizado o algoritmo de eleição *bully*.

# Operational Systems II (EN-US)

This repository represents the work for the Operating Systems II course during the 2024/1 term at UFRGS, under the guidance of Professor Alberto Schaeffer.

### General Project Description

This project involves implementing a service similar to Dropbox, enabling the sharing and automatic synchronization of files between different devices of the same user. The implementation was done using Unix TCP sockets API and C++.

### Features

The application includes a server and a client. The server is capable of managing files from multiple remote users, while the client is the part of the application on the user's machine that allows remote access to their files maintained by the server.

- The server can handle simultaneous requests from multiple users.
- A user can use the service from up to two different devices simultaneously.
- The data storage structures on the server must be kept in a consistent state and protected from concurrent access.
- Whenever a user modifies a file in the '*sync_dir*' directory on their device, the file is updated on the server and in the '*sync_dir*' directory of the user's other devices.
- User directories and files are restored when the server is restarted.
- The server can run in passive replication mode, with a primary server and multiple backups.
- The *bully* election algorithm is used for selecting the primary server in case of failure.
