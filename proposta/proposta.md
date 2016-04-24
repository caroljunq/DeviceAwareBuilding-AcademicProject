DeviceAwareBuilding-AcademicProject
====================================

# 0 - Como ler este trabalho

> isto é um comentário  
> *especialmente coisas em itálico*

[Isto é uma referencia] e de vez em quando [isto também](https://duckduckgo.com
"Tudo que você precisa")

Este trabalho está em andamento, a versão final será em LaTeX (PDF) então **Não
confie neste texto**

# 1 - Introdução

>_Contexto_  
_IoT como foco_

Recentemente Internet das Coisas (IoT - *Internet of Things*) vem tomando o foco
das atenções de empresas e entusiastas de Tecnologia da Informação (IT -
*Information Tecnology*) [DzoneIoT:2015] a tal ponto que as empresas líderes do
segmento já incluem IoT como uma de suas áreas de atuação [Ibm2016] [ARM-mbed]
[Microsoft2016] [Intel2016] [Oracle2016] [Google2016] [AmazonIoT2016].

Todo este movimento no mercado é justificado pelo baixo custo dos pequenos
dispositivos computacionais [RpiZeroLaunch] [Esp8266.net] e grandes
serviços na nuvem [Kaufmann2015] [Amazon2016]. Este baixo custo
possibilita a computação ubíqua descrita por Weiser em 1991 e 1992
[Weiser1999] que é entendida pelos autores como *"computação virtualmente
onipresente"*. Também para os autores esta virtual onipresença é base e
consequência para a IoT sendo esta a realizadora da computação ubíqua.

Uma vez contextualizado o mercado e a oportunidade de implementação da
computação ubíqua, percebemos a necessidade de dar aos elementos cotidianos
(coisas) a capacidade info-computacional, tornando-os sensores e atuadores
conectados, unicamente identificáveis e acessíveis através da rede mundial
(internet) [Lemos2013] [Kranenburg2012].

> *Numero de dispositivos*

É esperado que uma quantia total de 6,4 bilhões de dispositivos conectados
exista até o final de 2016 [GARTNER2015] e entre 26 bilhões [GARTNER2014] e 50
bilhões até 2020 com até 250 novas coisas conectando-se por segundo
[CiscoBlog2013].

# 2 - Problema

> **Problema**  
*Grande quantidade de dispositivos*

Tamanha quantidade de dispositivos conectados pouco acrescenta na vida diária se
humanos ou coisas não puderem simplesmente se encontrar, tanto em ambiente real
quanto virtual é necessário o contato entre as partes para a existencia de uma
interação.

> *Introduza o problema de localizar e contextualizar cada dispositivo.*

Mais ainda, para melhor funcionamento de aplicações, em especial o oferecimento
de conteúdo específico para cada usuário e situação, é necessário contextualizar
e para muitas aplicações a localização é a informação contextual mais importante
e relvante.

Destacamos a necessidade da criação desta informação através de sensores ativos
sempre que necessário para que o dispositivo tenha ciência deste contexto em
suas tomadas de decisão e para que outros (sistemas, pessoas e coisas) saibam a
localização de qualquer dispositivo ao qual têm interesse de interagir.

> *Exemplo da perda de aparelhos no predio (zebra) (ou outro exemplo)*

Um exeplo da necessidade de localização de dispositivos dentro de um prédio
seria um profissional saber onde está o dispositivo em seu local de trabalho,
seja ele um vendedor e seu tablet para demostrar um produto fora de estoque em
uma loja ou um médico e um desfibrilador.



> *Soluções corelatas*  
*Nota do autor: Introduza os meios existentes de localização (marcelo).*

> GPS não funciona bem indoor, existem 2 tipos de indoor

## 2.1 - Sobre Sistemas de Posicionamento

