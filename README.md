# Pimp My Arduino

Criando Arduinos Sob Medidas - Um livro Open Source

![](https://i.imgur.com/p0PnWoR.png)

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

<p align="justify">Se você já possui conhecimento sobre todas essas informações e sabe o que elas significam, sinta-se livre para ir para o próximo capítulo, caso contrário, iremos analisar esses dados.</p>

![](https://i.imgur.com/tnJnOTD.png)

Figura 1 - Arduino UNO
