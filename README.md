# SmartHome
Projeto disciplina AOC

Smart Home
Este software permitirá que o usuário controle via aplicativo web  os circuitos elétricos de sua casa, garantindo comodidade e segurança. Será utilizado um arquivo .txt para leitura, alteração e processamento dos dados para atualização do circuito. O arquivo será lido a cada 5 segundos e a partir disto o software realizará as alterações necessárias.

# Características 

Atualmente o software possui as seguintes características :

Utilização do Ômega para controlar e alterar os circuitos

Plataforma Linux 

Desenvolvimento em Shell Script

Versão : 1.0

# Codigo Fonte :

   API   : Smart Home	
   
   Autor : Filipe Henrique Calhau da Silva	
   		
   Data  : 20/11/2017			
   
   Versão: 1.2		
   
	Exibe o nome da aplicação
	
echo "Smart Home V1.2"

Inicia o loop

while true; do

conteudo=$(wget  -q -O -)	#  Lê o arquivo do servidor e salva o conteudo na variavel

fast-gpio set-output 0		# Configura o pino '0' como saida(output)

fast-gpio set 0 ${conteudo:0:1}	# Configura o valor do pino de acordo com o primeiro caracter do conteudo

fast-gpio set-output 1		# Configura o pino '1' como saida(output)

fast-gpio set 1 ${conteudo:1:1}	# Configura o valor do pino de acordo com o segundo caracter do conteudo
 

sleep 1; done	# Aguarda 1 segundo e inicia o loop novamente


# Pré-Requisitos 

Conexão com internet

# Suporte e colaboração

Para suporte ou colaboração (report de bugs ou melhorias no software) sinta-se á vontade para criar um novo report :
https://github.com/Vinilsx/SmartHome/issues




