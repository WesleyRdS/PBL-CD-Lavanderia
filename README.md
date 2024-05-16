# Sistema de Controle para Lavanderia Automatizada

Este código em Verilog descreve a implementação de um sistema de controle para uma lavanderia automatizada. Abaixo está uma explicação detalhada de cada parte do código:

## Declaração de Entradas e Saídas

Define as entradas e saídas do módulo, incluindo sinais de botões, sinais de clock, chaves de controle, blocos de display de 7 segmentos e a saída do sistema.

## Divisor de Frequência

Utiliza um divisor de frequência para gerar dois sinais de clock, um deles dividido por 2^17 e o outro por 2^16, para controlar a exibição nos displays de 7 segmentos.

## Máquina de Estados para Debouncing (Debounce)

Implementa uma máquina de estados finitos (MEF) para eliminar oscilações rápidas nos sinais dos botões (debounce). Isso é feito para garantir uma entrada de sinal estável.

## Seleção de Máquina Disponível

Utiliza chaves de controle para determinar se uma máquina de lavar está disponível para uso. Isso é feito por meio de um processo de lógica combinacional e uma MEF.

## Recepção de Cedulas

Implementa a funcionalidade para receber cédulas nas máquinas de lavar. As cédulas são inseridas e processadas de acordo com o estado atual do sistema.

## Seleção do Tipo de Operação de Lavagem

Utiliza chaves de controle para selecionar o tipo de operação de lavagem desejada, como lavagem normal, delicada, etc.

## Bloco de Liberação da Máquina

Determina se uma máquina pode ser liberada para o próximo cliente com base nas operações concluídas e nas cédulas recebidas.

## Exibição nos Displays de 7 Segmentos

Controla a exibição nos displays de 7 segmentos, selecionando os valores corretos com base nos estados das máquinas, operações de lavagem e liberação da máquina.

Em resumo, o código implementa um sistema de controle completo para uma lavanderia automatizada, incluindo detecção de máquinas disponíveis, recebimento de cédulas, seleção de operações de lavagem e exibição de status nos displays de 7 segmentos.
