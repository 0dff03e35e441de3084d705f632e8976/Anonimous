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

Subsistema Windows para Linux é um módulo do sistema operacional Windows 10, que visa a disponibilizar um ambiente Linux compatível no sistema da Microsoft, de forma que se possam executar programas (baseados em texto) nativos dos sistemas GNU/Linux dentro do próprio Windows sem a necessidade de emuladores ou do uso de máquinas virtuais. [1]

![INSTALANDO LINUX WSL NO WINDOWS](https://www.youtube.com/watch?v=i-l69xigO4k)

Neste exemplo vou falar do Ubuntu 18.04 LTS, clique em Obter. Você será redirecionado para Loja da Microsoft, clique em Obter novamente, um aviso irar aparecer informando para entrar com sua conta Microsoft, se já estiver logado com sua conta Microsoft prossiga ou se não quiser entrar com sua conta Microsoft clique em Não obrigado.

![PRIVOXY + TOR ANONIMATO NO WINDOWS]
(https://www.youtube.com/watch?v=ndQ2zfniHns)

Para melhorar a privacidade da sua sessão VPN, e por ser legal, o túnel lhe dão a opção de filtrar seu tráfego HTTP(s) através de Privoxy e Tor.

O que é que eles são?
Privoxy é um proxy web que foi projetado para esfregar páginas da Web para coisas ruins, como rastrear bugs, scripts de análise e outras coisas que geralmente são consideradas violações de privacidade. Ele também faz alguns anúncios básicos e outros bloqueios de aborrecimento. Ele não armazena cache ou armazena qualquer conteúdo que passe por ele.

Gostamos especialmente do Privoxy em dispositivos como o iPhone, onde não há uma maneira oficial de bloquear o conteúdo da Web. Você pode ler mais sobre Privoxy em http://www.privoxy.org/.

Tor é uma rede de anonimato. Ou seja, o Tor permite que alguém se conecte com coisas (geralmente sites) de uma maneira que torna muito difícil para qualquer pessoa encontrar sua localização real. É criptografado como uma VPN, mas é muito lento devido ao caminho deliberadamente complicado que seus dados levam. Para uma explicação muito melhor do que o Tor faz, leia a visão geral do Projeto Tor.

