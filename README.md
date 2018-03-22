# Pimp My Arduino

Criando Arduinos Sob Medidas - Um livro Open Source

<img src="https://i.imgur.com/p0PnWoR.png" height="818" width="626">

## Sumário
### 1. Prefácio
### 2. Mergulhando de Cabeça no UNO
### 3. Dissecando o UNO
### 4. Dividir para Conquistar
  * Microcontrolador
  * Alimentação
  * Programação
  * Área de Trabalho
  * Componentes Extras
  * Funcionais
### 5. Passeando pelos Blocos
### 6. A Comunidade Maker e o Creative Commons
### 7. Bananino
### 8. Considerações Finais

## 1 - Prefácio

<p align="justify"><b>O Arduino revolucionou o mundo.</b> Essa afirmação aparentemente exagerada se torna cada vez mais real na medida que se analisa os impactos que essa placa de prototipação de  circuitos eletrônicos acarretou no mundo Maker.  Sua história de origem apresenta uma de suas maiores conquistas, a eletrônica e a programação disponível para todos. Criada na Itália por um grupo de estudantes de design, o Arduino teve como objetivo principal a facilitação do desenvolvimento de qualquer aparelho eletrônico de maneira eficaz porém simples para qualquer “inventor”. Incrivelmente, a placa atingiu muito mais do que seu objetivo inicial, se tornando um fenômeno utilizado mundialmente que catalisou o desenvolvimento exponencial da comunidade Maker, onde pessoas de qualquer idade ou profissionalização têm a possibilidade de expressar a sua criatividade criando o que vier em suas mentes.</p>
 
<p align="justify">Após o sucesso mundial, começaram a surgir novas versões do Arduino. Nano, Mega, Mini, Esplora…. A marca Arduino atualmente possui inúmeras adaptações feitas para cada tipo de inventor ou projeto. Porém, o maior meio de desenvolvimento de novas maneiras de se reinventar a placa veio da gigantesca comunidade que cerca a plataforma. Por onde se procura, é possível encontrar cada vez mais adaptações criadas por pessoas comuns que tenham como interesse criar uma placa Compatível com Arduino feito sob medida, customizadas para atingir os objetivos que ela e seus projetos necessitavam.</p>

<p align="justify">O presente livro tem como objetivo detalhar da melhor maneira possível todas as informações necessárias para o desenvolvimento de uma placa Arduino própria. O funcionamento de um Arduino é muito simples e intuitivo, porém é necessário saber de algumas informações pertinentes ao substituir e adicionar componentes de um projeto já conhecido. Além disso, o universo Arduino não se limita apenas ao hardware (Eletrônica), podendo também abranger diversas questões de software (Programação).  A Banana Digital convida você, leitor, para explorar o mundo das possibilidades de uma simples placa.</p>

## 2 - Mergulhando de Cabeça no UNO

<p align="justify">De maneira geral, a versão UNO da placa Arduino (Figura 1) é a mais conhecida, simplesmente porque ela contém uma boa quantidade de portas de entrada e saída, memória interna, velocidade de processamento para projetos de pequeno porte. Enfim, é ideal para qualquer pessoa iniciando a sua aventura no mundo da eletrônica e se encaixa na grande maioria dos projetos. Neste capítulo do livro, vamos detalhar de maneira simplificada algumas características dessa placa.
Primeiramente, devemos observar e entender algumas das especificações dela. Observe a tabela abaixo:</p>

| Característica                  | Valor          |
|---------------------------------|----------------|
| Microcontrolador                | ATmega328P     |
| Tensão de Operação              | 5 volts        |
| Tensão de Entrada (Recomendada) | 7-12V          |
| Tensão de Entrada(Limites)      | 6-20V          |
| Pinos I/O                       | 14 (6 com PWM) |
| Pinos Analógicos                | 6              |
| Corrente por pino I/O           | 40 mA          |
| Corrente no pino 3.3v           | 50 mA          |
| Memória Flash                   | 32 kB          |
| SRAM                            | 2 kB           |
| EEPROM                          | 1 kB           |
| Velocidade de Clock             | 16 MHz         |

Tabela 1 - Especificações do Arduino UNO

---
<p align="justify">Se você já possui conhecimento sobre todas essas informações e sabe o que elas significam, sinta-se livre para ir para o próximo capítulo, caso contrário, iremos analisar esses dados.</p>

<img src="https://i.imgur.com/tnJnOTD.png" height="400" width="400">

Figura 1 - Arduino UNO

---
<p align="justify"><b>1.</b> Primeiramente, o <b>Microcontrolador</b>, isso é, o chip que controla o Arduino, é nele onde são realizadas toda a matemática, onde o código é armazenado e onde as instruções são realizadas, ou seja, ele é o “cérebro” da placa. No caso da UNO, o microcontrolador utilizado é o Atmega328P, desenvolvido pela Atmel.</p>

<img src="https://i.imgur.com/Ef6JAzF.png" height="267" width="400">

Figura 2 - ATMega328P

---

<p align="justify"><b>2.</b> A <b>Tensão de Operação</b> não apenas é a tensão necessária para o funcionamento da placa, mas também é a utilizada nos pinos I/O (Entrada e Saída). Portanto em todas as saídas e entradas digitais da placa, deverá “entrar” ou “sair” 5 volts.</p>

<p align="justify"><b>3.</b> Tanto a <b>Tensão de Entrada (Recomendada)</b> quanto a <b>Tensão de Entrada (Limite)</b> representam a tensão necessária na alimentação do dispositivo para o seu funcionamento. Esses valores decorrem do Regulador de Tensão da placa, sendo ele o componente que converte uma tensão mais elevada para uma tensão de referência fixa, nesse caso os 5V de Tensão de Operação. Portanto, o Regulador de Tensão do dispositivo (NCP1117) necessita no mínimo uma tensão de entrada de 6V para que na sua saída se tenha 5V. Além disso, só é permitido ter na sua entrada a tensão máxima de 20V, devido à potência máxima do componente, sendo essas as tensões limites (6V - 20V). Porém, para que a vida útil da placa seja a melhor possível, é recomendado a aplicação de uma tensão entre  7V e  12V.</p>

<p align="justify"><b>4.</b> <b>Os Pinos I/O</b>, também chamados de portas digitais, são as entradas e saídas digitais da placa. Através do código, é possível configurar cada uma como entrada ou saída de tensão (In ou Out). Se for configurada como saída, pode-se programá-la para o estado ligado (HIGH ou 1), onde a tensão na porta é de 5V, ou para o estado desligado (LOW ou 0), onde a tensão na porta é de 0V. Caso esteja configurado como entrada, é possível ler o estado da tensão aplicada sobre ela de maneira binária, ou seja, se está com 5V (1) ou com 0v (0). No caso da Arduino UNO, são 14 portas digitais para serem usufruídas.</p>

<p align="justify"><b>5.</b> Alguns dos Pinos I/O podem também ser configurados para emitirem sinais <b>PWM</b> (Modulação de Largura de Pulso). Esses sinais são utilizados muitas vezes para simular variações de tensões através do chaveamento entre os estados 1 e 0. Uma das aplicações por exemplo é para variar a velocidade de um motor de corrente continua controlado por um Arduino. Seis das 14 portas digitais do Arduino UNO podem ser utilizadas como emissoras de sinais PWM, sendo elas identificadas com um traço em cima do número do pino.</p>

