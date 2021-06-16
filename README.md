<h1 align="center"> SmartMirror </h1>

# Materiais utilizados
- Raspberry pi 3

- Fonte de energia

- Teclado e mouse usb

- Cabo hdmi

- Tela ou monitor com entrada hdmi ou adaptada

- Cartão SD Original e de qualidade com memoria maior que 8gb

# Instalando sistema no Raspbery pi 3

Com um computador acesse o site oficial do Raspberry pi (https://www.raspberrypi.org/software/)
Faça o download do software para ser alocado no SDcard.

Enquanto o Download esta sendo concluído formate o SDcard mesmo se o cartão for novo e importante este processo, utilize softwares de formatação um muito bom e o SDformatter 
(https://www.sdcard.org/downloads/formatter/).
Com o SD formatado e a imagem do Raspian baixada (obs: não baixe o Raspian Lite, pois ele não e compatível com a biblioteca) utilize um programa para escrever a imagem no SD.

Alguns exemplos de programas para isso:

- Win32Disk
- balena
- Raspberry pi image

Feito os passos anteriores insira o SD no Raspberry e coloque os outros cabos para começar a utilizar.
Um detalhe muito importante que ao ligar o Raspberry os dois Leds( Vermelho, Verde) precisam acender e piscar, caso isto não aconteça pode ser um erro na instalação da imagem no SD tente novamente com tutoriais na internet a comunidade do Rasp e muito solista para ajudar nesta situação.
Assim que o aparelho ligar vai ser como inicializar um computador a primeira vez selecione pais, linguagem, senha, etc...

<h1 align="center"> Sobre o SmartMirror </h1>

# O que é o SmartMirror?

MagicMirror² é uma plataforma de espelho inteligente modular de código aberto. Com uma lista crescente de módulos instaláveis, o MagicMirror² permite que você converta seu espelho de corredor ou banheiro em seu assistente pessoal.

# Site 
https://magicmirror.builders/

# Instalação

Atualmente a maneira mais segura da instalação do MagicMirror e de forma manual por linhas de código do próprio terminal do Rasp

# Sobre a Biblioteca
- Baixe e instale a versão mais recente do Node.js : 
  (Copie os códigos sem o uso das aspas)

  " curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash - "

  " sudo apt install -y nodejs "
  
 - Clone o repositório e verifique o branch master:

   " git clone https://github.com/MichMich/MagicMirror " 
   
 - Entre no repositório:

   " cd MagicMirror/  "
   
 - Instale o aplicativo: 

   " npm install "
  
  -  Faça uma cópia do arquivo de amostra de configuração: 

    " cp config/config.js.sample config/config.js  "
   
  -  Inicie o aplicativo:

    " npm run start "

# Detalhes Basicos:

Com o rasp intalado e o smart pronto para rodas vamos fazer alguns ajustes basicos como por exemplo a movimentação da tela para ser exibida na 
vertical
Para realizar este processo basta editar o arquivo /boot/confg.txt adicionando
a seguinte linha:
                
                {code}
                
                display_rotate=0
                
                {/code}
                
 OBS: Com o valor 0 (zero) a imagem ficará normal, na horizontal. Com o valor 1 (um) ela será rotacionada (girada) em 90 graus. 
 Com o valor 2 (dois) será girada em 180 graus e com o valor 3 (três) será rotacionada em 270 graus.
 
 
