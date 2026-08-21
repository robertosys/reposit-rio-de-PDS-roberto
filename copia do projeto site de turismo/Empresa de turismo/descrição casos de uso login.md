# Descrição do Caso de Uso: Login

## 1. Identificação e Nome

* **Nome do Caso de Uso:** Login
* **Código:** UC1

---

## 2. Atores e Descrição

* **Cliente:** Ator principal que inicia a solicitação de autenticação para acessar o sistema.
* **Banco de Dados:** Ator de suporte (externo) consultado para validar as credenciais fornecidas.
* **Descrição:** Permite que o cliente realize o acesso ao sistema por meio da verificação de suas credenciais de login.

---

## 3. Condições

* **Pré-condição:** O cliente deve possuir um cadastro prévio no sistema.
* **Pós-condição:** O cliente obtém acesso liberado ao site ou o acesso é negado caso as credenciais estejam incorretas.

---

## 4. Fluxo Principal

1. O **cliente** inicia a ação de login (`UC1`).
2. O sistema executa obrigatoriamente a validação de dados (`UC2`) (`<<include>>`).
3. O sistema consulta o **banco de dados** para verificar os dados informados (`<<include>>`).
4. O sistema concede o acesso liberado (`UC4`) (`<<extend>>`).
5. O sistema direciona o cliente para acessar o site (`UC3`) (`<<include>>`).

---

## 5. Fluxos Alternativos

* **5.1. Dados inválidos:**
* No passo 3 do fluxo principal, se o banco de dados retornar que os dados estão incorretos, o sistema aciona o fluxo de acesso negado (`UC5`) (`<<extend>>`).
* O sistema permite que o cliente retorne para a tela de login (`UC1`) para tentar novamente (`<<extend>>`).



---

## 6. Fluxos de Exceção

* **6.1. Indisponibilidade do Banco de Dados:**
* Caso o banco de dados não responda durante a validação (`UC2`), o sistema interrompe o processo de login e exibe uma mensagem de erro de conexão ao cliente.