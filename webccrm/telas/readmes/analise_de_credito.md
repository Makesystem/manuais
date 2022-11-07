# ANÁLISE DE CRÉDITO

---

[![Logo_Make](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/img_padrao/makesystem.png)](https://www.makesystem.com.br/)

---

# 1 - Chegando na tela Análise de crédito
>## __1.1 - Caminho__
* _Clicamos no_ ![menu()](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/img_padrao/menu1.png) `Menu` ;
* _Depois clicamos em_  ![Serviços](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/img_padrao/servicos_1.png) `Serviços` -> ![Analise_de_crédito](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/img_padrao/analise_de_cr%C3%A9dito_1.png) `Análise de Créditos` ;

![Caminho](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/caminho.gif)
![](tela_analise_de_cr%C3%A9dito/caminho.gif)

# 2 - Criando
>## __2.1 - Cadastrando uma regra__
* _Clica no ícone de_ ![Mais](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/img_padrao/add_1.png) ;
* _Para adicionar uma regra nova_ ;

>## __2.2 - Nova regra de análise financeira__
* _Na primeira caixa temos dados necessários para regra_
* __Nome__ ➡️ _Nesta parte do cadastro é o único campo obrigatório_ ;
*  __Cidade__ ➡️ _Pode ser colocar quantas cidades quiser, separando-as por <span style="color:red">**" , "** </span>**( vírgula )** Ex: São Leopoldo, Canoas, São Paulo_ ;
*   __Bairro__ ➡️ _Pode ser colocar quantos bairros quiser, separando-os por <span style="color:red">**" , "** </span>**( vírgula )** Ex: Morro do Espelho, Centro, Campo Grande_ ;
* __Canais__ ➡️ _Depende dos canais que estão configurados dentro do sistema, pode ser marcados quantos quiser também_ ;

![Regra_Análise](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/regra_analise.gif)

---

>## __A Regra valida uma dessas sequências__
* __Cidade, Bairro e Canal__
* __Cidade e Bairro__
* __Cidade e Canal__
* __Cidade__
* __Canal__
* __Nenhum__

 <span style="color:black;background-color:rgba(144,202,249,1);padding:6px;">Se for criada uma regra preenchendo os 3 campos, a regra valida os 3 campos, o mesmo vale para as outras opções.</span>

---
>## __2.3 - Cadastro Serasa__
![Mensagem_serasa](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/mensagem%20serasa.png)
* _Na segunda caixa temos os dados que teremos quando efetuarmos a contratação do serviço Verify-Id_
* __clientId__
* __username__
* __password__

_Preenchendo esses três primeiros abre os campos de:_
* __Verify-Id Score minímo, que pode ir de `0` até `999`__
* __Verify-Id Risco máximo__
* * _Risco muito alto_
* * _Risco alto_
* * _Risco moderado_
* * _Risco baixo_
* * _Risco muito baixo_

![Regra_Serasa](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/cadastro_serasa.gif)

<br />

>## __2.3 - Cadastro Serasa VerifyId__
![Mensagem_serasa](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/mensagem%20serasa.png)
* _Na segunda caixa temos os dados que teremos quando efetuarmos a contratação do serviço Verify-Id_
* __clientId__
* __username__
* __password__
>#### ⚠️ __LEMBRANDO__ que essas Informações <span style="color:red;font-style: italic;">( clienteId, username e password )</span> são fornecidas pelo Serasa.

_Preenchendo esses três primeiros abre os campos de:_
* __Verify-Id Score minímo, que pode ir de `0` até `999`__
* __Verify-Id Risco máximo__
* * _Risco muito alto_
* * _Risco alto_
* * _Risco moderado_
* * _Risco baixo_
* * _Risco muito baixo_

![Regra_Serasa](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/cadastro_serasa.gif)

<br />

>## __2.3 - Cadastro Serasa PreQual__
![Mensagem_serasaPrequal](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/mensagem%20serasa%20PreQual.png)
* __request Path__
* __clientId__
* __clientSecret__
* __usarname__
* __password__
* __X-User-Domain__
* __X-Correlation-id__
* __Loja__
* __Recomendação Mínima__
* * ➡️ APROVADO
* * ➡️ NEGADO

![Regra_PreQual](https://github.com/Makesystem/manuais/raw/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/cadastro_prequal.gif)

>#### ⚠️ __LEMBRANDO__ que essas Informações <span style="color:red;font-style: italic;">( request Path, clienteId, clientSecret, username, password, X-User-Domain, X-Correlation-id e Loja )</span> são fornecidas pelo Serasa.

<br />

# 3 - Visualizar os dados
>## __3.1 - Onde configurar__
* _Clicando em_ ⚙️Configurações -> ⚙️Sistema _e vá até_
![Visualizar_os_dados](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/Visualisar%20dados.png)
* _Os contextos selecionados veem os dados da_ **`análise de crédito`** _e_ **`validações cadastrais`** ⤵️

![Visão_Auditoria](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/vis%C3%A3o%20auditoria.gif)
* _Os contextos não selecionados veem assim_ ⤵️

![Visão_venda](https://raw.githubusercontent.com/Makesystem/manuais/main/webccrm/telas/separacao_tela/tela_analise_de_cr%C3%A9dito/visao%20venda.gif)
<br />

---

# Ficou com alguma dúvida? entre em contato com o [Suporte](http://api.whatsapp.com/send?1=pt_BR&phone=555130661344).

### Todos os links que temos aqui podem ser abertos de duas maneiras:
* _Clicando com o botão direito do mouse -> `Abrir link em uma nova guia`_ ;
* _Clicando com o `Scroll` do mouse no link_ ;

---
