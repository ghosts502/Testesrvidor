# Testesrvidor ainda esta falta testar a conexão entre as amquinas e o servidor principal e fazer o ping de dados 
sudo apt install wireguard

sudo mv maquina1.conf /etc/wireguard/wg0.conf

sudo wg-quick up wg0

ping 10.8.0.x

no terminal vscode 

caso for linux essa é uma das configurações 


✔️ Passo 1 — Instalar o WireGuard no Windows

Baixe o instalador oficial:

👉 WireGuard para Windows
https://www.wireguard.com/install/

Depois instale normalmente como qualquer programa.

✔️ Passo 2 — Abrir o programa WireGuard

Após instalar:

Clique no ícone do WireGuard na área de trabalho ou menu iniciar.

Vai abrir a janela principal com:

➕ Add Tunnel

✔️ Passo 3 — Importar o arquivo maquina1.conf

Clique em:

Add Tunnel → Import tunnel(s) from file


Selecione o arquivo:

maquina1.conf


Esse arquivo foi criado pelo script add_client.sh.

✔️ Passo 4 — Ativar a conexão

Depois de importar, vai aparecer o túnel:

maquina1


Clique em:

Activate


Se tudo funcionar certo, você verá:

Handshake OK

Bytes enviados/recebidos aumentando

IP interno da VPN: 10.8.0.x

❗ IMPORTANTE

No Windows, o WireGuard usa driver próprio, e não precisa:

❌ sudo
❌ apt install
❌ comandos wg-quick
❌ mover configs para /etc/wireguard

Isso existe somente no Linux.

🔥 Quer testar a comunicação entre as máquinas?

Depois de conectar no Windows:

Abra o Prompt de Comando e rode:

ping 10.8.0.1


(servidor)

Ou outra máquina cliente, ex:

ping 10.8.0.25
