![UpperSoft](https://raw.githubusercontent.com/uppersoft/teste-front-end/master/assets/logo-readme.png)

# Teste front-end

Teste aos candidatos as vagas de desenvolvimento Front-end da UpperSoft.



## Objetivo

Simular uma aplicação que consiste em gerenciar usuários de um sistema.

Não será necessário qualquer tipo de validação de acesso ou outros tipos de tratamento, o propósito é simplesmente avaliar a capacidade de desenvolvimento das duas telas propostas com as respectivas integrações.

Ao final será possível apresentar suas habilidades com HTML, CSS, JavaScript, NPM/YARN e integração com APIs.



## Desafio

Serão duas telas que, juntas, simulam o acesso a um sistema de gerenciamento de usuários.


#### Layout

[CLIQUE AQUI PARA VISUALIZAR AS TELAS, CORES E FONTES UTILIZADAS](https://scene.zeplin.io/project/5eb20728d9cc2c193e4ed1df)

- **Login**: Tela contendo cabeçalho, com logo da empresa, e um box com: **título**, campos de **E-mail** e **Senha** e **botão de acesso.**
- **Lista de Usuários**: Tela contendo cabeçalho, título, lista em coluna contendo 6 cards com as informações do usuário (foto, nome, email e botão de editar) e informação de quantos usuários estão sendo mostrados e a quantidade total.

Todos assets, incluindo as telas do link acima, estão dentro da pasta `assets`.

- Font:
	- **Nome:** Helvetica Neue (Bold e Medium)
	- **Title - Primary [LG]:** HelveticaNeue, Bold, 48px
	- **Title - Primary:** HelveticaNeue, Bold, 32px
	- **Content - Gray [LG]:** HelveticaNeue, Medium, 22px
	- **Content - Primary:** HelveticaNeue, Medium, 16px
	- **Content - Gray:** HelveticaNeue, Medium, 16px
- Cores utilizadas:
	- **Primary:** #174DBA
	- **Gray:** #EFF0F3
	- **White:** #FFFFFF
	- **Dark:** #505050


#### Pré-requisitos

- Deverá ser apresentado dois arquivos HTML (**index.html** e **lista-usuarios.html**) e demais arquivos de assets.
- O header *(barra superior azul com a logo)* deverá ser fixa no topo da tela quando houver scroll.
- A tela deverá ser **responsiva** (desktop e mobile), ajustando o conteúdo conforme o tamanho da tela.
- Deve ser possível inserir o E-mail e Senha e, após clicar no botão, uma request deverá ser enviada para a API de login, após o response da API **deverá haver o direcionamento para a tela de Lista de Usuários**.
- Deve ser possível visualizar a lista com os primeiros 6 usuários que a API fake retornar.
- Deve ser possível visualizar quantos usuários estão sendo mostrados e o total de usuários.
- O botão de editar, no card de usuário na tela de Lista de Usuários, não precisa executar nenhuma ação, mas deve existir em forma de botão.
- Não deve ser utilizado nenhum framework de front-end ou estilo (Bootstrap, Tailwind, Vue.js, React ou outros).
- Não deve ser utilizado CDN para qualquer tipo de biblioteca utilizada.
- Para simulação dos dados de usuário e login deve ser utilizada a API fake [https://reqres.in/](https://reqres.in/), dados para integração abaixo e informações sobre a API no link.


#### Integração com API

##### Login

Deve ser feita uma **request** `POST` para a rota `https://reqres.in/api/login` com o body contendo os **dados de e-mail e senha informados no formulário**. Enquanto a request é feita o usuário deve **aguardar na página**. Após ser finalizada ele deve ser **direcionado para a tela de Lista de Usuários**.

Exemplo do body da requisição:
```
	{
	    "email": "email@uppersoft.com.br",
	    "password": "senha"
    }
```

##### Lista de Usuário

Deve ser feita uma **request** `GET` para a rota `https://reqres.in/api/users?page=1` e os dados da resposta devem ser mostrados na tela da seguinte maneira:

- A lista de usuários deve ser os dados contido no `data`.
- Texto informativo na parte inferior deve utilizar o `total` e `per_page`.

Exemplo de resposta da API:
```
{
   "page":1,
   "per_page":6,
   "total":12,
   "total_pages":2,
   "data":[
      {
         "id":1,
         "email":"george.bluth@reqres.in",
         "first_name":"George",
         "last_name":"Bluth",
         "avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/calebogden/128.jpg"
      },
      {
         "id":2,
         "email":"janet.weaver@reqres.in",
         "first_name":"Janet",
         "last_name":"Weaver",
         "avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/josephstein/128.jpg"
      },
      {
         "id":3,
         "email":"emma.wong@reqres.in",
         "first_name":"Emma",
         "last_name":"Wong",
         "avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/olegpogodaev/128.jpg"
      },
      {
         "id":4,
         "email":"eve.holt@reqres.in",
         "first_name":"Eve",
         "last_name":"Holt",
         "avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/marcoramires/128.jpg"
      },
      {
         "id":5,
         "email":"charles.morris@reqres.in",
         "first_name":"Charles",
         "last_name":"Morris",
         "avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/stephenmoon/128.jpg"
      },
      {
         "id":6,
         "email":"tracey.ramos@reqres.in",
         "first_name":"Tracey",
         "last_name":"Ramos",
         "avatar":"https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg"
      }
   ],
   "ad":{
      "company":"StatusCode Weekly",
      "url":"http://statuscode.org/",
      "text":"A weekly newsletter focusing on software development, infrastructure, the server, performance, and the stack end of things."
   }
}
```

Para maiores informações sobre como integrar com a API e exemplos de utilização acesse o [site da API](https://reqres.in/).


### Plus

- Utilização de NPM/Yarn para instalação de bibliotecas.
- Utilização de pré-processador de CSS (SASS/SCSS)
- Utilização do Axios para as requests.
- Utilização dos arquivos SVGs disponibilizados nos assets.
- Utilização de SessionStorage para armazenar o token recebido no login e permitir o acesso a tela de Lista de Usuários somente se houver token na SessionStorage.
- Loading enquanto aguarda resposta da API.



## Como fazer

Você deverá criar um fork desse projeto e realizar todo o desenvolvimento em seu repositório, ao final deve nos enviar o link para que seja feita a validação.