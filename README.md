# -Álbum-de-Fotos---Desenvolvimento-de-Interfaces-WEB
Trabalho feito durante a disciplina de Desenvolvimento de Interfaces WEB, onde o objetivo era, utilizando ferramentas como HTML, CSS e JavaScript, construir um álbum de fotos responsivo utilizando JSON Server e um álbum geolocalizado.

Nesse trabalho, dei vida ao layout, apresentando informações reais sobre os álbuns, obtidas dinamicamente a partir de um servidor JSON Server que oferece uma API e servirá como back end da aplicação. 

Para montar minha aplicação utilizei o JSONServer como repositório para os dados e a API do Mapbox para exibição de mapas com os álbuns geolocalizados. 

JSONServer
O JSONServerLinks to an external site. oferece uma API baseada no padrão RESTful para acesso e manipulação de dados dispostos em um arquivo JSON no servidor. Um exemplo funcional do JSONServerLinks to an external site. está acessível no ambiente do Replit e você pode utilizar como base para o seu trabalho. Para isso, basta clonar (procedimento de FORK no Replit) e alterar o arquivo db.json, colocando os seus dados. 

INFO  

Exemplo de uso: https://replit.com/@rommelpuc/JSONServerLinks to an external site. (REPLIT)
Referrência da API do JSON Server: https://github.com/typicode/json-serverLinks to an external site.
 

Mapas com Mapbox
A API do MapboxLinks to an external site. permite a criação de mapas em sites web, bem como a utilização de uma série de outras funcionalidades associadas como navegação e pesquisa de endereços, para citar algumas. Será necessário criar um conta no ambiente do Mapbox e criar uma access token a ser incluída na sua aplicação.  

INFO 

Exemplo de uso: https://replit.com/@rommelpuc/MapboxLinks to an external site. (REPLIT)
Referência da API: https://docs.mapbox.com/mapbox-gl-js/api/Links to an external site.
 

Estruturas de Dados
Você deve estruturar os dados para a montagem da sua aplicação. Utilize o projeto de exemplo do JSONServer, faça uma cópia para o seu trabalho. No arquivo db.json, você deve criar as suas estruturas de dados. 

Para a montagem do seu trabalho, deve haver, pelo menos, três estruturas distintas: (1) álbuns, (2) fotos e (3) destaques. As informações básicas e OBRIGATÓRIAS de cada uma das estruturas mencionadas são apresentadas a seguir

ESTRUTURA ÁLBUNS

Identificador do álbum
Título do álbum
Descrição do álbum
Localização geográfica do álbum (longitude e latitude)
Data do álbum
URL da imagem de capa do álbum
 

ESTRUTURA FOTOS

Identificador da foto
URL da imagem
Descrição da imagem
Identificador do álbum ao qual a foto faz parte 
 

ESTRUTURA DESTAQUES

Identificador do destaque
Identificado do álbum em destaque
Texto para destaque (pode ser a própria descrição do álbum ou um texto alternativo)
 

Detalhamento do escopo
O trabalho deve contemplar as seguintes telas e suas funcionalidades descritas em seguida.

Tela principal

O cabeçalho traz o nome, o logotipo do site e um menu de opções 
A página deve apresentar um carrossel com fotos registradas na estrutura DESTAQUES e que fazem parte dos diversos álbuns registrados na aplicação
ORIENTAÇÃO: use componente do bootstrap
A página deve apresentar uma grade com todos os álbuns registrados na estrutura ÁLBUNS.  Deve ser apresentada as seguinte informações associada a cada um dos álbuns exibidos na página: uma imagem, o título do álbum, um breve descritivo (20 caracteres) e um link para mais detalhes desse álbum.
A página deve apresentar um mapa com marcadores sinalizando a localização geográfica de cada um dos álbuns registrados na esturtura ÁLBUNS.
ORIENTAÇÃO: utilize o exemplo do MapboxLinks to an external site. para montar o seu mapa
Rodapé com informações sobre responsável pelo site (aluno/aluna) 
 

Tela de detalhes do ÁLBUM

Informações gerais do ÁLBUM que apresente: foto de capa do album, título, descritivo, geolocalização (endereço ou latitude/longitude) e data de registro
Deve ser possível marcar o álbum como um destaque para ser exibido na home-page registrando essa informação na estrutura DESTAQUES (via requisição de POST na API JSONServer)
Grade com fotos incluídas no ÁLBUM e apresentadas de forma reduzida (thumbnail) com descrição. Os dados devem ser obtidos da estrutura FOTOS. 
 

Tela/popup/modal de zoom da FOTO 

A funcionalidade (página independente, popup ou modal) deve apresentar as fotos do álbum na forma de um carrossel, oferecendo botão para exibir a foto anterior e a próxima foto
A página de detalhes pode ser apresentada de forma independente da tela do álbum ou como um popup (no caso de popup, colocar botão para fechar ou fechar com tecla ESC) 
A página deve apresentar a descrição da foto de forma visível
