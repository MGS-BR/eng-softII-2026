O contador está autenticado no sistema
O cliente já está cadastrado
Os documentos estão disponíveis para envio

Pós-condições:

Os documentos foram processados
Os dados foram extraídos e armazenados
Um lançamento contábil foi gerado (aprovado ou rejeitado)

Requisitos correlacionados: RF04, RF10, RF11, RF13, RF15, RF16

Variações tecnológicas:

Upload pode ser feito via seleção de arquivo ou arrastar e soltar
Processamento pode usar diferentes motores de IA
Visualização pode variar entre mobile e desktop

Questões em aberto:

Quais tipos de documentos terão prioridade no processamento?
O nível de confiança mínimo da IA será configurável?
 Fluxo principal:

1 O contador acessa a funcionalidade de envio de documentos
2 O contador seleciona o cliente
3 O contador seleciona o tipo de documento
4 O contador adiciona os arquivos (upload ou arrastar)
5 [EV] O sistema valida os arquivos (formato e tamanho)
6 O contador confirma o envio
7 [EV] O sistema envia os documentos para processamento
8 [EV] O Sistema de IA extrai os dados dos documentos
9 [EV] O sistema calcula o nível de confiança
10 O sistema exibe os dados extraídos
11 O contador revisa as informações
12 O contador aprova o lançamento
13 O sistema registra o lançamento contábil

 Tratamento de exceções:

2a. Cliente não selecionado
2a.1 O sistema solicita a seleção de um cliente
2a.2 Retorna ao passo 2

5a. Arquivo inválido (formato ou tamanho)
5a.1 O sistema informa erro no arquivo
5a.2 O contador remove ou substitui o arquivo
5a.3 Retorna ao passo 4

8a. Falha no processamento da IA
8a.1 O sistema informa erro no processamento
8a.2 O sistema permite nova tentativa
8a.3 Retorna ao passo 7

9a. Baixa confiança na extração
9a.1 O sistema alerta o contador
9a.2 O contador revisa manualmente os dados
9a.3 Retorna ao passo 11

12a. Contador rejeita o lançamento
12a.1 O sistema marca o lançamento como rejeitado
12a.2 O sistema armazena o documento sem contabilização

4a. Nenhum arquivo selecionado
4a.1 O sistema solicita inclusão de pelo menos um arquivo
4a.2 Retorna ao passo 4
