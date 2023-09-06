<p align="center">
<img src="https://cwmkt.com.br/wp-content/uploads/2023/08/logo-github-cwmkt.svg" alt="DispZap Whats Marketing" width="240" />
<p align="center">Seja bem-vindo ao Guia de atualização do n8n, nodejs e quepasa 🚀</p>
</p>
  
<p align="center">
<img src="https://whatsapp.com/favicon.ico" alt="WhatsAPP-logo" width="32" />
<span>Grupo WhatsaAPP: </span>
<a href="https://link.cwmkt.com.br/grupo-whats" target="_blank">Grupo</a>
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
