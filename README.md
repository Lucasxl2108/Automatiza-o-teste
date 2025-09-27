Automação de Login e Download - Portal AVA Unieuro
Este projeto contém um script em Python que utiliza a biblioteca Selenium para automatizar todo o processo de login no portal AVA do Grupo Ceuma, navegar até a plataforma da Unieuro, acessar uma matéria específica e realizar o download de um arquivo.

🚀 Funcionalidades
O robô foi programado para executar as seguintes tarefas de forma autônoma:

Abertura do Navegador: Inicia uma instância visível do Google Chrome.

Navegação Multi-Etapas:

Acessa o portal principal do AVA.

Seleciona a instituição correta (Unieuro).

Navega da página inicial da Unieuro até a página de login.

Login Automático: Preenche as credenciais de usuário e senha e clica no botão para acessar a plataforma.

Acesso Direto à Matéria: Após o login, navega diretamente para a URL da matéria especificada.

Download de Arquivo:

Localiza o link de um arquivo específico na página da matéria.

Acessa a página de visualização do arquivo e força o download automático para uma pasta local.

🛠️ Tecnologias Utilizadas
Python 3: Linguagem de programação principal.

Selenium: A principal ferramenta para automação de navegadores web.

ChromeDriver: O "driver" que permite ao Selenium controlar o Google Chrome.

📋 Pré-requisitos
Antes de executar, garanta que você tenha os seguintes itens instalados no seu computador:

Python 3: Download aqui (Lembre-se de marcar "Add Python to PATH" durante a instalação).

Google Chrome: O navegador precisa estar instalado.

⚙️ Como Configurar e Executar
Siga estes passos para colocar o robô em funcionamento.

1. Baixar o ChromeDriver
Este script utiliza um ChromeDriver local. A versão do ChromeDriver precisa ser a mesma da versão do seu Google Chrome.

Verifique sua versão do Chrome: Digite chrome://settings/help na barra de endereço do navegador.

Baixe o driver: Acesse o Chrome for Testing Dashboard, encontre a sua versão e baixe o chromedriver-win64.zip.

Extraia o arquivo: Descompacte o arquivo .zip.

2. Organizar a Pasta do Projeto
Crie uma pasta para o seu projeto e organize os arquivos da seguinte forma:

/nome-da-sua-pasta
|
|-- executar_robo.py      (O código Python)
|-- chromedriver.exe      (O arquivo que você baixou e extraiu)
3. Instalar as Dependências
Abra um terminal (CMD, PowerShell, etc.), navegue até a pasta do seu projeto e instale a biblioteca Selenium com o comando:

Bash

pip install selenium
4. Configurar Suas Informações
Abra o arquivo executar_robo.py e edite as variáveis no topo do código com as suas informações:

SEU_USUARIO: Seu CPF ou identificação de usuário.

SUA_SENHA: Sua senha de acesso.

URL_DIRETA_DA_PAGINA_DA_MATERIA: O link da matéria onde o arquivo se encontra.

SELETOR_DO_LINK_DO_ARQUIVO: O texto do link do arquivo que você deseja baixar.

5. Executar o Script
Com tudo configurado, execute o script pelo terminal:

Bash

python executar_robo.py
Uma janela do Chrome se abrirá e executará todos os passos automaticamente. O arquivo será salvo na sua pasta de Downloads, dentro de uma nova pasta chamada downloads_faculdade.

📝 Estrutura do Código
O script é dividido em seções claras:

Configuração de Variáveis: No topo do arquivo, onde você define suas credenciais e URLs alvo.

Configuração do ChromeDriver: Define o caminho do download e as opções de inicialização do Chrome, como forçar o download de PDFs.

Inicialização do Selenium: Prepara o serviço e o driver do Chrome usando o chromedriver.exe local.

Bloco try...finally: Garante que todas as ações sejam executadas e que o navegador seja fechado no final, mesmo que ocorra um erro.

Lógica de Navegação e Ações: Contém a sequência de comandos get, click e send_keys que compõem o fluxo da automação.
