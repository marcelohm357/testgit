======Guia: Criando um Repositório Flutter com Git e VS Code======

Antes de enviar seu código para o GitHub, você precisa inicializar um repositório Git na pasta do seu projeto. Isso cria um histórico de todas as alterações que você fizer.

1. Inicializar um Novo Repositório (EXPLICAÇÕES DOS COMANDOS APÓS CRIAÇÃO DE REP.)

     Aqui está o que cada comando faz na primeira opção, para criar um novo repositório:

        echo "# TEST_GIT" >> README.md: Cria um arquivo chamado README.md e adiciona o texto "# TEST_GIT" a ele. O README.md geralmente contém uma descrição do seu projeto.

        git init: Inicializa um repositório Git vazio no diretório atual. Ele cria a pasta .git, que o Git usa para rastrear todas as alterações do seu projeto.

        git add README.md: Adiciona o arquivo README.md à "área de stage" (ou staging area). É como se você estivesse dizendo ao Git: "Prepare esse arquivo para o próximo commit".

        git commit -m "first commit": Salva as alterações que estão na área de stage no histórico do Git. A mensagem "first commit" descreve o que foi feito nesta primeira alteração. Pense no commit como uma fotografia do seu projeto naquele momento.

        git branch -M main: Renomeia a branch padrão de "master" para "main". A branch "main" é a linha principal de desenvolvimento do seu projeto.

        git remote add origin https://github.com/marcelohm357/TEST_GIT.git: Conecta o seu repositório local com o repositório remoto no GitHub. O origin é um apelido para essa URL, facilitando o trabalho.

        git push -u origin main: Envia (ou push) as alterações do seu repositório local para o repositório remoto no GitHub. O -u define o origin main como a branch padrão, então nas próximas vezes você pode usar apenas git push.

2. Enviar um Repositório Existente (EXPLICAÇÕES DOS COMANDOS APÓS CRIAÇÃO DE REP.)

     Já esta segunda opção é para quando você já tem um projeto com Git iniciado localmente e quer conectá-lo e enviá-lo para o GitHub:

        git remote add origin https://github.com/marcelohm357/TEST_GIT.git: Assim como na primeira opção, este comando conecta seu repositório local com o repositório remoto no GitHub.

        git branch -M main: Renomeia a sua branch principal para "main".

        git push -u origin main: Envia seu repositório local para o GitHub.

Este guia cobre os passos para iniciar um novo projeto Flutter e conectá-lo a um repositório Git, usando o VS Code como ambiente principal e o GitHub Desktop para gerenciar o repositório.

3. Crie o Repositório no GitHub

    A- Primeiro, crie um novo repositório vazio diretamente no GitHub.

    B- Acesse o GitHub e clique no botão "New".

    C- Dê um nome ao seu repositório. Por exemplo, meu_app_flutter. Lembre-se que o nome deve estar em letras minúsculas e usar _ (underscore) se tiver mais de uma palavra para seguir a convenção do Dart.

    D-  Não marque a opção "Add a README file" ou ".gitignore". Deixe o repositório vazio.

    E- Clique em "Create repository".

4. Clone o Repositório para o seu Computador com o GitHub Desktop
    
    A- Agora, traga o repositório vazio do GitHub para a sua máquina usando o GitHub Desktop.

    B- Abra o GitHub Desktop.

    C- No menu superior, vá em File > Clone a repository.

    D- Na janela que se abre, selecione a aba "GitHub.com". Você verá a lista dos seus repositórios.

    E- Encontre o repositório que você acabou de criar na lista e selecione-o.

    F- Clique em "Choose..." para selecionar a pasta no seu computador onde você quer salvar o repositório.

    G- Clique no botão "Clone".

    H- Após a clonagem, o GitHub Desktop irá perguntar se você quer abrir o repositório. Selecione a opção para abrir com o Visual Studio Code.

    I- O VS Code será aberto na pasta do seu repositório, que ainda estará vazia.

5. Adicione a Estrutura do Projeto Flutter

        A- Aqui, você vai usar o comando do Flutter para gerar as pastas necessárias.

        B- Abra o Terminal do VS Code (Ctrl + '). Certifique-se de que o terminal está na pasta do seu repositório.

        C- Execute o comando para criar a estrutura do projeto na pasta atual:

                        

                         >   flutter create .   <

    
    
        O ponto (.) no final é crucial, pois ele instrui o Flutter a criar o projeto na pasta onde você já está.


6.  Entenda a Estrutura de Pastas do Flutter
    
    Após a criação, o Flutter gerará uma série de pastas e arquivos essenciais. É importante entender para que cada um serve:

        A. <android, ios, linux, macos, windows, web>: Essas pastas contêm os arquivos específicos para cada plataforma. Elas permitem que o seu aplicativo Flutter seja compilado e executado como um aplicativo nativo em cada sistema operacional, usando um único código-fonte na pasta lib.

        B. <lib>: Esta é a pasta mais importante. É onde você vai escrever a maior parte do seu código Flutter, na linguagem Dart. O arquivo main.dart é o ponto de entrada da sua aplicação.

        C. <assets>: Use esta pasta para armazenar recursos como imagens, fontes, vídeos ou qualquer outro arquivo que sua aplicação precise usar.

        D. <test>: Esta pasta é para os testes unitários e de widget da sua aplicação.

        E. <.gitignore>: Um arquivo especial que o Git usa para saber quais arquivos ou pastas ele deve ignorar ao rastrear as mudanças. Isso inclui arquivos de cache e build que não precisam ser enviados para o repositório.

        F. <pubspec.yaml>: Este arquivo de configuração gerencia as dependências do seu projeto. É aqui que você adiciona pacotes (bibliotecas) de terceiros que deseja usar no seu aplicativo.

7. Publique as Mudanças no GitHub

    Agora que o seu repositório local tem todos os arquivos do Flutter, é hora de enviá-los para o GitHub.

        A- Volte para o GitHub Desktop. Ele já terá detectado todas as mudanças (os novos arquivos do Flutter).

        B- Na caixa do lado esquerdo, digite uma breve descrição do que você está enviando. Por exemplo: Initial commit of Flutter project structure.

        C- Clique no botão Commit to main e depois em Push origin para enviar todas as alterações para o GitHub.

    Com isso, todos os arquivos do seu projeto Flutter serão enviados para o seu repositório no GitHub.

8. Entendendo e Usando o Arquivo README.md

    O README.md (onde o ".md" significa Markdown) é o arquivo de documentação mais importante em um repositório. Quando alguém visita seu projeto no GitHub, o conteúdo do README.md é a primeira coisa que ela vê, servindo como uma página de boas-vindas. Ele é usado para:

        Apresentar o projeto: Uma breve descrição do que o seu aplicativo faz.

        Fornecer instruções: Como instalar, rodar e usar o projeto.

        Documentar a jornada: Como você fez neste caso, para registrar o seu aprendizado e o processo de configuração.

    Para publicar este guia como seu README.md:

        No VS Code, clique no ícone "New File" na barra lateral.

        Nomeie o arquivo como README.md.

        Cole todo o texto deste guia no novo arquivo e salve-o.

        Vá para o GitHub Desktop, adicione uma mensagem de commit como Add README.md file e clique em Commit & Push para enviar a atualização para o GitHub.








Pronto! Agora, ao acessar a página do seu repositório no GitHub, você verá este guia completo. É uma ótima maneira de se organizar, documentar seu trabalho e mostrar seu progresso para outros desenvolvedores.