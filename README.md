#  Vinheria Agnello - Monitoramento Inteligente


O sistema tem como objetivo monitorar as condições ideais de armazenamento de vinhos, analisando temperatura, umidade e luminosidade, garantindo a qualidade do ambiente.

---

##  Integrantes

- Matheus Sá Teles  RM:571719
- Pedro Antônio RM: 572549 
- Guilherme Cunha Romano  RM: 569301
- Guilherme Alvejan RM: 570835 

---

##  Componentes utilizados

- Arduino (C/C++)
- Sensor DHT22 (temperatura e umidade)
- Sensor LDR (luminosidade)
- Display LCD I2C
- LEDs (verde, amarelo e vermelho)
- Buzzer
- VS Code
- Git e GitHub

---

##  Funcionamento do sistema

O sistema realiza leituras dos sensores a cada 5 segundos e avalia as condições ambientais.

Com base nos dados coletados, ele classifica o ambiente em três níveis:

###  Status OK (LED Verde)
- Temperatura entre 10°C e 15°C  
- Umidade entre 50% e 70%  
- Baixa luminosidade  

---

###  Alerta (LED Amarelo + buzzer leve)
- Temperatura fora do ideal OU  
- Luminosidade moderada  

---

###  Crítico (LED Vermelho + buzzer forte)
- Umidade fora do ideal OU  
- Luminosidade muito alta  

---

##  Sensores utilizados

###  DHT22
- Mede temperatura e umidade
- Conectado ao pino digital 7

###  LDR (Sensor de luz)
- Conectado ao pino analógico A0
- Valores utilizados:
  - Até 400 → Ambiente escuro (ideal)
  - 401 a 700 → Meia luz (alerta)
  - Acima de 700 → Muito claro (crítico)

---

##  Display LCD

O display alterna automaticamente entre 3 telas:

1. Luminosidade
2. Temperatura
3. Umidade

A troca acontece a cada 2,5 segundos.

---

##  Estrutura do Hardware

Componentes utilizados:

- Arduino Uno  
- Breadboard  
- 3 LEDs (verde, amarelo, vermelho)  
- Resistores  
- Sensor DHT22  
- Sensor LDR  
- Buzzer  
- Display LCD I2C  

### Ligações principais:

- LEDs:
  - Verde → pino 2  
  - Amarelo → pino 3  
  - Vermelho → pino 4  

- Buzzer → pino 5  
- DHT22 → pino 7  
- LDR → A0  
- LCD I2C → SDA/SCL  

---

##  Lógica do sistema

O sistema:

1. Realiza múltiplas leituras (5 leituras para maior precisão)
2. Calcula média dos valores
3. Verifica limites definidos
4. Atualiza:
   - LEDs
   - Buzzer
   - Display LCD

---

##  Organização do código

Principais funções:

- `fazerLeituras()` → coleta dados dos sensores  
- `atualizarIndicadores()` → controla LEDs e buzzer  
- `mostrarTela()` → alterna informações no display  
- `mostrarLuminosidade()`  
- `mostrarTemperatura()`  
- `mostrarUmidade()`  

---

## ▶️ Como executar o projeto

1. Conectar os componentes conforme o esquema
2. Abrir o código no VS Code / Arduino IDE
3. Instalar bibliotecas:
   - `LiquidCrystal_I2C`
   - `DHT sensor library`
4. Selecionar a placa Arduino Uno
5. Fazer upload do código

---

##  Observações

- O sistema realiza média das leituras para evitar variações bruscas
- Caso o sensor DHT falhe, o LCD exibirá mensagem de erro
- Projeto voltado para simulação de controle ambiental em vinherias




