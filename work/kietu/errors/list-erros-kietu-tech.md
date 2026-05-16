# 🐞 Erros Encontrados

---

## 1. Validação obrigatória de dados bancários no ambiente dev

No ambiente de desenvolvimento, a criação de um cliente ainda exige a inserção obrigatória dos seus dados bancários, mesmo em cenários onde isso não deveria ser necessário.

<p align="center">
  <img src="./img/imagem1.png" width="600">
</p>

---

## 2. Solicitação indevida de dados da organização ao criar conta como membro

Durante o processo de criação de conta por um membro, o sistema apresenta a janela para inserção dos dados da organização, mesmo quando a organização já existe.

Exemplo: um membro está apenas criando sua conta através da plataforma, porém recebe a solicitação para cadastrar os dados da empresa à qual pertence.

O problema ocorre principalmente quando o convite ainda não foi enviado ao membro. Ainda assim, o sistema precisa tratar esse cenário corretamente, permitindo que o membro prossiga sem precisar cadastrar novamente uma organização já existente.

---

## 3. Preenchimento automático incorreto dos campos da organização

Ao preencher os dados da organização, alguns campos passam a ser preenchidos automaticamente com o valor inserido no campo anterior, de forma incorreta.

Exemplo: ao preencher o campo “Nome da Organização”, o campo seguinte (“NIF”) já aparece automaticamente preenchido com o mesmo nome da organização.

O comportamento esperado seria que cada campo permanecesse vazio até que o utilizador inserisse manualmente as informações correspondentes.

---

## 4. Inconsistência entre frontend e backend ao registar cliente

Em determinado momento, ao inserir um cliente, o frontend apresentou a mensagem:

> “Não foi possível executar a operação, ou houve uma falha.”

No entanto, ao tentar registar novamente com os mesmos dados, o sistema informou que o cliente já existia.

Ou seja, o frontend indicou erro na operação, mas o backend executou o registo com sucesso.

---

## 5. Paginação não funcional nas listas

Os botões **ANTERIOR** e **SEGUINTE** nas listas de clientes e membros (e possivelmente outras listas) não estão funcionais.

Exemplo:
- Existem 17 funcionários
- A lista mostra apenas 15 por página
- Os botões de navegação deveriam estar ativos para permitir ver os restantes 2 registos

<p align="center">
  <img src="./img/imagem3.png" width="600">
</p>

<p align="center">
  <img src="./img/imagem4.png" width="600">
</p>

---

## 6. Campo de prazo obrigatório na criação de subtarefas

Atualmente, ao criar uma subtarefa, o sistema exige obrigatoriamente o preenchimento de um prazo.

No entanto, a tarefa principal já possui um prazo definido, o que torna desnecessária a obrigatoriedade de informar uma nova data para cada subtarefa criada.

Esse comportamento pode dificultar a criação rápida de subtarefas, já que o utilizador é forçado a definir uma data mesmo quando pretende apenas associar a subtarefa ao prazo já existente da tarefa principal.

O ideal seria permitir que a subtarefa herdasse automaticamente o prazo da tarefa principal, ou então tornar o campo de prazo opcional.

---

## 7. Subtarefa não desmarca no frontend

Uma subtarefa, após ser marcada como concluída, não é possível desmarcá-la no frontend, indicando possível problema de estado ou sincronização.

<p align="center">
  <img src="./img/imagem5.png" width="600">
</p>

---

## 8. Problema no Timestamp das Notificações

Todas as notificações estão a aparecer com a mensagem “há menos de um minuto”, independentemente do tempo decorrido. Possivelmente, o problema está relacionado com o frontend.

<p align="center">
  <img src="./img/imagem7.png" width="600">
</p>

---

## 9. Saudação inicial utiliza o e-mail em vez do nome do utilizador

Atualmente, ao entrar no sistema, a mensagem de boas-vindas apresenta o e-mail do utilizador.

Exemplo:
> “Bem-vindo, 2001.dnp@gmail.com”

No entanto, seria mais adequado e amigável apresentar o primeiro e último nome do utilizador.

Exemplo esperado:
> “Bem-vindo, Domingos Pedro”

Essa alteração melhora a experiência do utilizador, tornando a interface mais profissional, personalizada e intuitiva.

---

# ✅ Resolvidos

- [x] Notificações em Diferentes Edge Cases de Alteração de Tarefas

---

# 📌 Observação

Todos os problemas acima foram observados no ambiente de desenvolvimento e podem estar relacionados a:
- validações excessivas no frontend
- inconsistência entre frontend e backend
- problemas de estado (state management)
- paginação incompleta ou desativada
- preenchimento automático indevido de inputs
- tratamento incorreto de formulários e fluxos de convite
