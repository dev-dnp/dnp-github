# Erros Encontrados
---

## 1. No ambiente dev a criação de um cliente ainda exige a inserção obrigatória dos seus dados bancários:

![erro](./img/imagem1.png)

## 2. No ambiente dev, não se permite registar o mesmo IBAN:
   
![erro](./img/imagem2.png)

## 3. Houve um momento que inseri um cliente, mas surgiu uma mensagem no frontEnd dizendo que “Não foi possível executar a operação, ou houve uma falha”. Quando tentei registar novamente os mesmo dados, a aplicação respondeu-me que o “cliente já existe”. Ou seja, o frontend retornou um erro na operação, mas mesmo assim o backend registou os dados. Não pude capturar a mensagem, mas aconteceu isso.

<br>

## 4. Os botões de ANTERIOR e SEGUINTE nas listas dos clientes e membros, ou talvez mais outras listas, não está funcional. Por exemplo, eu tenho 17 funcionários e a minha lista só traz 15 por vez, nesta situação os botões devem estar ativos para permitir ver os outros dois  (2) clientes que faltam.

![erro](./img/imagem3.png)

![erro](./img/imagem4.png)

## 5. Uma subtarefa já marcada, não desmarca no frontend

![erro](./img/imagem5.png)
