# Red

```
     XXX          XXXXXXXX
   XXX XXXX   XXXXX      XX
  X       XXXX          X
 XX                     XX
 X       Internet        X
 XXX                     X
    XXXXXXXX     XXXXXXXX
           XXXXXX
             +
             |
             |
             |
             |
             v
+------------+------------+
|         Proxmox         |
|          Cloud          |
|                         |
|         hxx.pw          |
|                         |
+-----+-------------+-----+
      |             |
      |             |
      |             |
      v             v
 +----+----+   +----+----+
 |m1.hxx.pw|   |m2.hxx.pw|
 +---------+   +---------+
```

## Accesos

### SSH
>m1.hxx.pw:10022 --> DNAT (hxx.pw) 10.10.10.1 --> (m1.hxx.pw) 10.10.10.100:22
>m1.hxx.pw:10122 --> DNAT (hxx.pw) 10.10.10.1 --> (m2.hxx.pw) 10.10.10.101:22

### HTTP/S
> m1.hxx.pw --> NGINX PROXY hxx.pw --> (m1.hxx.pw) 10.10.10.100:[80|443]
> m2.hxx.pw --> NGINX PROXY hxx.pw --> (m2.hxx.pw) 10.10.10.101:[80|443]

