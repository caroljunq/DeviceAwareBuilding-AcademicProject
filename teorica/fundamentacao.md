
# Fundamentação teórica

> Base: Palavras chaves que descrevem o projeto, baseado em citações?

> HABILITANDO UM PRÉDIO A LOCALIZAR CONTEXTUALMENTE DISPOSITIVOS UTILIZANDO REDES SEM FIO

> Nesta seção apresentam-se conceitos, fundamentos e teorias que dão suporte
ao presente trabalho. Dentre eles, Computação em Nuvem, Balanceamento de Cargas
e Redes Neurais Artificiais.

Para conceituar, fundamentar e dar suporte teórico ao presente trabalho
apresentamos nesta seção os tópicos: Iot, localização contextual de dispositivos
e localização baseada em redes sem fio.

## Internet das coisas (*IoT*)

Uma das primeiras aplicações e definições de IoT foi feita por Kevin Ashton em
1999 para a *Procter & Gamble* (P&G) ([ASHTON, 2009]) e simultaneamente no
laboratório Auto-ID Labs no Instituto de Tecnologia de Massachusetts (MIT -
*Massachusetts Institute of Technology*) utilizando identificação por
radio-frequência (RFID - *radio-frequency identification*) ([Atzori et al,
2010]; [Mattern e Floerkemeier, 2010]) e desde então cresceu ultrapassando o
escopo da tecnologia RFID porém sempre com as premissas de "uma infraestrutura
global para a Sociedade da Informação, habilitando serviços avançados através da
interconexão de coisas (físicas e virtuais) baseadas em tecnologias, existentes
e evolutivas, de informação e comunicação" ([ITU 2012]) ([Wortmann, 2015]).

