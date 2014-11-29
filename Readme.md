Objetivo geral: desenvolver conhecimento e prática de implementação de um escalonador de
processos em um sistema operacional didático.

Objetivos específicos:
a)analisar e planejar a implementação de um escalonador de processos no
sistema operacional xv6;
b)implementar o escalonador;
c)validar o escalonador através deexperimentos;
d)escrever um documento (extensão do documento apresentado no T1) descrevendo
todas os itens anteriores e uma conclusão do trabalho.

Plataforma:xv6 → http://pdos.csail.mit.edu/6.828/2012/xv6.html

Descrição do problema:implementar um escalonador de processos com quatro filas de processos
com seleção por loteria: Fila 0 até Fila 3; para seleção da fila, aplica-se o procedimento de loteria e,
após sorteio da fila, aplica-se a abordagem round robin internamente à fila concedendo a todos os
processos desta uma fatia (quantum) até o próximo sorteio (i.e., todos da fila sorteada são atendidos
uma única rodada, só então se realiza um novo sorteio e repete-se o procedimento).
Cada fila recebe um número fixo de bilhetes:
•Fila 0: 6 bilhetes;
•Fila 1: 3 bilhetes;
•Fila 2: 2 bilhetes;
•Fila 3: 1 bilhete.
Quando um processo é criado (instanciado), deve-se informar em qual fila o processo será inserido(i.e.,
o usuário define no instante da criação do processo).
