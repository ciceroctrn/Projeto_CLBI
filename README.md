# Projeto de modernização dos sistemas da Torre Anemométrica🗼 do Centro de Lançamento Barreira do Inferno para atender a implantação do software 🚀 SVO Roket 

Este repositório contém um script CRBasic desenvolvido para o datalogger **CR3000** da **Campbell Scientific**, utilizando **4 sensores RM Young modelo 05103** (anemômetros tipo aerovane) para medição de **velocidade, direção do vento e vento máximo**.

Este sistema é uma atualização do modelo anterior baseado no **CR23X**, e agora alimenta o sistema **SVO Rocket**, que recebe dados de vento tanto deste sistema quanto de uma **Estação Meteorológica de Altitude - Digicora II**.

Este repositório contém um script **CRBasic** desenvolvido para o datalogger **CR3000** da Campbell Scientific, utilizando **4 sensores RM Young modelo 05103** (anemômetros tipo aerovane) para medição de **velocidade e direção do vento**.

# 📋 Descrição do Script

O script realiza leituras a cada segundo e armazena os seguintes dados:

* Velocidade do vento (m/s)

* Direção do vento (graus)

* Tensão da bateria (V)

* Temperatura do painel (°C)

* Velocidade média (10 amostras)

* Direção média (10 amostras)

* Desvio padrão da velocidade (10 amostras)

# ⚙️ Funcionalidades

* Leitura de velocidade via `PulseCount` com fator de calibração específico

* Leitura de direção via `VoltSE` com fator de escala de 0.142

* Cálculo de estatísticas (média e desvio padrão)

* Armazenamento em tabela com intervalo de 1 segundo

# 📁 Estrutura do Repositório
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

# 🚀 Como Usar

1. Abra o software **LoggerNet** ou **CRBasic Editor** da Campbell Scientific

2. Carregue o script `rmyoung_cr3000.crb`

3. Compile e envie para o datalogger CR3000

4. Verifique os dados coletados na tabela `Dados_1s`

# 📡 Recursos Adicionais (opcionais)

O script pode ser expandido para incluir:

* Transmissão serial (RS232, FTP, etc.)

* Correção de direção com offset (ex: 225°)

* Exportação para cartão SD ou servidor remoto

# 🧑‍💻 Autor

Desenvolvido por **Técnico Cícero Tasso** com base em script original para o **CR23X**.

Se tiver dúvidas ou sugestões, fique à vontade para abrir uma issue ou enviar um pull request.

**Campbell Scientific®** e **RM Young®** são marcas registradas de seus respectivos fabricantes.
