## Алиасы для быстрого подключения

Редактируем

```
sudo nano ~/.ssh/config
```

    Host AliasName
    HostName 1.2.3.4
    User YourUserName
    Port YourSSHPort

Где:

`Host` — алиас для удаленного сервера;

`HostName` — доменное имя или IP адрес удаленного сервера;

`User` — имя пользователя для соединения по SSH;

`Port` — порт SSH на удаленном сервере.

---

## SCP - утилилта для удалённого копирования файлов по протоколу SSH

push to remote server:

    scp file.txt user@remote.host:/some/remote/directory

Copy from remote to local:

    scp <user>@<remote_IP>:/<path_to_file> /home/Download

All files from directory to remote:

    scp -r /home/user/dir/* <user>@<remote_IP>:/home/Download
