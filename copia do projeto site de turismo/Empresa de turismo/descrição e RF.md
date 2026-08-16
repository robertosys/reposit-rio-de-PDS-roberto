# projeto de desenvolvimento de um site de viagens
* Caso de uso: UC-01
*     Nome: Tur-Tur 

## 2. Atores: Usuário / Banco de dados -

*Descrição: Permite que o usuário busque por passagens aéreas, podendo filtrar elas por preço e avaliação, usuário também poderá inserir avaliações e por fim ser redirecionado para a página da companhia aérea para concluir a compra.


### 3. Condições
 * Usuário deve possuir conexão com a internet
 * Usuário deverá estar logado no aplicativo 
 * O aplicativo deve estar em perfeito funcionamento podendo se comunicar com as APIs das companhias aéreas
 * O usuário é redirecionado com sucesso para a finalização da compra no site ou sistema da companhia 

#### 4. Fluxo Principal
 * Usuário devera Estar logado no aplicativo 
 * Usuário devera buscar o destino (lugar, preço, datas)
 * Usuário seleciona a opção "buscar"
 * O sistema consulta as companhias aéreas e exibe uma lista de passagens disponíveis.
 * O Usuário aplica os filtros de "Menor Preço" e/ou "Melhores Avaliações".
 * O sistema reorganiza e atualiza a lista de passagens conforme os filtros selecionados. 
 * O Usuário seleciona uma passagem específica do seu interesse.
 * O sistema mostra os detalhes da viagem, as avaliações e o botão de comprar na companhia aérea, também a opção de inserir avaliação
 * O usuário seleciona a passagem que quer comprar
 * O sistema redireciona o usuário para a página da companhia aérea

##### 5. Fluxo alternativo
* Nenhum voo encontrado ou incompatível com os filtros
* No passo 4 a 7 do Fluxo Principal, se não houver passagens que correspondam  à busca *original ou aos filtros aplicados:
* O sistema exibe uma mensagem informando que não há passagens disponíveis para aqueles filtros.
* O sistema oferece as opções "Limpar Filtros" ou "Alterar Datas".
* O Usuário altera os dados ou limpa os filtros, e o fluxo retorna ao passo 2 ou 3 do Fluxo Principal.

###### 6. Fluxo de exceção
* Falha de comunicação com as companhias aéreas: Se tiver algum erro com o site das companhias aéreas 
* O sistema mostra uma mensagem de erro que Não foi possível carregar as passagens no momento e pedir para que verifique sua conexão ou tente novamente mais tarde.
* O sistema exibe um botão "Tentar Novamente".
* O caso de uso é encerrado ou aguarda nova ação do usuário.
