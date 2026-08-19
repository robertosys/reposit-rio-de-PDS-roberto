# descrição caso de uso RESERVAR LIVRO.
## UCS 2 - "Use case 2".
### Atores:
* Aluno
* Descrição: Este caso de uso permite que um Aluno, após encontrar um livro de seu interesse, garanta a sua reserva para retirada posterior na biblioteca.
### Condições
* Pré-condições:
* 1. O Aluno deve estar logado no sistema.
* 2. O Aluno já deve ter selecionado um livro específico.
* Pós-condições:
* 1. Uma reserva é criada para o Aluno e o livro.
* 2. A quantidade de exemplares disponíveis é diminuída em 1.
### Fluxo principal.
* 1. O Aluno seleciona a opção "Reservar".
* 2. O sistema verifica a disponibilidade.
* 3. O sistema confirma que o Aluno não possui pendências.
* 4. O sistema registra a reserva.
* 5. O sistema atualiza o status do livro.
* 6. O sistema exibe uma mensagem de sucesso com a data limite para retirada.


### Fluxos Alternativos.
* FA-01: Livro Indisponível No passo 2 do Fluxo Principal, se não houver exemplares:
* a. O sistema informa a indisponibilidade.
* b. O sistema oferece a opção "Entrar na Fila de Espera".
* c. O caso de uso termina.

### Fluxos de Exceção.
* FE-01: Aluno com Pendências
* No passo 3 do Fluxo Principal, se o Aluno tiver pendências:
* a. O sistema exibe uma mensagem de erro.
* b. O caso de uso é encerrado.
