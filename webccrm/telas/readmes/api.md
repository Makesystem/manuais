# API


>### `Neste treinamento utilizaremos o Postman como ferramenta para montagem das requisições para API.`

---

![Postman](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/md_api/postman.png)

---

## 1 - Como baixar e instalar o Postman

### 1.1 - Baixar/Instalar para Windows
* Para baixar clique [aqui.](https://dl.pstmn.io/download/latest/win64)
* ▶️ Instalação bem simples, só avançar e ele já vai abrir o Postman ⤵️
  <br>
![PS](/md_api/instalação_win_1.png)

### 1.2 - Baixar/Instalar para Mac
* Para baixar clique [aqui.](https://dl.pstmn.io/download/latest/osx_arm64)
* ▶️ Instalação bem simples, o arquivo virá com formato .zip só extrair o instalador e efetuar a instalação, só avançar e ele já vai abrir o Postman.
>##### ![PS](/md_api/ps.png) _Se ficar alguma dúvida na instalação neste modo deixaremos um vídeo demonstrando melhor aqui no ícone do YouTube._ [![PS](/md_api/ytb.png)](https://www.youtube.com/watch?v=i9FQWDx8NIY)

---

## 2 - Configuração do Postman

### 2.1 - Efetuando login
* Depois de efetuado a instalação o Postman abrirá nesta tela ⤵️
  ![config_1](/md_api/config_1.png)
* Para criar uma conta é só clicar no __"Sign up for Free"__ ⤵️
  <br>
  ![criar_conta](/md_api/criar_conta.png)
  <br>
* Pode ser criada a conta com quaquer e-mail mas também com a opção de login mais facilitado com uma conta do Google ⤵️
  <br>
  ![config_2](/md_api/config_2.png)

### 2.2 - Criando o Workspace
* Depois de efetuado o login abrirá essa tela e clica em __Workspace__ para entrar nos ambientes de trabalho criado ou criar um novo  ⤵️
  <br>
  ![config_3](md_api/config_3.png)
  <br>
* Próxima tela clica em __Create Workspace__ para criar um ambiente de testes da API ⤵️
  <br>
  ![config_4](md_api/config_4.png)
  <br>
* Deixa marcado a opção __Blank Workspace__ para criar um ambiente em branco e depois _Next__ para ir para próxima parte de criação ⤵️
  <br>
  ![config_5](md_api/config_5.png)
  <br>
* Próxima parte seta o nome, alguma descrição e escolhe quem terá visão do **_Workspace_** ⤵️
* * __Personal__ -> Só o quem criou tem acesso;
* * __Team__ -> Todo o time tem acesso;
* * __Public__ -> Qualquer pessoa terá acesso;
  <br>
  ![config_6](md_api/config_6.png)
  <br>
* Agora estamos dentro do Workspace criado, clicamos no + que tem na tela e selecionamos a opção __![graphQL](md_api/graphQL.png) GraphQL__ ⤵️
  <br>
  ![config_7](md_api/api_1.gif)
  <br>
  * No campo **_Enter URL_** temos dois links para busca.
  * * Para filtrar as vendas -> 🔗 https://legacyapi.makesystem.com.br/sale/graphql
  * * Para o histórico de contatos -> 🔗 https://legacyapi.makesystem.com.br/historic/graphql
* E a **_Key_** que passamos no momento da contratação do serviço. ⤵️
  <br>
  ![config_8](md_api/api_2.gif)
  <br>
* Depois de configurado, virá todos os endpoints que teremos para efetuar as consultas, são eles: ⤵️
* * _listar_auditorias_
* * _listar_status_vendas_
* * _listar_vendas_

## 3 - Consumindo os Endpoints

### 3.1 - Listar Auditorias
* Quando marcar __listar_auditorias__ por padrão já vem marcado na query _dataAuditoria, dataRegistro, id e observacao_ ⤵️
  ![consumindo_endpoint_1](md_api/consumindo_endpoint_1.png)
* Dentro da query listar_auditorias tem os seguinte Argumentos:
* * __pagina__ ➡️ _Se no filtro que aplicar tiver mais que o limite de vendas setadas, será separado por páginas, marcando o campo, você pode colocar o número da página que quer trazer._
* * __contem_status_de_venda_da_auditoria__ ➡️ _Quando marcar a opção já vem com null escrito_ ![contem_null](md_api/contem_status_null.png)_, do lado do campo tem as duas opções  "_ ⚪ _true" ou "_ ⚪ _false". Sendo true para trazer no filtro as que contém os status e false para as que não contém._
* * __contem_usuarios__ ➡️ _Quando marcar a opção já vem com null escrito._ ![contem_usuarios](md_api/contem_usuarios.png)_, do lado do campo tem as duas opções_  _"_ ⚪ _true" ou "_ ⚪ _false". Sendo true para trazer as vendas que tem usuário e false para as que não tem usuário._ 
* * __data_hora_minima__ e __data_hora_maxima__ ➡️ _Limitar a data e hora que quer efetuar a busca, se marcar esse campo precisa colocar a data no padrão_ __" 01/01/2023 ou 01/01/2023 23:59:59 "__ _( hora não é obrigatório )._
* * __ids_de_status_de_venda__ ➡️ _Para buscar um id específico, ( esses id são fornecidos no endpoint ._ __"listar_status_vendas"__ _)_ _o padrão é colocado entre colchetes_ _"_ __[ ]__ _"_ _Ex: [1,2,3,4]_ _"._
* * __ids_de_auditoria__ ➡️ _Para buscar por Id da auditoria._
* * __ids_de_usuarios__ ➡️ _Para buscar um usuário específico por id, ( esses id são fornecidos no endpoint._ __"listar_usuarios"__ _)._
* * __limite__ ➡️ _Para limitar quantos registos virá no arquivo ( Limite máximo é 100 registos )._
* * __ids_de_venda__ ➡️ _Para trazer o id da ação da venda._
* * __dataAuditoria__ ➡️ _Data setada quando troca de status._
* * __dataRegistro__ ➡️ _Quando a venda foi criada._
#### *  __itens__ ➡️ _Tem todos os itens da venda_ ⤵️
* * * ↪️ __motivoStatusItemVenda__ ➡️ _Dentro do sistema pode ser criado o status e ter um motivo para o mesmo e pode ser setado um motivo para o item, cada item da venda pode receber um status, pode ser cancelado só um item da venda e não ela completo._ ( **Exemplo =>** _Status da venda **Cancelada**, Motivo Cancelado cliente, Sem Viabilidade. )_
* * * ↪️ __pontos__ e __pontosBonus__ ➡️ _Se o produto for criado com método de pontos cadastrados, virá neste campo._
* * * ↪️ __produto__ ➡️ _Quais produtos estão vinculados à essa venda._
* * * ↪️ __statusItemVenda__ ➡️ _Se o status estiver ativo ou não, a descrição e o nome do status._
* * * ↪️ __tipoProduto__ ➡️ _Tipo do produto._
* * * ↪️ __valor__ ➡️ _Valor do produto._
* * * ↪️ __motivoStatus__ ➡️ _Dentro do sistema pode ser criado o status e ter um motivo para o mesmo._
#### *  __usuario__ ➡️ _As informações do usuário que tem para buscar:_ ⤵️
* * * ↪️ __documento__ ➡️ _Documento do usuário que fez a venda._
* * * ↪️ __email__ ➡️ _E-mail do usuário que fez a venda._
* * * ↪️ __login__ ➡️ _login do usuário que fez a venda._
* * * ↪️ __loginterceiro__ ➡️ _Se o usuário tiver login de terceiro utilizado em alguns dos nossos micro-serviços, aparecerá na venda._
* * * ↪️ __nome__ ➡️ _Nome do usuário que fez a venda._
<br>
  
### 3.2 - Listar Usuários
* * __pagina__ ➡️ _Se no filtro que aplicar tiver mais que o limite de vendas setadas, será separado por páginas, marcando o campo, você pode colocar o número da página que quer trazer._
* * __limite__ ➡️ _Para limitar quantos registos virá no arquivo ( Limite máximo é 100 registos )_
* * __texto_a_pesquisar__ ➡️ _Se quiser filtrar um nome específico, masrcando a opção abre um campo_ ![entervalue](md_api/enter_value.png)
* * __ativo__ _Se deixar desmarcado não vira se está ativo ou não._ **(true, false)**
* * __id__ _Para trazer o id no resultado de busca do usuário._
* * __nome__ _Para trazer o nome no resultado de busca do usuário._
<br>❇️ __Quando marcar _listar_usuarios_ por padrão já vem marcado as opções:__
  ➡️ _ativo, id e nome_

#### Como fica a query com todas as informações marcadas e preenchidas.⤵️
![query_listar_usuarios](md_api/query_listar_usuarios.png)

#### E o resultado ⤵️
![query_listar_usuarios_result](md_api/query_listar_usuarios_result.png)

<br>

### 3.3 - Listar Status das Vendas
* * __pagina__ ➡️ _Se no filtro que aplicar tiver mais que o limite de vendas setadas, será separado por páginas, marcando o campo, você pode colocar o número da página que quer trazer._
* * __limite__ ➡️ _Para limitar quantos registos virá no arquivo ( Limite máximo é 100 registos )_
* * __texto_a_pesquisar__ ➡️ _Se quiser filtrar um nome específico, marcando a opção abre um campo_ ![entervalue](md_api/enter_value.png)
* * __ativo__ _Se deixar desmarcado não vira se está ativo ou não._ **(true, false)**
* * __id__ _Para trazer o id no resultado de busca do status._
* * __nome__ _Para trazer o nome no resultado de busca dos status._
<br>❇️ __Quando marcar _listar_status_vendas_ por padrão já vem marcado as opções:__
➡️ _ativo, id e nome_

#### Como fica a query com todas as informações marcadas e preenchidas.⤵️
![query_listar_status_vendas](md_api/query_listar_status_vendas.png)

#### E o resultado ⤵️
![query_listar_status_vendas_resul](md_api/query_listar_status_vendas_result.png)
## 3.4 - Listar Vendas
* * __pagina__ ➡️ _Se no filtro que aplicar tiver mais que o limite de vendas setadas, será separado por páginas, marcando o campo, você pode colocar o número da página que quer trazer._
* * __ids_de_status_de_venda__ ➡️ _Para buscar um id específico, ( esses id são fornecidos no endpoint ._ __"listar_status_vendas"__ _)_ _o padrão é colocado entre colchetes_ _"_ __[ ]__ _"_ _Ex: [1,2,3,4]_ _"._
* * __ids_de_status_de_venda_auditoria__ ➡️ _Para buscar um id específico, ( esses id são fornecidos no endpoint ._ __"listar_status_vendas"__ _)_ _o padrão é colocado entre colchetes_ _"_ __[ ]__ _"_ _Ex: [1,2,3,4]_ _"._ 
* * __limite__ ➡️ _Para limitar quantos registos virá no arquivo ( Limite máximo é 100 registos )_
* * __contem_usuarios__ ➡️ _Quando marcar a opção já vem com null escrito._ ![contem_usuarios](md_api/contem_usuarios.png)_, do lado do campo tem as duas opções_  _"_ ⚪ _true" ou "_ ⚪ _false". Sendo true para trazer as vendas que tem usuário e false para as que não tem usuário._
* * __primeira_auditoria__ ➡️ _Quando marcar a opção já vem com null escrito._ ![primeira_auditoria](md_api/primeira_auditoria.png)_, do lado do campo tem as duas opções_  _"_ ⚪ _true" ou "_ ⚪ _false". Sendo true para trazer as vendas que tem usuário e false para as que não contêm primeira auditoria._
* * __data_hora_minima__ e __data_hora_maxima__ ➡️ _Limitar a data e hora que quer efetuar a busca, se marcar esse campo precisa colocar a data no padrão_ __" 01/01/2023 ou 01/01/2023 23:59:59 "__ _( hora não é obrigatório )._
* * __ids_de_usuarios__ ➡️ _Para buscar um usuário específico por id, ( esses id são fornecidos no endpoint._ __"listar_usuarios"__ _)._
* * __contem_status_de_venda__ ➡️ __contem_usuarios__ ➡️ _Quando marcar a opção já vem com null escrito._ ![contem_status_venda](md_api/contem_status_venda.png)_, do lado do campo tem as duas opções_  _"_ ⚪ _true" ou "_ ⚪ _false". Sendo true para trazer as vendas que tem usuário e false para as que não contêm status da venda._
* * __identificador__ ➡️ _Se quiser filtrar um identificador específico, marcando a opção abre um campo_ ![entervalue](md_api/enter_value.png)
* * __auditoriaExtra1, auditoriaExtra2 e auditoriaExtra3__ ➡️ _Se marcar essas opções, vira os extras atríbuidos a venda._
* * __dataRegistro__ ➡️ _Quando a venda foi criada._
* * __nomeCampanha, nomeCanal, nomeGrupo, periodoHabilitacao, solicitacao, pontosCampanha, tecnologia e telefoneLocalizado__ ➡️ _Deixando marcado, virá essas informações na busca._
<br>❇️ __Quando marcar _listar_status_vendas_ por padrão já vem marcado as opções:__
➡️ auditoriaExtra1, auditoriaExtra2, auditoriaExtra3, contrato, dataHabilitacao, dataInstalacao, dataRegistro, emInstalacao, idUltimaAuditoria, identificador, nomeCampanha, nomeCanal, nomeGrupo, periodoHabilitacao, periodoInstalacao, pontosCampanha, solicitacao, statusInstalacao, tecnologia, telefoneLocalizado, valor, valorManual, valorPromocao.
