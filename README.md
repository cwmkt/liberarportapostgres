<p align="center">
	<img src="https://www.chatwoot.com/docs/img/logo.png" alt="Chatwoot-logo" width="100" />	
	<p align="center">O Chatwoot oferece todas as ferramentas para gerenciar conversas, construir relacionamentos e encantar seus clientes em um só lugar.</p>
</p>

<p align="left">
	<img src="https://whatsapp.com/favicon.ico" alt="WhatsAPP-logo" width="32" />
	<span>Grupo WhatsaAPP: </span>
	<a href="https://chat.whatsapp.com/CLKge3hmHmmBcIL04mBzmT" target="_blank">Grupo</a>
</p>

<hr />
<hr />

sudo nano /etc/postgresql/14/main/pg_hba.conf
</p>
Linha 97
</p>
host    all             all             127.0.0.1/32            scram-sha-256
</p>
Alterar para
</p>
host    all             all             0.0.0.0/0               md5
</p>
depois
</p>
sudo nano /etc/postgresql/14/main/postgresql.conf
</p>
Linha 60
</p>
#listen_addresses = 'localhost' # what IP address(es) to listen on;

Alterar para
</p>
listen_addresses = '*'		# what IP address(es) to listen on;
</p>
sudo systemctl restart postgresql
</p>
<hr />
<hr />
