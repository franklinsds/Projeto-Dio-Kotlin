[Ir para o conteúdo](https://gist.github.com/cami-la/560b455b901778391abd2c9edea81286#start-of-content)

[ ](https://gist.github.com/)

[Todas as essências](https://gist.github.com/discover)[De volta ao GitHub](https://github.com/)





![@VagnerBellacosa](https://avatars.githubusercontent.com/u/83479901?s=40&v=4) 



<details class="details-reset details-overlay details-overlay-dark js-command-palette-dialog" id="command-palette-pjax-container" data-turbo-replace="" style="box-sizing: border-box; display: block;"><summary aria-label="gatilho da paleta de comando" tabindex="-1" role="button" style="box-sizing: border-box; display: list-item; cursor: pointer; list-style: none; transition: color 80ms cubic-bezier(0.33, 1, 0.68, 1) 0s, background-color, box-shadow, border-color;"></summary></details>

[![@Camila](https://avatars.githubusercontent.com/u/64323124?s=64&v=4)](https://gist.github.com/cami-la)

# [cami-la](https://gist.github.com/cami-la) / **[API para Sistema de Avaliação de Créditos.md](https://gist.github.com/cami-la/560b455b901778391abd2c9edea81286)**

Ativo pela última vez 2 dias atrás • [Denunciar abuso](https://gist.github.com/contact/report-content?content_url=https%3A%2F%2Fgist.github.com%2F560b455b901778391abd2c9edea81286&report=cami-la+(user))

- Se inscrever
-  Estrela[2](https://gist.github.com/cami-la/560b455b901778391abd2c9edea81286/stargazers)
-  Garfo0

[Código](https://gist.github.com/cami-la/560b455b901778391abd2c9edea81286)[Revisões19](https://gist.github.com/cami-la/560b455b901778391abd2c9edea81286/revisions)[estrelas2](https://gist.github.com/cami-la/560b455b901778391abd2c9edea81286/stargazers)

Embutir 





[Baixar ZIP](https://gist.github.com/cami-la/560b455b901778391abd2c9edea81286/archive/4c8626313c208870ff47c28c85bdbf83335f55b0.zip)

API para Sistema de Avaliação de Créditos

[Cru](https://gist.github.com/cami-la/560b455b901778391abd2c9edea81286/raw/4c8626313c208870ff47c28c85bdbf83335f55b0/API%20para%20Sistema%20de%20Avalia%C3%A7%C3%A3o%20de%20Cr%C3%A9ditos.md)

[**API para Sistema de Avaliação de Créditos.md**](https://gist.github.com/cami-la/560b455b901778391abd2c9edea81286#file-api-para-sistema-de-avaliacao-de-creditos-md)

# API para Sistema de Avaliação de Créditos

Uma empresa de empréstimo precisa criar um sistema de análise de solicitação de crédito. Sua tarefa será criar uma **API REST SPRING BOOT E KOTLIN** 🍃💜para a empresa fornecer aos seus clientes as seguintes funcionalidades:

- ### Cliente (cliente):

  - Cadastrar:
    1. **Solicitação:** *nome, sobrenome, cpf, renda, e-mail, senha, CEP e rua*
    2. **Resposta:** *String*
  - Editar cadastro:
    1. **Solicitação:** *id, primeiroNome, sobrenome, renda, CEP, rua*
    2. **Resposta:** *primeiroNome, sobrenome, renda, cpf, e-mail, renda, CEP, rua*
  - Visualizar perfil:
    1. **Solicitação:** *id*
    2. **Resposta:** *primeiroNome, sobrenome, renda, cpf, e-mail, renda, CEP, rua*
  - Deletar cadastro:
    1. **Solicitação:** *id*
    2. **Resposta:** *sem retorno*

- ### Solicitação de Empréstimo (Crédito):

  - Cadastrar:
    1. **Request:** *creditValue, dayFirstOfInstallment, numberOfInstallments e customerId*
    2. **Resposta:** *String*
  - Listar todas as qualificações de emprestimo de um cliente:
    1. **Solicitação:** *customerId*
    2. **Resposta:** *creditCode, creditValue, numberOfInstallment*
  - Exibir um emprestimo:
    1. **Requisição:** *customerId e creditCode*
    2. **Resposta:** *creditCode, creditValue, numberOfInstallment, status, emailCustomer e incomeCustomer*

  [![API para Sistema de Avaliação de Créditos](https://camo.githubusercontent.com/ef0b5d0d26c39c16d8a6e84da8bb84e56d2192bf7dd3efee5c7e08bc343f0a0f/68747470733a2f2f692e696d6775722e636f6d2f377068796131362e706e67)](https://camo.githubusercontent.com/ef0b5d0d26c39c16d8a6e84da8bb84e56d2192bf7dd3efee5c7e08bc343f0a0f/68747470733a2f2f692e696d6775722e636f6d2f377068796131362e706e67)
  Diagrama UML Simplificado de uma API para Sistema de Avaliação de Crédito

  [![Arquitetura em 3 atletas Projeto Spring Boot](https://camo.githubusercontent.com/d626239c1792fd86f917115024a2c347d1269c8193982da9ce8a3a2b0519a652/68747470733a2f2f692e696d6775722e636f6d2f314561355048332e706e67)](https://camo.githubusercontent.com/d626239c1792fd86f917115024a2c347d1269c8193982da9ce8a3a2b0519a652/68747470733a2f2f692e696d6775722e636f6d2f314561355048332e706e67)
  Arquitetura em 3 atletas Projeto Spring Boot

  ### DESAFIO

  Implemente as regras de negócios a seguir para a solicitação de concessão:

  1. o máximo de parcelas permitidas será 48
  2. data da primeira parcela deve ser no máximo 3 meses após o dia atual

  ------

  ### Links Úteis

  - [https://start.spring.io/#!type=gradle-project&language=kotlin&platformVersion=3.0.3&packaging=jar&jvmVersion=17&groupId=me.dio&artifactId=credit-application-system&name=credit-application-system&description=Credit%20Application%20System% 20with%20Spring%20Boot%20and%20Kotlin&packageName=me.dio.credit-application-system&dependencies=web,validation,data-jpa,flyway,h2](https://start.spring.io/#!type=gradle-project&language=kotlin&platformVersion=3.0.3&packaging=jar&jvmVersion=17&groupId=me.dio&artifactId=credit-application-system&name=credit-application-system&description=Credit Application System with Spring Boot and Kotlin&packageName=me.dio.credit-application-system&dependencies=web,validation,data-jpa,flyway,h2)
  - https://docs.spring.io/spring-boot/docs/2.0.x/reference/html/common-application-properties.html
  - https://medium.com/cwi-software/versionar-sua-base-de-dados-com-spring-boot-e-flyway-be4081ddc7e5
  - [https://strn.com.br/artigos/2018/12/11/todas-as-anota%C3%A7%C3%B5es-do-jpa-anota%C3%A7%C3%B5es-de-mapeamento/](https://strn.com.br/artigos/2018/12/11/todas-as-anotações-do-jpa-anotações-de-mapeamento/)
  - [https://pt.wikipedia.org/wiki/Objeto_de_Transfer%C3%AAncia_de_Dados](https://pt.wikipedia.org/wiki/Objeto_de_Transferência_de_Dados)
  - https://pt.wikipedia.org/wiki/CRUD
  - https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#repository-query-keywords
  - https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.query-methods.at-query
  - https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#glossary

  ------

  ### autor

  ![img](https://avatars.githubusercontent.com/u/64323124?v=4)
  **Camila Cavalcante**

  

  feito com❤️por Cami-la 👋🏽 Entre em contato!

  [![Emblema do Linkedin](https://camo.githubusercontent.com/851ca2b6c09b4301697aa2420a1c48731004bb3d10c1c01f8ce1ea8078944882/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d43616d696c612d626c75653f7374796c653d666c61742d737175617265266c6f676f3d4c696e6b6564696e266c6f676f436f6c6f723d7768697465266c696e6b3d68747470733a2f2f7777772e6c696e6b6564696e2e636f6d2f696e2f63616d692d6c612f)](https://www.linkedin.com/in/cami-la/) [![Selo do Gmail](https://camo.githubusercontent.com/517d4a4989827ca1e83e2f36c3b19eb3cd6fcde335ebcb9cefbcc4fc17a2d23f/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d63616d696c616473616e746f73636176616c63616e746540676d61696c2e636f6d2d6331343433383f7374796c653d666c61742d737175617265266c6f676f3d476d61696c266c6f676f436f6c6f723d7768697465266c696e6b3d6d61696c746f3a63616d696c616473616e746f73636176616c63616e746540676d61696c2e636f6d)](mailto:camiladsantoscavalcante@gmail.com)

  ### Contribuindo

  Este repositório foi criado para fins de estudo, então contribua com ele.
  Se te ajudari de alguma forma, ficarei feliz em saber. E caso você conheça alguém que se identifica com o conteúdo, não deixe de compatibilizar.

  Se possível:

  ⭐️estrela o projeto

  🐛Encontrar e relatar problemas



[![@VagnerBellacosa](https://avatars.githubusercontent.com/u/83479901?s=80&v=4)](https://gist.github.com/VagnerBellacosa)

Escrever Visualização

Adicionar texto de títuloAdicionar texto em negrito, <Ctrl+b>Adicionar texto em itálico, <Ctrl+i>

Adicione uma citação, <Ctrl+Shift+.>Adicionar código, <Ctrl+e>Adicionar um link, <Ctrl+k>

Adicione uma lista com marcadores, <Ctrl+Shift+8>Adicionar uma lista numerada, <Ctrl+Shift+7>Adicionar uma lista de tarefas, <Ctrl+Shift+l>

Mencionar diretamente um usuário ou equipeFaça referência a um problema ou pull request

Anexe arquivos arrastando e soltando, selecionando ou colando-os.O estilo com Markdown é suportado

Comente

## Rodapé

© 2023 GitHub, Inc.

Navegação no rodapé[Termos](https://docs.github.com/site-policy/github-terms/github-terms-of-service)[Privacidade](https://docs.github.com/site-policy/privacy-policies/github-privacy-statement)[Segurança](https://github.com/security)[Status](https://www.githubstatus.com/)[Documentos](https://docs.github.com/)[Entre em contato com o GitHub](https://support.github.com/?tags=dotcom-footer)[Preços](https://github.com/pricing)[API](https://docs.github.com/)[Treinamento](https://services.github.com/)[blog](https://github.blog/)[Sobre](https://github.com/about)