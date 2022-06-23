# Protocolo HTTP

HTTP = Hyper Text Transfer Protocolo, ou seja, é a comunicação entre o cliente e o servidor. 

É um protocolo sem estado (Stateless), ou seja, ele responde ao pedido requerido naquele momento, e não de estados anteriores.

- Browser = Implementa o cliente HTTP
- Servidor = Host dos objetos web

Mensagens = Cliente (Request); Servidor (Response)

Resquest | Response
---------|---------
Texto em ASCII | Status Line - Versão do protocolo, status code e o status da mensagem
Request Line - Método HTTP (ação) e versão do protocolo | Header Line - Conexão encerrada, dados da mensagem (data, servidor, última modificação e tamanho da mensagem), content-type (tipo de dado) 
Header Line - URL (Host que foi enviado), tipo de conexão não persistente, agente que realizou o request e preferência do cliente (se não houver, anvia padrão) | 
Enitity body (parte de busca) |
Método GET 90% |

## - Métodos: 

GET = solicita um recurso ***MÉTODO SEGURO***

HEAD = GET sem corpo de resposta (metadados) ***MÉTODO SEGURO***

POST = submete dados de um recurso, servidor aceita todos os dados do pacote 

PUT = envia um novo estado para esse corpo de dados, substituindo o estado existente 

DELETE = remove um recurso 

TRACE = verifica a cadeia de requerimento, como dignóstico e testes

OPTION = verifica os recursos atrelados ao servidor, parte de configuração ***MÉTODO SEGURO***

CONNECT = unifica um recurso de ponta a ponta, estabelecendo uma conexão segura com o recurso

PATCH = (RFC 5789) é uma modificação parcial do recurso

*P.S.: Método Seguro não ocorre alteração de dados.* 

## - Status Code do Response:

200 OK = Request bem sucedido e objeto enviado

301 Moved Permanently = Objeto realocado e nova URL no campo de envio

400 Bad Request = Resposta genérica, servidor não encontrou a mensagem

404 Not Found = Documento solicitado é inexistente

505 HTTP Version Not Supported = Versão do protocolo não suportada pelo servidor

 ## Cookie

Esses cookies são referenciados pela RFC 6265, são para rastreanmento e identificação dos usuários, ou seja, para restrição de acesso ou fornecimento de funções, por exemplo, publicidade. 

### Cookies - Componentes 

Tipos | Componentes
------|------------
Cookie header line | Request e Response message 
Cookie file | Mantido no cliente (gerenciado pelo navegador - Browser) e servidor
Banco de Dados Back-end | Web site

## Conceitos Básicos de Segurança

- Criptografia por Chave

Exemplo: Vooê te um arquivo que precisa ser restrito a leitura, e você precisa que os dados desse arquivo sejam ilegíveis para outras pessoas.Existe então um código que desordena esses dados para que somente quem possue a chave consiga ler. Nesse caso, esse arquivo foi criptografado por chave, que foi o código que desordenou os dados, e só quem possui a chave (código), consegue acessar. 

Chave assimétrica =  Chave privada (assinatura) e chave pública (verificação de autenticidade). 

Chave simétrica = Chave única privada: 

- Cifra de Cesar, é uma chave que funciona de forma a substituição da letra pela k-ésima (terceira letra posterior a letra inicial) do alfabeto, tendo uma rotatividade da chave. 

- Cifra de fluxo = Utilização por sequência de bits pseudo-aleatório, com mapeamento de 1 para 1.

- Cifra por bloco = Utilizada por protocolos de segurança na internet, SSL, PGP e Ipsec. Utiliza bloco de bits, mapeamento de 1 bloco por 1 bloco com 3 bits cada. 

Certificação de chave pública, nada mais é do que comprovar sua autenticidade através da Entidade Certificadora. Essa entidade deve ser de alta confiabilidade. 

# Protocolo SSL

SSL = Secure Socket Layer, é um protocolo de segurança para conexões TCP, visando a confiabilidade (não haja leitura), integridade (ão haja mudança) e autencidade end-point (e ambos os lados sejam fidedignos) dos dados de ponta a ponta.

## Operação - Fases 

- 1ª fase: Handshake = Estabelecimento de conexão TCP, ou seja, trocas de comunicação em três vias. 

- 2ª fase: Key Derivation = Verificação de autencidade, em que há o envio da Master Secret Key (EMS). 

- 3ª fase: Data Transfer = Tranferência efetiva de dados após a codificação. Adicionando a verificação da integridade da mensagem. 

# HTTPS

É a segurança de comunicação HTTP utilizando o protocolo da SSL. 

# API

API = Application Programming Interface, é o intermédio entre o usuário e o servidor ou hardware. 

## Propriedades da API 

- Acesso de dados: A API irá requerir os dados do usuário, junto a um código que executa o arquivo dentro do servido do banco de dados. Assim, será devolvido a busca para a API quando finalizada e a API printará os resultados para o usuário. 

- Esconder complexidade

- Estender funcionalidades: Comunicação emtre software e hardware. É a agregação de funcionalidades de plataformas distintas, seja hardware ou software. Havendo também uma comunicação entre aplicativos. 

- Segurança: Protocolos de segurança devem ser comtemplados ao projeto usando uma API se tratar de dados sensíveis. 

# Padrão REST 

- HTTP = Comunicação entre API e Sistema 
- Regras: Arquitetura REST 

## Modelo 

CLIENT-SERVER = Princípio da separação, em que o lado do cliente se preocupa com a interface e o lado servidor se preocupa com o armazenamento. 

STATELESS = Protocolo, o request tem que fornecer entendimento completo ao servidor do que o cliente precisa. Existe um Tradeoff (escolha), há muito repetição de dado, pode ocasionar uma sobrecarga por interação (per-interaction overhead), havendo a performance da rede x propriedades do REST.

CACHE = Aumenta a eficiência da rede, contrapondo o Tradeoff, reduzindo a sobrecarga por interação, fazendo as requests serem etiquetadas (Label Requests), como cacheable ou non-cacheable. 

UNIFORM INTERFACE = Define a interface uniforme entre os componentes, aplicando o pricípio da eng. de software fica simplificado. 

DATA ELEMENT | MODERN WEB EXEMPLES
-------------|--------------------
Resource identifier | URL, URN 
Representation | HTML, document, JPEG image
Representation metadata | Media typo, last-modified time
Resource metadata | Source link, alternates, vary
Control data | If-modified-since, cache-control

LAYERED SYSTEM = Sistema em camadas, sendo hierárquico, tendo uma melhor proteção de dados. 

CODE ON DEMAND = É opcional, e permite que as funcionalidade dos clientes sejam extendidas em applets ou scripts. 

# API - HTTP JAVA

## Pacote HTTP 

- HttpClient = Classe que define o cliente HTTP, que efetivamente cria o cliente. Usando o .newBuilder(), que é responsável pela configuração e estado do cliente. E o .newHttpClient(), que cria um nome cliente HTTP e é imutável. 

- HttpRequest = Classe de solicitações e utilização de métodos, realizando as requesições. É criada a partir do builder, e é imautável, usando os métodos .GET(), .POST(), e .HEAD().

- HttpResponse = Resultdo da solicitação HTTP, é criada a partir do evio de uma solicitaçãodo clientes, sedo então, criada indiretamente. Usando o método HttpClient.send(). Podendo ser Sincrona, em que os dados chegam e ordem para o outro lado. ou sendo Assíncrona, em que é enviada de forma desordenada, mas assim que chega na outra ponta, é reordenada novamente. 