[ASHTON, 2009]:(<http://www.rfidjournal.com/articles/view?4986> "That 'Internet of Things' Thing")
[ASHTON, 2009](<http://www.rfidjournal.com/articles/view?4986> "That 'Internet of Things' Thing")

[Atzori et al, 2010]:(<http://www.sciencedirect.com/science/article/pii/S1389128610001568> "The internet of things: a survey")
[Atzori et al, 2010](<http://www.sciencedirect.com/science/article/pii/S1389128610001568> "The internet of things: a survey")

[Mattern e Floerkemeier, 2010]:(<http://www.vs.inf.ethz.ch/publ/papers/Internet-of-things.pdf> "From the Internet of Computers to the Internet of Things")
[Mattern e Floerkemeier, 2010](<http://www.vs.inf.ethz.ch/publ/papers/Internet-of-things.pdf> "From the Internet of Computers to the Internet of Things")

[ITU 2012]:(<http://handle.itu.int/11.1002/1000/11559> "Overview of the Internet of things")
[ITU 2012](<http://handle.itu.int/11.1002/1000/11559> "Overview of the Internet of things")

[Wortmann, 2015]:(<http://link.springer.com/article/10.1007%2Fs12599-015-0383-3> "Internet of Things: Technology and Value Added")
[Wortmann, 2015](<http://link.springer.com/article/10.1007%2Fs12599-015-0383-3> "Internet of Things: Technology and Value Added")

Hoje em dia, quase qualquer tecnologia de comunicação acessível a computadores
pode ser utilizada como meio de comunicação entre nós da IoT, tornando RFID mais
uma, porém de grande importância, tecnologia info-comunicacional a disposição
das coisas para sua conexão. Esta gama de tecnologias possibilita uma variedade
equivalente de coisas conectadas. Se a coisa pode usar de uma tecnologia de
conexão, considerando suas restrições de volume, custo e utilidade, muito
provavelmente vai fazê-lo gerando ao menos uma identidade virtual representando
seu objeto físico e seus atributos. Esta identidade virtual e atributos virtuais
serão expostos para todos indivíduos, humanos ou coisas, que lhe forem
convenientes de qualquer lugar do universo virtual, fazendo efetivamente parte da
internet.

## Localização contextual de dispositivos

Em ciência da computação, os termos *"Contexto"* e *"Consciência de Contexto"*
expressam uma ideia recente estudada nos campos de inteligência artifical e
ciência cognitiva desde 1991. O tema "Contexto" ainda é considerado atual e promissor a
ponto de mudar o cenário de negócios nos próximos 10 anos porém sem definição
simples. Tamanha é a falta de uma definição geral que realmente funcione para
casos reais que existe uma proposta de definir o termo utlizando uma nova
metodologia de pesquisa holística através de mineração e agrupamento de texto
advindo de publicações ciêntificas ([Pascalau, Nalepa, Kluza 2013]).

[Pascalau, Nalepa, Kluza 2013]:(<http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.672.5972> "Towards a Better Understanding of Context-Aware Applications")

[Pascalau, Nalepa, Kluza 2013](<http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.672.5972> "Towards a Better Understanding of Context-Aware Applications")

Mesmo sem uma definição permanente em vista, utilizaremos o que é considerado
estado da arte para o termo *"Contexto"* que foi introduzido por Dey e Abowd em
1999 ([Dey e Abowd, 1999]) e reforçado por Dey em 2000 ([Dey, 2000]):

[Dey, 2000]:(<http://www.cc.gatech.edu/fce/ctk/pubs/dey-thesis.pdf> "Providing architectural support for building context-aware applications")

[Dey, 2000](<http://www.cc.gatech.edu/fce/ctk/pubs/dey-thesis.pdf> "Providing architectural support for building context-aware applications")

> *"Contexto é qualquer informação que pode ser utilizada para caracterizar a
situação de uma entidade. Uma entidade é uma pessoa, lugar ou objeto que é
considerado relevante para a interação entre um usuário e uma aplicação,
incluindo o próprio usuário e a aplicação."*  
[Dey e Abowd, 1999] p. 3. Tradução Nossa.

[Dey e Abowd, 1999]:(<http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.150.4833> "Towards a Better Understanding of Context and Context-Awareness")
[Dey e Abowd, 1999](<http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.150.4833> "Towards a Better Understanding of Context and Context-Awareness")

### - Localização contextual

Das informações contextuais que uma aplicação de cliente móvel pode obter, a
localização é uma das mais importantes. Ajudar pessoas a navegar por mapas,
encontrar objetos e pessoas com os quais tem interesse de interagir é sem dúvida
uma boa meta a ser alcançada com a coleta da localização do cliente ([Bellavista
et al, 2008]).

Na categoria de Serviços Baseados em Localização (LBS - *Location-Based
Services*) existem duas gerações. A primeira orientada a conteúdo que falhou,
pois a informação de localização era armazenada pela rede, podendo até ser
vendida pelo provedor a terceiros, causando a sensação de Spam no usuário final
ao receber conteúdo desta provedora. Já na segunda geração, a posse da informação
foi movida para o cliente móvel, deixando a cargo do usuário escolher se ela seria
compartilhada e com quem. Esta mudança trouxe maior engajamento do usuário,
resultando numa maior aceitação dessa geração ([Bellavista et al, 2008]).

[Bellavista et al, 2008]:(<http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=4487093> "Location-Based Services: Back to the Future")
[Bellavista et al, 2008](<http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=4487093> "Location-Based Services: Back to the Future")

Ao contrário das técnicas atuais, neste trabalho os humanos ou tomadores
de decisão não estarão em posse do cliente móvel, e sim em posse do prédio.
Portanto, a mesma informação, sem degradação em sua importância, passará a ser
coletada e armazenada pelo provedor da rede como nos LBSs de primeira geração.
Esta decisão garante o foco no usuário uma vez que este mudou, antes ele detinha
um cliente móvel, agora ele detem múltiplos. Isso torna a detenção do todo (coisas
dentro do prédio) mais precioso do que o das partes (os clientes móveis).

Uma vez encontrada a localização de um dispositivo, metadados sobre o prédio são
mesclados formando um conjunto rico contextualmente do ponto de vista da aplicação IoT Prédio
como fornecedora principal dos dados para a internet e portanto seus usuários detentores.
Essa riqueza é garantida com metadados sobre o dispositivo (identificação, nome,
histórico, carecteristicas) e sobre o prédio (ex.: mapa, estrutura de salas, horário
de funcionamento, consumo energético, humanos responsáveis e lista de
equipamentos) que trazem possibilidades de extração de informação importantes para
os detentores deste prédio e seu conteúdo. Esta capacidade do prédio deve-se
pelo papel de coordenador de informações e controlador de meta-informações
semelhante ao Coordenador em uma aplicação na arquitetura
Modelo-Apresentação-Adaptador-Controlador-Coordenador (MPACC -
*Model-PresentationAdapter-Controller-Coordinator*) proposto por Román e
Campbell ([Román e Campbell 2001]).

[Román e Campbell 2001]:(<http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.408.8058> "A Model for Ubiquitous Applications")
[Román e Campbell 2001](<http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.408.8058> "A Model for Ubiquitous Applications")

### - Contexto de um dispositivo em um prédio

Para os metadados agregados à informação de posição pelo prédio, definimos que o
modelo de divulgação terá de conter além da posição do dispositivo: informação
sobre este (nome, histórico), informação da estrutura do prédio (mapa imagem,
mapa lógico, nome, localização global, endereço, etc), ligação entre a estrutura
do prédio e a localização do dispositivo (posição no mapa lógico) e informação
sobre o estado do prédio (horário de funcionamento, frequentadores, etc).

Este modelo visa prover fácil mineração e reutilização de informações por
terceiros após a implementação do projeto que é medida pela disponibilidade e
relacionamento das informações providas. Essa métrica também será utilizada para
avaliar o projeto final.

Este foco em reusabilidade vem da definição de Web Semantica (*Semantic Web*) e
de uma de suas realisadoras, a Ligação de Dados (*Linked Data*), que sugere o
uso de um formato padrão além de ser acessível e gerenciável pelas ferramentas
de exploração. Desta forma a Web de Dados (*Web of Data*) é construída opondo
uma simples coleção de dados [W3C, 2015].

[W3C, 2015]:(<https://www.w3.org/standards/semanticweb/data> "Data - W3C")
[W3C, 2015](<https://www.w3.org/standards/semanticweb/data> "Data - W3C")

## Localização baseada em redes sem fio

Para o sistema de posicionamento nos baseamos em técnicas de triângulação de
distâncias adquiridas com a medição de características eletromagnéticas (ex.:
potência de sinal) e características dos protocolos (ex.: Tempo de chegada) que
já foram explorados anteriormente ([Abusubaih et al, 2007], [Bahillo et al,
2009], [Feldmann et al, 2003]).

[Abusubaih et al, 2007]:(<http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=4668193> "A dual distance measurement scheme for indoor IEEE 802.11 wireless local area networks (2007) By Abusubaih, Murad and Rathke, Berthold and Wolisz, Adam")
[Abusubaih et al, 2007](<http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=4668193> "A dual distance measurement scheme for indoor IEEE 802.11 wireless local area networks (2007) By Abusubaih, Murad and Rathke, Berthold and Wolisz, Adam")


[Bahillo et al, 2009]:(<http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=5073583> "IEEE 802.11 Distance Estimation Based on RTS/CTS Two-Frame Exchange Mechanism (2009) By A. Bahillo and J. Prieto and S. Mazuelas and R. M. Lorenzo and J. Blas and P. Fernandez")
[Bahillo et al, 2009](<http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=5073583> "IEEE 802.11 Distance Estimation Based on RTS/CTS Two-Frame Exchange Mechanism (2009) By A. Bahillo and J. Prieto and S. Mazuelas and R. M. Lorenzo and J. Blas and P. Fernandez")

[Feldmann et al, 2003]:(<https://www.researchgate.net/publication/220719209_An_Indoor_Bluetooth-Based_Positioning_System_Concept_Implementation_and_Experimental_Evaluation> "An indoor Bluetooth-based positioning system: concept , Implementation and experimental evaluation (2003) By Feldmann, Silke; Kyamakya, Kyandoghere; Zapater, Ana; Lue, Zighuo")
[Feldmann et al, 2003](<https://www.researchgate.net/publication/220719209_An_Indoor_Bluetooth-Based_Positioning_System_Concept_Implementation_and_Experimental_Evaluation> "An indoor Bluetooth-based positioning system: concept , Implementation and experimental evaluation (2003) By Feldmann, Silke; Kyamakya, Kyandoghere; Zapater, Ana; Lue, Zighuo")

Portanto os sensores seguirão as especificações de *WiFi IEEE 802.11* ([Crow et
al, 1997]) e *Bluetooth low energy* (BLE) ([Hossain e Soh, 2007]).

[Crow et al, 1997]:(<http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=620533> "IEEE 802.11 Wireless Local Area Networks (1997) By Crow, B.P. and Widjaja, I. and Kim, L.G. and Sakai, P.T.")
[Crow et al, 1997](<http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=620533> "IEEE 802.11 Wireless Local Area Networks (1997) By Crow, B.P. and Widjaja, I. and Kim, L.G. and Sakai, P.T.")

[Hossain e Soh, 2007]:(<http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=853758> "A Comprehensive Study of Bluetooth Signal Parameters for Localization (2007) By Hossain, A. K. M. Mahtab and Soh, Wee-Seng")
[Hossain e Soh, 2007](<http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=853758> "A Comprehensive Study of Bluetooth Signal Parameters for Localization (2007) By Hossain, A. K. M. Mahtab and Soh, Wee-Seng")

Rpi como sensor
