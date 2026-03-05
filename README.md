B-DIRO: Robô Didático com Dispositivos Lógicos Programáveis e VHDL
O projeto B-DIRO (Bertoloti Didatic Robot) consiste no desenvolvimento de um robô com propósitos didáticos para fomentar o aprendizado prático de Dispositivos Lógicos Programáveis (DLPs/PLDs). O sistema permite que estudantes coloquem em prática conceitos de eletrônica digital e linguagens de descrição de hardware (HDL) em um ambiente físico, saindo apenas da simulação.

🎯 Objetivo
Oferecer uma solução de baixo custo e montagem simplificada que viabilize o estudo de circuitos reais em sala de aula, tornando o aprendizado de eletrônica digital mais atrativo e prático.

🚀 Funcionalidades e Aplicações
O robô pode ser configurado para diferentes modos de operação através da lógica gravada no chip:


Seguidor de Linha: Utiliza sensores ópticos reflexivos para percorrer trajetos estabelecidos.


Modo Atrativo/Repulsivo: Utiliza sensores de luz (LDR) para perseguir ou fugir de fontes de luminosidade.


Lógica Customizável: Graças ao uso de DLPs, o comportamento do robô pode ser inteiramente remodelado via programação, sem necessidade de alterar o circuito físico.

🛠️ Tecnologias e Componentes
Hardware Principal

DLP ATF16V8B-15PU: Dispositivo lógico programável de alta performance que atua como o "cérebro" do robô.


Arduino Nano: Utilizado como interface para a gravação dos comandos no chip DLP.


Conversor DC/DC Step-Up (Boost): Responsável por elevar a tensão necessária para o processo de gravação do chip.

Sensores:

LDR (Foto-resistores) para detecção de luz.

Sensores ópticos reflexivos (infravermelho) para detecção de linha.


Atuadores: Motores DC 6V com caixa de redução e eixo duplo.

Software e Linguagens

Linguagens: VHDL e CUPL (Cornel University Programming Language).


WinCupl: Software para compilação do código e design do funcionamento do CPLD.


Afterburner: Código que permite a programação dos chips através do processador do Arduino.


Arduino IDE: Para carregar o firmware de gravação.

💻 Como Gravar o Circuito
A gravação do comportamento no chip segue o fluxo:

Desenvolver a lógica (Tabela Verdade) no WinCupl e gerar o arquivo .jed.

Calibrar a tensão de gravação no circuito gravador utilizando o comando afterburner via PowerShell.

Utilizar o comando afterburner wv para gravar e verificar o código no chip.

👥 Autores
Trabalho desenvolvido como requisito para o título de Tecnólogo em Sistemas Embarcados na Fatec Jundiaí – Deputado Ary Fossen:

Alex Bertoloti do Carmo Grellet 

João Vitor Comoti Pires dos Santos 

Nicolas Kevin Fagundes Silva 

Orientador: Prof. Me. Peter Jandl Jr. 

📄 Licença
Este projeto foi desenvolvido para fins acadêmicos. (Sugestão: Adicione aqui uma licença como MIT ou CC BY-NC).