Sistemas de posicionamento (PS - *Positioning System*) em geral determinam a
partir de um conjuto não vazio de pontos de referência (RP - *Reference Point*),
cuja localização global em relação a um ponto origem escolhido (*O*) é conhecida
e com precisão maior ou igual a interna do sistema, a posição relativa de um
ponto móvel dentro deste sistema (MU - *Mobile User*) aos RPs e consequentemente
a posição relativa ao *O*.

Para PSs eletônicos baseados em radio-frequência (RF - *Radio Frequency*)
geralmente utilizam-se dois componetes básicos, Transmissores e Receptores, seu
funcionamento assume que ao menos um destes está no RP e outro no MU. Para
calcular a posição do MU utiliza-se as propriedades da comunicação por RF como
tempo de chegada (TOA - *Time Of Arrival*), diferenial de tempo de chegada (TDOA -
*Time Difference Of Arrival*) e ângulo de chegada de sinal (AOA - *Angle Of
Arrival*).

Para maior precisão é comum a utilização de multiplas RPs, geralmente com o
número mínimo igual ao número de dimenções espaciais que deseja-se calcular.
Notamos que para sistemas distribuídos como a sincronização de relógios é um
problema clássico o tempo conta como dimenção.

Os sistemas classificados como "Sistema de Navegação Global por Satélite" (GNSS -
*Global Navigation Satellite System*) como o tradicional Estadounidense Sistema
de Posicionamento Global (GPS - *Global Positioning System*) utilizam a técnica
onde o dispositivo móvel contém o receptor e os transmissores são fixos em
satélites na órbita terrestre [Djuknic2001]. Devido a posição e número de
satélites o GPS e seus correlatos estão sempre presentes do ponto de vista de um
observador da superfície terrestre sendo para este tipo de usuário um sistema
ubíquo.

Entretanto a força do sinal GNSS não é suficiente para penetrar a maioria dos
prédios uma vez que estes dependem de visão direta (LOS - *Line-Of-Sight*) entre
os satélites e o receptor. A reflexão do sinal muitas vezes permite a leitura em
ambientes fechados, porém o cálculo da posição não será confiável
[Dartmouth2000].

Portanto, apesar da ubiquidade dos GNSSs em ambientes abertos, são necessárias
soluções diferentes para obter um Sistema de Posicionamento para Ambientes
Fechados (IPS - *Indoor Positioning System*) porém a ubiquidade deste é
essencial para conquistar o mesmo nível de confiânça trasido pelos GNSSs.

Para implementar este IPS propomos o uso de tecnologias já implantadas em
dispositivos e ubíquoas como Wi-Fi (padrão *IEEE 802.11*) e Bluetooth (Padrão
*Bluetooth SIG*) para que os objetos conectados sobre o qual temos interesse em
encontrar não necessitem de modificações para o fazermos.

# 3 - Justificativa

> *Nota do parecerista: Reescrever*
Na visão dos autores, promover o desenvolvimento local através de trabalhos
exemplo, treinamentos ou manuais é fundamental para a equiparação dos
desenvolvedores locais com as tecnologias e tendencias de mercado então
justificamos sua execução para que outras organizações possam encontrar novos
caminhos.

 Como a manipulação de RF é geralmente mais complicada em sistemas com
*hardwares* heterogênios

> *Economia em cada aparelho*

Escolhemos o sistema de antenas sensoras e dispositivos transmissores ao invés
do contrario (explicar com o detalhes o pq da escolha e falar o que é contrário)
para economia de harware no sentido de menos hardware em cada dispositivo e
levando em conta  a quantidade prevista de em média 5 dispositivos conectados
por pessoa e de que, com este sistema, estes dispositivos não precisariam de
sensores para localizar-se além de informações mais completas para o prédio.

> *Funcionamento por prédio*  
 -> *uma vez instalado qualquer quantidade de
devices é recebida, facil gerencia dentro do predio*  
 -> *beneficios para o admin do predio*  


# Objetivos

## Objetivos Gerais

> *Nota do parecerista: Este não é o objetivo do TCC do Marcelo Augusto
Cordeiro??*

