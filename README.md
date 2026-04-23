# Sistema de Monitoramento de Luminosidade para Vinheria Agnello

## Participantes
- Guilherme Cunha Romano — RM: 569301  
- Matheus Sá Teles de Souza — RM: 571719  
- Pedro Antônio — RM: 572549  
- Guilherme Alvejan — RM: 570835  



##  Descrição do Projeto

Este projeto consiste em um **sistema de monitoramento de luminosidade** utilizando **Arduino Uno** e um **sensor LDR (Light Dependent Resistor)**.  
O sistema foi desenvolvido para atender ao desafio proposto no contexto de uma **vinheria**, onde a qualidade do vinho pode ser afetada pelas condições de iluminação do ambiente.

Com base na luminosidade medida, o sistema sinaliza três estados diferentes por meio de **LEDs** e um **buzzer**, facilitando a identificação de situações normais, de atenção ou de risco.

---

##  Objetivo

- Medir a **luminosidade do ambiente** utilizando um sensor LDR  
- Converter o sinal analógico usando o **conversor A/D do Arduino**  
- Indicar visualmente o estado do ambiente através de LEDs  
- Emitir um **alerta sonoro** quando a luminosidade estiver em nível de risco  

---

##  Funcionamento do Sistema

O Arduino realiza a leitura do sensor LDR por meio da entrada analógica **A0**.  
O valor lido varia de **0 a 1023**, de acordo com a intensidade da luz no ambiente.

Com base nesse valor, o sistema trabalha com três níveis:

| Luminosidade | Estado | Indicação |
|-------------|-------|-----------|
| Baixa (< 300) | OK | 🟢 LED Verde |
| Média (300–699) | Atenção | 🟡 LED Amarelo |
| Alta (≥ 700) | Risco | 🔴 LED Vermelho + 🔊 Buzzer |

Quando o estado é **Risco**, o **buzzer é acionado por 3 segundos**.  
Caso a luminosidade continue elevada, o alarme volta a tocar.

---

##  Componentes Utilizados

- Arduino Uno  
- Protoboard  
- Sensor LDR (luminosidade)  
- Resistor 10kΩ (divisor de tensão do LDR)  
- 3 LEDs (verde, amarelo e vermelho)  
- 3 resistores de 220Ω (para os LEDs)  
- Buzzer  
- Jumpers  

---

##  Organização dos Pinos

| Componente | Pino Arduino |
|----------|--------------|
| LDR | A0 |
| LED Verde (OK) | 8 |
| LED Amarelo (Atenção) | 9 |
| LED Vermelho (Risco) | 10 |
| Buzzer | 6 |
| Alimentação | 5V e GND |

-
## Testes

- Cobrir o LDR → LED Verde aceso  
- Ambiente parcialmente iluminado → LED Amarelo aceso  
- Luz intensa (ex: lanterna do celular) → LED Vermelho + Buzzer  

---

##  Conclusão

Este sistema demonstra de forma prática:
- O uso de sensores analógicos  
- A conversão Analógico-Digital do Arduino  
- A automação de alertas visuais e sonoros  

Trata-se de uma solução simples, eficaz e didática para monitoramento ambiental, podendo ser facilmente expandida para incluir sensores de temperatura e umidade.

---
