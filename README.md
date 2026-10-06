# Projeto-Banco-de-Dados-Oficina-Mecanica
Criação de um esquema conceitual do Zero para o controle de ordens de serviço de uma Oficina Mecanica


##![Diagrama EER](Projeto%20Conceitual%20de%20BD%20Oficina%20Mecanica.png)



## Objetivo do desafio

Criar o esquema conceitual a partir da narrativa, contemplando:

- Clientes e veículos: clientes levam veículos para conserto ou revisão periódica.
- Equipe e mecânicos: cada veículo é atendido por uma equipe de mecânicos, que possuem código, nome, endereço e especialidade.
- Ordem de serviço: possui número, data de emissão, valor, status e data para conclusão dos trabalhos.
- Serviços e peças: o valor dos serviços vem de uma tabela de referência de mão-de-obra, e o valor das peças também compõe a OS.
- Autorização: o cliente autoriza a execução dos serviços.

## Como foi resolvido

- Clientes e veículos: um cliente pode ter vários veículos (1:N), e cada veículo pode ter várias OS (1:N).
- Equipe e mecânicos: uma equipe tem vários mecânicos (1:N) e executa várias OS (1:N).
- Ordem de serviço: guarda número, datas, valor e status, ligada a um veículo e a uma equipe.
- Serviços: ficam na tabela de referência de mão-de-obra, cada um com descrição e preço. Conserto e revisão são serviços da tabela. A relação com a OS é N:N.
- Peças: cada peça tem nome, código e valor. A relação com a OS é N:N, com a quantidade usada.
- Autorização: registrada na própria OS, com os campos Autorizacao e Data_Autorizacao.
