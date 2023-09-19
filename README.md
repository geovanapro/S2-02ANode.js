# S2-02ANode.js
Primeiramente, é preciso realizar a instalação do Nodejs. 
Abra o terminal de comandos na máquina virtual (desta forma: CTRL+ALT+T)
Digite: 
sudo apt install python3-pip
Aguarde, a instalação. E a seguir, digite: 
pip3 install --user nodeenv 
Aguarde a instalação, e para verifica-la digite no terminal: 
source ~/.profile 
Ou reinicie a máquina (para ativar o comando "nodeenv --version")
E logo a seguir: 
nodeenv --version
Seguidamente, é necessário instalar o NodeEnv. Continuando no terminal de comandos, digite: 
nodeenv nodejs-env 
Obs:o nodeenv é o comando, e nodejs-env é o nome da pasta (diretório) que irá ser
instalado o NodeJs.
Aguarde a instalação (para ativar esta versão do NodeJs)
Digite: 
source ./nodejs-env/bin/activate
O indicador de prompt irá mudar, sinalizando que você está com o ambiente ativo.
Para testar, digite: 
node --version
Obs: Sempre que ativar por este modo, NÃO instale nenhum pacote pelo apt install porque poderá ocorrer problemas.
Desative desta forma(no prompt irá constar que não está mais ativo): 
deactivate_node
Logo depois, iniciaremos a instalação do Node-Red e para isso, digite: 
npm install -g node-red
Espere a instalação do Node-Red.
Para ativar o Node-Red, digite no terminal: 
node-red
No computador HOST digite: "http://localhost:1880", para testar a instalação do NodeJs com NodeEnv.

Os proximos passos serão para criar uma pasta "src" dentro de "Documentos", digite:
cd Documentos/
mkdir src
Com a pasta criada, acesse da seguinte forma a pasta src:
cd src/
Após isso, digite: 
source nodejs-env/bin/activate
Entre no nano index.js, e edite o html colocando o seguinte código:
Para entrar no nano:
sudo nano index.js
Logo ápos, edite colocando o código a seguir:

var http = require('http');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World');
}).listen(5000);

ATENÇÃO: Substitua "Hello World", para o que é desejado escrever dentro do html. E substitua 5000, pela porta desejada. E salve (CTRL+O) e para sair (CTRL+X)
Por fim, para acessar no node na web. Digite:
node index.js

Entre no firefox, digite na aba de pesquisa: 

localhost:5000 

Sendo "5000", a porta de acesso escolhida.
Para fechar, entre no terminal e digite: CTRL+C

E este foi o tutorial, espero que tenham compreendido o processo!!!
