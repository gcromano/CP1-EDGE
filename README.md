# Sistema de Monitoramento de Luminosidade para Vinheria Agnello

## Participantes
- Guilherme Cunha Romano — RM: 569301  
- Matheus Sá Teles de Souza — RM: 571719  
- Pedro Antônio — RM: 572549  
- Guilherme Alvejan — RM: 570835  

## Descrição do Projeto
Este projeto consiste no desenvolvimento de um sistema de monitoramento da luminosidade do ambiente da Vinheria Agnello, com o objetivo de garantir condições adequadas para o armazenamento de vinhos.

O sistema utiliza um Arduino em conjunto com um sensor LDR para realizar a leitura da intensidade luminosa do ambiente. Com base nesses valores, o estado do ambiente é indicado por meio de sinais visuais (LEDs) e sinal sonoro (buzzer).

A simulação foi desenvolvida e testada na plataforma Wokwi.

## Objetivo
Monitorar a luminosidade do ambiente e indicar seu estado por meio de LEDs, classificando-o em três níveis:

- Condição adequada
- Nível de alerta
- Condição crítica

Quando o ambiente se encontra em condição crítica, o sistema emite também um alerta sonoro por meio de um buzzer.

## Funcionamento do Sistema
O sensor LDR realiza a leitura contínua da luminosidade do ambiente. De acordo com o valor obtido, o sistema aciona apenas um LED por vez, indicando o estado atual:

- LED verde: indica que a luminosidade está dentro dos níveis ideais.
- LED amarelo: indica um nível de alerta.
- LED vermelho: indica uma condição crítica.

Quando o LED vermelho é acionado, o buzzer emite um sinal sonoro por 3 segundos, alertando sobre a condição crítica do ambiente.

## Critérios de Luminosidade
A luminosidade é classificada em três estados:

- Condição adequada (LED verde): luminosidade dentro do intervalo ideal.
- Nível de alerta (LED amarelo): luminosidade fora do ideal, porém ainda aceitável.
- Condição crítica (LED vermelho): luminosidade excessivamente alta ou baixa.

Os limites de cada faixa podem ser ajustados diretamente no código conforme a necessidade do projeto.

## Componentes Utilizados
- Arduino Uno
- Sensor LDR
- LED verde
- LED amarelo
- LED vermelho
- Resistores
- Buzzer
- Plataforma de simulação Wokwi

## Linguagem e Ferramentas
- Linguagem: C++
- Plataforma: Arduino
- Simulador: Wokwi

## Como Reproduzir o Projeto
1. Acesse a plataforma Wokwi.
2. Crie um novo projeto utilizando o Arduino Uno.
3. Monte o circuito conectando:
   - O sensor LDR a uma porta analógica.
   - Os LEDs às portas digitais, utilizando resistores.
   - O buzzer a uma porta digital.
4. Insira o código-fonte do projeto no editor.
5. Inicie a simulação.
6. Varie a luminosidade do LDR para observar a alternância dos LEDs e o acionamento do buzzer na condição crítica.