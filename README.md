# B-DIRO: Bertoloti Didatic Robot

O **B-DIRO** é um robô didático desenvolvido para facilitar o ensino de **Dispositivos Lógicos Programáveis (DLPs/PLDs)** e linguagens de descrição de hardware (HDL). O projeto visa substituir a dependência de simuladores por uma plataforma física de baixo custo, onde os alunos podem testar circuitos lógicos em tempo real.



## 🎯 Objetivo
Proporcionar uma ferramenta prática para o estudo de eletrônica digital, álgebra booleana e sistemas embarcados, permitindo a transição do conhecimento teórico para a implementação em hardware reconfigurável.

## 🛠️ Especificações de Hardware

### Unidade Lógica
* **Chip ATF16V8B-15PU**: Um dispositivo lógico programável (EEPLD) que armazena a lógica de controle do robô.


### Atuadores e Sensores
* **Motores**: 2 Motores DC 6V com caixa de redução.
* **Driver de Motor**: CI MX1616 ou MX1508 (Ponte H).
* **Sensores de Linha**: Sensores óticos reflexivos infravermelhos (IR).
* **Sensores de Luz**: Foto-resistores (LDR) para modos de busca de luminosidade.

### Gravador de Hardware
Para programar o chip, o projeto inclui um gravador baseado em:
* **Arduino Nano**: Interface USB-Serial e controle de gravação.
* **Módulo Boost (MT3608)**: Elevador de tensão para fornecer os 12V-14V necessários para a gravação da memória Flash do chip.


## 💻 Software e Ferramentas
* **WinCupl**: Compilador para a linguagem CUPL.
* **Afterburner**: Software utilizado para carregar o ficheiro JEDEC (.jed) no chip através do Arduino.(https://github.com/ole00/afterburner/tree/version_4_legacy)
* **Linguagens**: VHDL e CUPL.

## 🚀 Como Utilizar

### 1. Criar a Lógica
Desenvolva a lógica desejada (ex: Seguidor de Linha) no WinCupl. O comportamento é definido por equações booleanas ou tabelas de verdade.


### 2. Gravar o Chip
Conecte o gravador ao computador e utilize o terminal (PowerShell/CMD) para enviar a lógica:
```powershell
# Verificar conexão e chip
afterburner i -d COM3 -t GAL16V8

# Gravar o arquivo de lógica
afterburner wv -d COM3 -t GAL16V8 -f projeto.jed

```

### 3. Testar no Robô
Insira o chip programado no soquete do robô B-DIRO e ligue a alimentação. O robô executará a lógica gravada instantaneamente.

## 👥 Equipe e Autores

Este projeto é um Trabalho de Graduação realizado na Fatec Jundiaí – Deputado Ary Fossen:

Alex Bertoloti do Carmo Grellet

João Vitor Comoti Pires dos Santos

Nicolas Kevin Fagundes Silva

Orientador: Prof. Me. Peter Jandl Jr.

## 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos e educativos.
