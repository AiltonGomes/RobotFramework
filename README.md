# Robot Framework
Projeto de automação em Robot Framework e Selenium WebDriver

Configuração MACÇ

-- 1 - Instalando o Python. 1.1 Baixe o Python no link: https://www.python.org/downloads/

  1.2 Instale via executável o executavel baixado. OBS: durante a instalação um dos passos é selecionar para que as variáveis sejam adicionadas ao PATH do mac.
  Para conferir se deu certo, no prompt de comando (cmd) execute:
  python -version

-- 2 - Instale o pip. 

  2.1 No bash execute o comando abaixo: sudo easy_install pip
  Verifique se o pip foi realmente instalado:
  pip --version

-- 3 - Instale o robot framework. 

  3.1 No bash execute o comando abaixo: pip install robotframework

-- 4 - Instale o robot framework 

  4.1 No bash execute o comando abaixo: pip install robotframework-Selenium2Library

-- 5 - Instale os drivers navegador.
  
  5.1 Para instalar os drivers, precisamos instalar o brew. No bash execute o comando abaixo: /usr/bin/ruby -e "$(curl -fsSL    https://raw.githubusercontent.com/Homebrew/install/master/install)"

  5.2 Após instalar a brew o chromedriver foi migrado do homebrew/core para homebrew/cask.
  Agora pode instalar com o comando abaixo:
  brew cask install chromedriver

!!! Pronto instalação completa

Configuração Windowns:

-- 1 - Instalando o Python. 

1.1 Baixe o Python no link: https://www.python.org/downloads/

  1.2. Instale via executável o executavel baixado. OBS: durante a instalação um dos passos é selecionar para que as variáveis sejam adicionadas ao PATH do windowns.
  Para conferir se deu certo, no prompt de comando (cmd) execute:
  python --version
  pip -- version

-- 2 - Intalando o Robot Framework. 

  2.1 No prompt de comando (cmd) execute e aguarde a instalação: pip install robotframework Para conferir se deu certo, no prompt de comando (cmd) execute: robot --version

  !!! Pronto instalação completa
  -- Sempre que rodar o projeto tem que ser com o comando descrito abaixo, assim ele irá criar os arquivos de outputs dentro de uma pasta log organizando melhor os       arquivos.

  robot -d ./logs ARQUIVO_DO_TESTE.robot
  -- Rodando todos os testes de uma pasta

  robot -d .logs tests
  -- Rodando testes com tags

  robot -d ./logs -i TAG ARQUIVO_DO_TESTE.robot
  -- Criando CssSelector - Para isso vc precisa passar o elemento a propriedade e o valor, exemplo abaixo.

  <input type='checkbox' value='iron-man'>

  No exemplo acima o input é o elemento, value é a propriedade e iron-man o valor, então o CssSelector ficaria assim:

  css:input[value=iron-man]

  Abaixo esta um exemplo de como criar uma pesquisa no console do navegador e verificar se ele encontra o elemento correto.

  document.querySelector("input[value='iron-man']")
  -- Criando Xpath - Para isso vc precisa passar o elemento pai e o filho, exemplo abaixo.

  //*[@id='checkboxes']/input[7]

  No exemplo acima o id checkboxes é o elemento pai, o input é um dos filhos e 7 é o filho que queremos selecionar, para validade de que esta criado corretamente fazemos isso no Elements dando o comando ctrl+f e na pesquisa criamos.
