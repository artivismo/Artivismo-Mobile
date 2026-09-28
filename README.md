# Artivismo

> Sistema web e aplicativo mobile que se dispõe a ser um software arte-educador, propondo-se a ampliar a visão de mundo e aprofundar a sensibilidade de um aluno, além de também possibilitar um ensino anticolonial de arte. 

O Artivismo apresenta aulas e materiais de estudo que abordam conteúdos de Artes Visuais, possibilitando o aprendizado nas áreas de Desenho Tradicional, Desenho Digital, Colagem, Pintura, Fotografia e Escultura. Os conteúdos apresentados focam em abordar a arte de maneira anticolonial, ou seja, que fujam do padrão eurocêntrico e apresentam técnicas artísticas de outras culturas, valorizando a diversidade na Arte. As aulas são divididas em módulos, dentro de cada módulo há um "caminho" de aulas a ser seguido, as aulas são apresentadas em forma de slides em pdf e ao final de cada caminho haverá um exercício sugestivo para o usuário testar seus conhecimentos de forma prática, além disso, ao final dos módulos, o usuário terá acesso a um certificado de conclusão do curso. O software também conta com um fórum para a interação entre os usuários, que é dividido entre uma sala geral e salas específicas para as seis áreas artísticas presentes no sistema.

## Tecnologias utilizadas
* Node.js
* React Native
* Typescript
* Expo
* Firebase

## Descrição das funcionalidades

### Autenticação de usuários

A autenticação dos usuários é feita apartir da vinculação do projeto com um **back-end** estabelecido pela plataforma **Firebase**, essa plataforma fornece recursos de validação de contas por diversos meios, como email, senha, telefone, conta do google, entre outras, o projeto utiliza a autenticação por **email e senha**. Após a **tela inicial** de boas vindas, o usuário tem duas opções, se **cadastrar** e criar uma nova conta ou **entrar** com uma conta já cadastrada, sendo que essa opção só será válida se existir um cadastro para aquele email e senha na plataforma. Ao se cadastrar, o usuário indica seu **nome completo**, o **nome de usuário** (nome artistico), **Email**, **Telefone de contato**, **Senha** e a **Área Artística** que deseja estudar. A conexão com o Firebase é responsável por captar os dados de email e senha por meio dos formulários e **verificar** se esse conjunto já existe nos registros da plataforma, caso passe na verificação, uma mensagem de boas vindas será exibida para o usuário e ele irá ser **encaminhado para a página principal**, caso não, uma mensagem indicará que aquele email fornecido **já está sendo utilizado** e o usuário será encaminhado para a página inicial de boas vindas novamente. No caso do usuário tentar entrar por meio de uma conta já existente, Firebase fará uma verificação após captar os dados do formulário, caso aquele conjunto de email e senha estejá registrado no Firebase, será exibida uma mensagem de **boas vindas** e o usuário será encaminhado para a tela inicial, caso não, será exibida uma mensagem indicando um **erro na autenticação** e o usuário não conseguirá prosseguir.

### Módulos e aulas

Os módulos e aulas com conteúdos artísticos serão exibidos de acordo com a área artística escolhida pelo usuário na hora do cadastro, essa informação será guardada e por meio de condicionais, irá encaminhar o usuário para a tela de módulos correspondente á área artística escolhida. Dentro de cada tela inicial, existiram aproximadamente seis módulos de conteúdo e um certificado, que estarão bloqueados ou disponíveis. Tanto as aulas, quanto o certificado serão exibidos por meio de slides em pdf, que poderão ser baixados ou imprimidos caso o usuário queira.

> Observação: Esse projeto se encontra em construção e não foi finalizado. A funcionalidade dos módulos irá seguir um sistema de progresso, cujo cada módulo irá passar de **bloqueado**, onde o usuário não consegue acessar o caminho artístico, ou **disponível**, que tornará possível o acesso ao caminho de aulas, conforme o usuário termina um módulo, desbloqueia o próximo. Ao final de todas as aulas, o usuário terá acesso ao certificado e poderá vizualizar ou imprimi-lo.


### Fórum
    A seção Fórum do site foi desenvolvida com o auxílio da Biblioteca Socket.Io e o framework Express. 
   **Biblioteca SOCKET.IO**
    A Biblioteca Socket.io possui como objetivo, na aplicação web, abrir uma comunicação persistente entre cliente e servidor trocando uma requisição HTTP comum por uma a base de Websockets. Isto permite uma comunicação bidirecional entre cliente e servidor, ou seja ao invés de o cliente(Neste caso página Fórum) enviar uma mensagem e a partir dai o servidor enviar outra para que uma comunicação possa ocorrer, o cliente pode enviar quantas mensagens quiser independentemente da resposta que o servidor possa enviar, sendo isto também aplicável ao servidor, a resposta de um dos dois lados não e essencial para a comunicação entre eles.
    Esta Biblioteca foi escolhida justamente para facilitar e tornar mais rápida a comunicação entre os usuários em tempo real, promovendo uma real socialização entre eles.
    **Express**
    Atualmente o Framework Express não possui grande participação na elaboração atual do fórum sendo responsável apenas pelo fornecimento do servidor para a integração ao socket.io tornando-o responsável pela comunicação bidirecional, entretanto, essa função poderia facilmente ser substituida uma vez que o próprio socket.io poderia ter essa função. Sua função, portanto, será assegurada no futuro com uma maior adição de recursos ao chat, como por exemplo o upload de imagens que exigirá rotas http sendo essa uma grande utilização do Framework.

>Observação: A elaboração do fórum só foi realizada no desenvolvimento da aplicação web, por conta disso as tecnologias utilizadas só constam com seus datalhamentos na versão web.

### Perfil do usuário
As informações cadastrais do usuário estarão disponíveis na página de perfil, sendo elas:
* **nome completo**
* **nome de usuário** (nome artistico)
* **Email**
* **Telefone de contato**

Esses dados aparecem um embaixo do outro respectivamente, será exibida também a **Área Artística** escolhida, que aparece ao lado dos outros dados. Além disso, o usuário poderá alterar esse dados caso queira, basta clicar em **editar perfil**, após a alteração clicar em **salvar** e os novos dados serão exibidos na página.
> Observação: Esse projeto se encontra em construção e não foi finalizado. O perfil também exibe uma foto de perfil e uma imagem de banner acima dos dados cadastrais, essas imagens serão alteráveis na página de **alterar perfil**, assim como os outros dados.
 

## Como executar (Pré-requisitos)
* Instalar o Node.js na sua máquina


### Executando a Aplicação Mobile
1. Abrir a pasta do projeto mobile no terminal
2. Executar o comando **"npm install expo"** 
3. Executar o comando **"npx expo install"**
4. Executar o comando **"npx expo start"**


