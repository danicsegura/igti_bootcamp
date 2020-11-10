# 1. ler input do usuário o nome do cliente e pesquisar na lista clientes (até que seja digitado um nome existente)
# poderá ser buscado por somente parte do nome
# caso encontrar: mostrar o primeiro nome encontrado
# caso não: 'Não encontrei esse nome.'
# somente passar para o próximo item se algum cliente for encontrado

# 2. pedir a lista de produtos e suas quantidades do usuário
# inclusão deverá ser terminada quando for incluído um produto vazio (tecla enter)

# 3. calcular:
  # imposto para cada item: 10% do valor do item multiplicado pela quantidade deste item
  # total do item = (item*quantidade)+imposto
  # total da nota fiscal

# 4. fazer um relatório com o layout abaixo:
# ===========================================
# Nota fiscal
# Cliente: Maria e Fátima
# Itens comprados
# Computador - Quantidade: 1 - Valor do imposto: R$100.05 - Valor total: R$1100.55
# Mouse - Quantidade: 2 - Valor do imposto: R$12.01 - Valor total: R$264.22
# Total da Nota: R$1364,77
# Volte Sempre!
# ===========================================


# Funções
def ler_nome_cliente(clientes):
  indice_cliente = -1

  while (indice_cliente == -1):
    nome_cliente = input('Digite o nome do cliente: ')
    while (not nome_cliente.isalpha()):
      nome_cliente = input('O nome não pode conter caracteres especiais ou números. Tente novamente: ')

    # encontrar o índice do cliente inserido na lista clientes
    for i,cliente in enumerate(clientes):
      if (nome_cliente.upper() in cliente.upper()):
        print(cliente)
        indice_cliente = i
        break
    if (indice_cliente == -1):
      print('Não encontrei esse nome.')
  
  return indice_cliente

def processar_compra(itens_comprados,quantidades_itens):
  item_compra = ler_item_compra()

  if (item_compra == -1):
    # return -1 (item_compra)
    return -1

  itens_comprados.append(produtos[item_compra])
  
  quantidade_compra = ler_quantidade()
  quantidades_itens.append(quantidade_compra)

  return item_compra

def ler_item_compra():
  produto_compra = input('Insira o nome do produto comprado: ')

  indice = -1

  if produto_compra == '':
    return -1;

  for i,produto in enumerate(produtos):
    if (produto_compra.upper() in produtos[i]['nome'].upper()):
      indice = i
      break
  return indice
  
def ler_quantidade():
  quantidade_compra = input('Digite a quantidade comprada deste produto: ')
  while (not quantidade_compra.isdigit()):
    quantidade_compra = input('A quantidade deve ser um número. Tente novamente.')
  return quantidade_compra

def calcular_imposto(item_compra, itens_comprados, quantidades_itens):
  # item_compra = indice do item em produtos
  # quantidades_itens = lista de preços na mesma ordem

  for i,produto in enumerate(itens_comprados):
    quantidades_itens[i] = float(quantidades_itens[i])
    imposto = quantidades_itens[i] * (itens_comprados[i]['preco'] * 0.1)
    preco_total_item = itens_comprados[i]['preco'] + imposto
    imposto_itens.append(imposto)
    precos_totais.append(preco_total_item)


  # para sair do while loop
  return imposto_itens, precos_totais

def calcular_soma_total(precos_totais):
  soma = 0
  for preco in precos_totais:
    soma += preco
  
  return soma

# Main
clientes = ['Marcelo',"Joana D'arc",'Maria de Fátima']
produtos = [{'nome':'computador', 'preco':1000.50}, {'nome':'mouse', 'preco':120.10},{'nome':'Monitor LCD', 'preco':999.99}]
itens_comprados = []
quantidades_itens = []
imposto_itens = []
precos_totais = []

# se a função ler_nome_cliente retornar True, vamos a proxima etapa
# ou seja, se o cliente for encontrado no sistema, prosseguir
indice_cliente = ler_nome_cliente(clientes)
if (indice_cliente != -1):
  item_compra = processar_compra(itens_comprados,quantidades_itens)
  # quando nada é inserido pelo usuário e só aperta ENTER, retorna -1
  while item_compra != -1:
    item_compra = processar_compra(itens_comprados,quantidades_itens)
  
  imposto_itens, precos_totais = calcular_imposto(item_compra, itens_comprados, quantidades_itens)
  soma_total = calcular_soma_total(precos_totais)

  # imprime relatório
  print('===========================================')
  print('Nota fiscal')
  print('Cliente: {}'.format(clientes[indice_cliente]))
  print('Itens comprados:')
  for i,item in enumerate(itens_comprados):
    # {:.2f} em valor do imposto e valor total >>> é para limitar somente exibir duas casas após a vírgula
    print('{} - Quantidade: {} - Valor do imposto: R${:.2f} - Valor total: R${:.2f}'.format(itens_comprados[i]['nome'].capitalize(), quantidades_itens[i], imposto_itens[i], precos_totais[i]))
  print('Total da nota: R${:.2f}'.format(soma_total))
  print('Volte sempre!')
  print('===========================================')
