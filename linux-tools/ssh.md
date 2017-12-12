## ssh

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

chmod 700 .ssh

cd .ssh && touch authorized_keys config
chmod 600 config authorized_keys

```

```
vi config
Host hostname
   HostName <ip>
   Port <port>
   User <username>
```
