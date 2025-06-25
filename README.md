# 🔔 PROJETO: TAREFAS COM DISPLAY E LED USANDO FreeRTOS - BITDOGLAB

**Autores:**

- FELIPE LEME CORREA DA SILVA
- VITOR GOMES DE SOUZA

**Instituição:**

- EmbarcaTech - HBr - Campinas

---

# 📦 SOBRE O PROJETO

Este projeto demonstra o uso de [**FreeRTOS**](https://www.freertos.org) com a placa de desenvolvimento [**BitDogLab**](https://github.com/BitDogLab) para executar múltiplas tarefas simultaneamente, utilizando um **display** e um **LED RGB** para mostrar a temperatura interna da **Raspberry Pi Pico**.

O sistema é composto por duas tarefas principais:

- Uma tarefa que faz a leitura da **temperatura interna** e a mostra no display em tempo real.
- Uma tarefa que alterna as cores do **LED RGB** conforme a temperatura lida: abaixo de 33ºC fica verde, amarelo entre 33ºC e 39ºC e vermelho acima de 40ºC.

---

# 🗂️ ESTRUTURA DO PROJETO

```
/tarefa-freertos-2-felipe_e_vitor
│── include/                             # Arquivos auxiliares
│── FreeRTOS                             # Arquivos da biblioteca da FreeRTOS utilizado no projeto
│── tarefa-freertos-2-felipe_e_vitor.c   # Código principal com FreeRTOS
│── CMakeLists.txt                       # Script de build do projeto
│── README.md                            # Este documento
│── LICENSE.txt                          # Licença do projeto
```

# 🛠️ FUNCIONALIDADES IMPLEMENTADAS

- ✅ Execução simultânea de tarefas com FreeRTOS
- ✅ Leitura de temperatura interna da Raspberry Pi Pico
- ✅ Mostra no display o valor da temperatura
- ✅ Alternância de cores no LED RGB (vermelho, verde, azul)

# 🌐 CONFIGURAÇÕES DE HARDWARE

| Componente   | GPIO          | Função                     |
| ------------ | ------------- | -------------------------- |
| LED RGB      | GPIO 11,12,13 | Vermelho, Verde e Azul     |
| Display OLED | GPIO 14,15    | Comunicação I2C (SDA, SCL) |

# 🔄 FLUXO DE FUNCIONAMENTO

1. Ao ligar o sistema, aparerá "SISTEMA INICIANDO" no **display**.
2. Faz a leitura da **temperatura interna**.
3. Mostra a temperatura **lida** no display.
4. Checa em qual grupo se encaixa e seta a cor do **LED RGB** conforme este grupo.
5. O sistema continua operando em tempo real com **gerenciamento multitarefa via FreeRTOS**.

# 🖥️ Execução e Gravação no Pico

1. Compilar com:

```
mkdir build
cd build
cmake ..
make
```

2. Copiar o ".uf2" gerado para o Raspberry Pi Pico W.

# ⚙️ TECNOLOGIAS UTILIZADAS

- C com Pico SDK
- FreeRTOS (multitarefa cooperativa)
- Temperatura interna do RP2040
- I2C com display OLED SSD1306
- BitDogLab (Raspberry Pi Pico W com periféricos integrados)

# 📹 MÍDIA

[**Vídeo demonstrativo**](https://www.youtube.com/watch?v=S7c0B9Y1x-M&list=PLEB5F4gTNK68zDlrXbcCgJ6NejaP0PvHX&index=15)

# 📜 Licença

- GNU GENERAL PUBLIC LICENSE
