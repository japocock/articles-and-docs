# Linux

Useful links and documents

Curl Website every second

```sh
while sleep 1; do curl http://www.google.co.uk; done
```

View latest installed updates

```sh
/var/log/yum.log | tail -5
```

Check if port is open or closed. 

```sh
timeout 1 bash -c "echo > /dev/tcp/10.xxxxxx/1433 " > /dev/null 2>&1 && echo "Port 1433 is open" || echo "Port 1433 is closed"
```

