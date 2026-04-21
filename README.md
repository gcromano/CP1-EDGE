# Controle de Temperatura para Armazenamento de Vinhos

## Participantes 
Guilherme Cunha Romano RM:569301 
Matheus Sá Teles de Souza RM:571719
Pedro Antônio RM: 572549
Guilherme Alvejan RM:570835

## Descrição
Este projeto consiste em um sistema de controle de temperatura voltado para o armazenamento adequado de vinhos. O sistema utiliza três indicadores luminosos (LEDs) para representar visualmente o estado da temperatura do ambiente, de acordo com faixas recomendadas para conservação do produto.

O projeto foi desenvolvido em C++ utilizando a plataforma Arduino e simulado no ambiente Wokwi.

## Objetivo
Simular o comportamento térmico de um ambiente de armazenamento de vinhos e indicar, por meio de LEDs, se a temperatura está:
- Ideal
- Em estado de alerta
- Inadequada

Além disso, o sistema simula uma fase inicial de instabilidade térmica e, após um período, passa a operar apenas dentro da faixa ideal, representando a estabilização do ambiente.

## Funcionamento Geral
O sistema opera em duas fases:
1. Fase inicial: a temperatura varia entre valores que representam condições de alerta ou inadequadas.
2. Fase estabilizada: a temperatura passa a variar somente dentro da faixa ideal para armazenamento de vinhos.

A cada ciclo, o sistema avalia o valor da temperatura simulada e aciona apenas um LED correspondente ao estado atual.

## Faixas de Temperatura Utilizadas
As faixas de temperatura adotadas no projeto são baseadas em recomendações comuns para armazenamento de vinhos:

- Temperatura ideal (LED verde): entre 12 °C e 15 °C
- Situação de alerta (LED amarelo): acima de 15 °C até 18 °C
- Temperatura inadequada (LED vermelho): abaixo de 12 °C ou acima de 18 °C

## Componentes Utilizados
- Arduino Uno
- LED verde
- LED amarelo
- LED vermelho
- Três resistores de 220 ohms
- Simulador Wokwi

Não é utilizado sensor físico de temperatura. A variação térmica é simulada diretamente por software para fins didáticos.

## Linguagem e Ferramentas
- Linguagem: C++
- Plataforma: Arduino
- Simulador: Wokwi

## Justificativa da Simulação
A simulação da temperatura por software permite representar o processo de estabilização térmica de forma controlada e previsível, o que é adequado para ambientes educacionais e estudos conceituais de sistemas embarcados.