Considerando características locais, propõem-se a construção de uma aplicação
para localizar contextualmente dispositivos dentro de um prédio piloto e avaliar
sua precisão.

Além desta aplicação, é objetivo definir o custo do projeto piloto incluindo
esforço de pesquisa assim como definir um custo para replicação deste
localizador contextual em outros prédios.

## Objetivos Específicos

-  Estabelecer o estado da arte sobre a desenvolvimento de aplicações IoT;
-  Identificar desafios locais para o desenvolvimento;
-  Identificar provedores de serviços, dispositivos e ferramentas para o
desenvolvimento;
-  Construir um protótipo de sala conectada virtualmente que identifique os
dispositivos conectados a rede que existem dentro nela através de conexões sem
fio;
-  Estimar o custo total do projeto piloto incluindo esforço de pesquisa;
-  Estimar o custo de replicação da aplicação em outros prédios.

> *Nota do parecerista: Na proposta do Marcelo, foi informado que o Luís
Henrique ficará responsável por todos os sensores, o que inclui sua construção,
posicionamento, configuração e programação dos gateways.*

# 4 - Método de Pesquisa

*Ambiente conciente*  

Abordagens para medir distâncias através de redes sem fio Wi-Fi
([bahillo2009ieee]) e Bluetooth já existem e, propor novas maneiras não é o foco
deste trabalho, utilizando essas técnicas propomos estabelecer uma rede de nós
sensores colaborativos fixos no ambiente onde deseja-se obter a localização dos
dispositivos. As informações de distância serão compartilhadas entre os nós para
maior precisão da estimativa de distância.

> Esta rede estará conectada a internet e proverá o serviço de localização

Mesmo com a grande quantidade de dispositivos já conectados são poucos os
documentos descrevendo boas práticas para concepção, construção e manutenção de
aplicações IoT, especialmente sobre os cuidados tomados quanto a segurança e
análise de custos para a implementação e manutenção.

Além disso, a falta de referências neste sentido é agravada quando considera-se
implementação no interior do estado de São Paulo visto que poucas são as
organizações atualizadas neste tema levando a uma falta enorme de conteúdo
escrito na linguagem local além de serviços e produtos disponíveis para
construção de uma plataforma completa e competitiva nesta região.

----------------------------

Utilizaremos prototipagem ágil semelhante ao desenvolvimento de um produto
utilizando a metodologia *Scrum* [James2016], executando iterações de uma semana
onde a cada iteração uma nova versão melhorada do produto completo (hardware,
software, documentação e resultados) será entregue.

Dentro de cada iteração as camadas da aplicação IoT serão escolhidas,
implementadas, justificadas e avaliadas sendo todo processo documentado. Como
resultado de cada iteração será gerado um relatório das mudanças a partir da
iteração anterior.


![Modelo das camadas][divisaoProjeto.png]  
Fonte: Marcelo Augusto Cordeiro

[divisaoProjeto.png]: latex/img/projeto.JPG

A Figura \ref{fig:projeto} apresenta a arquitetura simplificada de uma aplicação
IoT. Esta será modificada a cada iteração do projeto especialmente as camadas de
sensores, *gateway* e base de dados.

> *Nota do parecerista: Reescrever a metodologia....descrever detalhadamente as
atividades que deverão ser desenvolvidas*


# Cronograma


Devido a natureza ágil e iterativa da metodologia, o cronograma será dividido em
apenas três partes: Levantamento Bibliográfico Inicial, Desenvolvimento
Iterativo e Revisão Final. Estas partes serão distribuídas conforme a
Tabela~\ref{table:cronograma}.


Tabela 1 – Cronograma de Atividades Propostas

