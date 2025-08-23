# Projeto de modernização dos sistemas da Torre Anemométrica🗼 do Centro de Lançamento Barreira do Inferno para atender a implantação do software 🚀 SVO Roket 

Este repositório contém um script CRBasic desenvolvido para o datalogger **CR3000** da **Campbell Scientific**, utilizando **4 sensores RM Young modelo 05103** (anemômetros tipo aerovane) para medição de **velocidade, direção do vento e vento máximo**.

Este sistema é uma atualização do modelo anterior baseado no **CR23X**, e agora alimenta o sistema **SVO Rocket**, que recebe dados de vento tanto deste sistema quanto de uma **Estação Meteorológica de Altitude - Digicora II**.

Este repositório contém um script **CRBasic** desenvolvido para o datalogger **CR3000** da Campbell Scientific, utilizando **4 sensores RM Young modelo 05103** (anemômetros tipo aerovane) para medição de **velocidade e direção do vento**.

---

## 📋 Descrição do Script

O script realiza leituras a cada segundo e armazena os seguintes dados:

* Velocidade do vento (m/s)

* Direção do vento (graus)

* Tensão da bateria (V)

* Temperatura do painel (°C)

* Velocidade média (10 amostras)

* Direção média (10 amostras)

* Desvio padrão da velocidade (10 amostras)

---

## ⚙️ Funcionalidades

* Leitura de velocidade via `PulseCount` com fator de calibração específico

* Leitura de direção via `VoltSE` com fator de escala de 0.142

* Cálculo de estatísticas (média e desvio padrão)

* Armazenamento em tabela com intervalo de 1 segundo

---

## 📁 Estrutura do Repositório

```plaintext
├── diagramas/                  # Diagramas de ligação dos sensores e dataloggers
├── manuais/                    # Manuais dos dataloggers CR23X, CR3000 e dos sensores RM Young 05103
├── src/                        # Código fonte das versões CR23X e CR3000
│   ├── cr23x/
│   └── cr3000/
├── loggernet_instalador/      # Instalador do programa LoggerNet
├── supervisório/              # Interface gráfica do sistema supervisório
├── operacao_manutencao/       # Procedimentos de operação e manutenção
└── README.md                  # Este arquivo com instruções e descrição técnica

```

---

## 🚀 Como Usar

1. Abra o software **LoggerNet** ou **CRBasic Editor** da Campbell Scientific

2. Carregue o script `rmyoung_cr3000.crb`

3. Compile e envie para o datalogger **CR3000**

4. Verifique os dados coletados na tabela `Dados_1s`

---

## 📡 Recursos Adicionais (opcionais)

O script pode ser expandido para incluir:

* Transmissão serial (RS232, FTP, etc.)

* Correção de direção com offset (ex: `225°`)

* Exportação para cartão SD ou servidor remoto

---

## 🧑‍💻 Autor

Desenvolvido por **Técnico Cícero Tasso** com base em script original para o **CR23X**.

Se tiver dúvidas ou sugestões, fique à vontade para abrir uma issue ou enviar um pull request.

**Campbell Scientific®** e **RM Young®** são marcas registradas de seus respectivos fabricantes.

---

## 📎 Licença

Este projeto é parte de um desafio acadêmico e **não possui fins comerciais**.

---

## 🤝 Contato

Desenvolvido por: **Cícero Tasso**  
GitHub: [@ciceroctrn](https://github.com/ciceroctrn/CR3000)

---

## 🔌 Diagramas de Ligação

### 📐 Canais Utilizados no CR3000

* **Sensor 1**: SE1 (direção), Pulse1 (velocidade), VX1 (alimentação)
* **Sensor 2**: SE3 (direção), Pulse2 (velocidade), VX2 (alimentação)
* **Sensor 3**: SE5 (direção), Pulse3 (velocidade), VX3 (alimentação)
* **Sensor 4**: SE7 (direção), Pulse4 (velocidade), VX4 (alimentação)

---

## 📡 **Comunicação**

* **LoggerNet**: RS232
* **SVO Rocket**: Conversor Serial/Ethernet

---

## 🚀 Como Usar

1. Abra o software **LoggerNet** ou **CRBasic Editor** da Campbell Scientific
2. Carregue o script `rmyoung_cr3000.crb`
3. Compile e envie para o datalogger **CR3000**
4. Verifique os dados coletados na tabela `Dados_1s`

---

## 🛠️ Operação e Manutenção

### ▶️ Procedimento de Inicialização

1. Verifique conexões físicas dos sensores RM Young 05103 ao CR3000.
2. Confirme alimentação nos canais VX1 a VX4.
3. Conecte o CR3000 ao computador via RS232.
4. Abra o LoggerNet ou CRBasic Editor.
5. Carregue e compile o script `rmyoung_cr3000.crb`.
6. Envie o script ao datalogger e verifique a tabela `Dados_1s`.

### 🔄 Procedimento de Manutenção

* **Mensalmente**:

  * Inspecione cabos e conectores dos sensores.
  * Verifique integridade dos sinais nos canais SE e Pulse.
  * Limpe os sensores RM Young 05103 com pano seco.

* **Trimestralmente**:

  * Verifique tensão da bateria e temperatura do painel.
  * Teste comunicação com LoggerNet e SVO Rocket.
  * Atualize firmware do CR3000 se necessário.

* **Anualmente**:

  * Calibre os sensores RM Young conforme especificações do fabricante.
  * Revise o script CRBasic para melhorias ou correções.

---

## 🖥️ Interface Gráfica do Supervisório

A interface gráfica do sistema supervisório pode ser desenvolvida com as seguintes características:

### 🧩 Componentes Visuais

* Painel de velocidade e direção do vento em tempo real
* Indicador de vento máximo registrado
* Gráficos históricos (linha ou barra)
* Indicadores de tensão da bateria e temperatura do painel
* Status de comunicação com LoggerNet e SVO Rocket

### 🛠️ Tecnologias Sugeridas

* **LabVIEW** ou **SCADA BR** para supervisório industrial
* **Python + Dash/Plotly** para aplicações web
* **Node-RED** para integração com MQTT e IoT

## 🔌 Comunicação

* Leitura dos dados via RS232 ou Ethernet
* Atualização em tempo real com intervalo de 1 segundo

---

## 📁 Estrutura Recomendada

```plaintext
├── supervisório/
│   ├── assets/                # Ícones e imagens
│   ├── scripts/               # Código da interface
│   ├── config/                # Arquivos de configuração
│   └── logs/                  # Logs de operação

```
---
