<p align="center">
<img src="https://cwmkt.com.br/wp-content/uploads/2024/04/logo_github.png" width="240" />
<p align="center">Seja bem-vindo ao Guia de completo de como liberar banco de dados  🚀</p>
</p>
  
<p align="center"> 
<a href="https://hubconnect.top" target="_blank">👉 Participe da Comunidade HubConnect 👈</a>
</p>

<hr />
<hr />

## Liberando Postgres para acesso externo

Execute comando abaixo

```bash
sudo nano /etc/postgresql/14/main/pg_hba.conf
```

Linha 97

host    all             all             127.0.0.1/32            scram-sha-256

Alterar para

```bash
host    all             all             0.0.0.0/0               md5
```


depois

Linha 60

```bash
sudo nano /etc/postgresql/14/main/postgresql.conf
```

#listen_addresses = 'localhost' # what IP address(es) to listen on;

Alterar para

```bash
listen_addresses = '*'		# what IP address(es) to listen on;
```

```bash
sudo systemctl restart postgresql
```