| Atividade							 	| 	Fev	 | 	Mar	 | 	Abr	 | 	Mai	 | 	Jun	 | 	Jul	 | 	Ago	 | 	Set	 | 	Out  |
| ------------------------------------- |:------:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| Levantamento Bibliográfico Inicial	| 	X	 | 	X	 | 	 	 | 	 	 | 	 	 | 	 	 | 	 	 | 	 	 | 	     |
| Desenvolvimento Iterativo				| 	 	 | 	X	 | 	X	 | 	X	 | 	X	 | 	X	 | 	X	 | 	X	 | 	     |
| Revisão Final							| 	 	 | 	 	 | 	 	 | 	 	 | 	 	 | 	 	 | 	 	 | 	X	 | 	X    |
Fonte: Produzido pelo autor

> *Nota do parecerista: A atividade ``Desenvolvimento Iterativo'' deve ser dividida em sub-atividades...*

-----------------------------------

> **Nossa solução**  


> Por exemplo, utilizando uma série de sensores Wi-Fi posicionados em pontos fixos
dentro de um prédio, com a triangulação do sinal é possível calcular a posição
de dispositivos conectados à rede Wi-Fi [SubPos].


[SubPos]:http://subpos.org/
[bahillo2009ieee]:http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=5073583

> *Marcelo*: Para oferecer uma posição confiável, é necessário que estes sensores
coletem e transmitam a força do sinal Wi-Fi em cada dispositivo com uma alta
frequência.




Utilizando como exemplo o prédio do Laboratório de Tecnologia da Informação
Aplicada (LTIA) da Faculdade de Ciências da Unesp de Bauru, em um dia comum, é
observado uma média de 30 dispositivos conectados à rede Wi-Fi.

Considerando um sensor que a cada 30 segundos colete 1 kB de dados de cada
dispositivo, por mês, seriam coletados mais de 2 GB de dados. Portanto, para
garantir um sistema escalável, é necessário a utilização de técnicas de Big Data
para armazenar e manipular esses dados. O melhor modo de se definir Big Data
ainda é discutido por pesquisadores, mas uma definição simples é a de que “se é
necessário se preocupar com o tamanho dos dados, então é Big Data.” (ESPOSITO,
2015, tradução nossa)



> % Entendemos que devido a natureza física e info-computacional das coisas
>  conectadas tanto sua localização e identificação na rede de comunicação
>  (endereço lógico, de internet, IPv6 ou URI) quanto sua localização e
>  identificação física (posicionamento global e relativo, identidade física) são
>  de igual importância.

> % Porém para os autores apenas a localização lógica foi bem resolvida, documentada
>  e padronizada pela ciência da computação pois sistemas de localização físicos,
>  apesar de existirem e funcionarem perfeitamente no dia-a-dia especialmente em
>  ambientes abertos, não são tão onipresentes quanto os lógicos nem trazem
>  contextualização de maneira tão simples.

>% Para exemplificar esta visão dos autores faremos uma comparação entre uma
>  localização no formato oferecido por um sistema de posicionamento global (GPS)
>  como o trio Latitude, Longitude e elevação com um endereço lógico na internet, o
>  endereço IPv6. Nesta camada é possível comparar o nível de abrangência dos dois
>  protocolos da mesma maneira que comparamos números.

> % Porém as similaridades tornam-se estreitas no próximo nível de abstração
>  considerando para endereço lógico uma URI (*Uniform Resource Identifier*)
>  com um DNS (*Domain Name System*) propriamente aplicado quando comparamos
>  a um endereço físico contendo País, Região, Cidade, Bairro, Rua, Número de rua,
>  número de repartição (apartamento, casa), identificação do cômodo (unitário,
>  atômico nesta especificação) e finalmente uma posição relativa dentro deste
>  cômodo cuja complexidade não diminui mesmo quando levamos em conta técnicas de
>  endereçamento como ZIP e CEP.

> % Para diminuição desta complexidade podemos abordar o problema fora da teoria de
>  informação com um ponto de vista geométrico utilizando uma posição GPS comum até
>  a fase de repartição (até onde GPS via satélite é eficiente) e dentro da
>  repartição (fora de alcance dos satélites) utilizar uma nova coordenada de
>  Direção e Distância a partir de um ponto fixo único desta repartição.