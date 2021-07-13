# Anonimous

 Anonimato

## Ficar completamente anônimo com Tor

Ficar anônimo na internet não é apenas um direito seu, mas é fundamental para garantir a sua privacidade online. E para tal, não há nada melhor que instalar o Tor.

## Vamos lá

O Tor está presente nos repositórios da maioria das distribuições. algumas delas são Debian-like, Ubuntu, Linux Mint, Kali e etc, bastaria rodar:

apt install tor privoxy 
apt install apt-transport-https apt-transport-tor

## Pós instalação

Abra o arquivo de configuração do Privoxy em /etc/privoxy/config e procure por:

listen-address localhost:8118

## Em seguida, substitua por:

listen-address 127.0.0.1:8118

## Agora localize a linha que diz:

#forward-socks5 / 127.0.0.1:9050 .

## E remova o # que se encontra no inicio da linha, deixando assim:

forward-socks5 / 127.0.0.1:9050 .

Observação: Repare que no fim da linha existe um ponto (.). Não remova este ponto.

## Agora salve o arquivo.

## Anonimizando as conexões
Sua máquina já está pronta para ser anonimizada, porém, é necessário subir os serviços. Abra seu terminal e execute:

- /etc/init.d/tor start 

- /etc/init.d/privoxy start

## Dica 

Você pode colocar estes serviços para serem iniciados durante o boot com o comando abaixo:

- update-rc.d tor enable 
- update-rc.d privoxy enable

![Proxy](https://static.imasters.com.br/wp-content/uploads/2018/06/06105459/Maan.jpg)

![ATIVANDO SUBSISTEMA DO WINDOWS PARA LINUX](https://www.youtube.com/watch?v=NU5eZbyogW0)

![INSTALANDO LINUX WSL NO WINDOWS](https://www.youtube.com/watch?v=i-l69xigO4k)

![PRIVOXY + TOR ANONIMATO NO WINDOWS](https://www.youtube.com/watch?v=ndQ2zfniHns)



