# [Curso de Python: crie a sua primeira aplicação](https://cursos.alura.com.br/course/python-crie-sua-primeira-aplicacao)
Faça esse curso de Python web e:
- Crie um projeto em Python usando o VSCode
- Descubra o fluxo de uma aplicação com o uso de condicionais e laços de repetição
- Aprenda a utilizar blocos de controle de execução try-except
- Crie funções para mostrar o menu principal e registrar restaurantes em listas e dicionários

# 1. Manipulação de Strings: O que aprendemos?
- Exploramos o uso da função `print()` e sua sintaxe e recursos, que oferecem diversas maneiras de formatar e exibir mensagens;
- Aprendemos como utilizar a função `input()` para receber uma informação do usuário e como armazenar ela para utilizarmos no nosso código;
- Iniciamos a construção do primeiro programa na linguagem Python, com a criação do ‘Hello World’ para testarmos a função print, seguido da criação de um menu de opções para nosso serviço de cadastro de restaurantes.

## Código
```py
print('Sabor Express\n')

print('1. Cadastrar restaurante')
print('2. Listar restaurante')
print('3. Ativar restaurante')
print('4. Sair\n')

opcao_escolhida = input('Escolha uma opção: ')
print(f'Você escolheu a opção {opcao_escolhida}')
```
## Para saber mais: The Zen of Python
Ao ingressar no mundo da programação, é fácil se perder em meio a diferentes abordagens e práticas. É nesse momento que a **Filosofia do Python** se revela como um guia fundamental para os desenvolvedores novatos.

Escrita por Tim Peters, **The Zen of Python** remete a um conjunto de princípios que oferece uma abordagem equilibrada e simplificada para escrever código em Python, expressando diretrizes de design de forma concisa, semelhante a um poema ou aforismo.

Apesar de não ser uma forma tradicional de poesia, o **The Zen of Python** reflete a filosofia e é considerado um guia informal de boas práticas de programação para a linguagem. Ao seguir esses princípios, pessoas devs cultivam padrões de qualidade desde o início, integrando-se a uma comunidade que valoriza colaboração e transparência, fortalecendo o compromisso com projetos de alta qualidade.

Podemos ver sua versão original em inglês:

```
Beautiful is better than ugly.\
Explicit is better than implicit.\
Simple is better than complex.\
Complex is better than complicated.\
Flat is better than nested.\
Sparse is better than dense.\
Readability counts.\
Special cases aren't special enough to break the rules.\
Although practicality beats purity.\
Errors should never pass silently.\
Unless explicitly silenced.\
In the face of ambiguity, refuse the temptation to guess.\
There should be one-- and preferably only one --obvious way to do it.\
Although that way may not be obvious at first unless you're Dutch.\
Now is better than never.\
Although never is often better than right now.\
If the implementation is hard to explain, it's a bad idea.\
If the implementation is easy to explain, it may be a good idea.\
Namespaces are one honking great idea -- let's do more of those!\
```

Ou sua versão traduzida para o português:

```
Bonito é melhor que feio.\
Explícito é melhor que implícito.\
Simples é melhor que complexo.\
Complexo é melhor que complicado.\
Plano é melhor que aninhado.\
Esparso é melhor que denso.\
Legibilidade conta.\
Casos especiais não são especiais o bastante para quebrar as regras.\
Embora praticidade vença a pureza.\
Erros nunca devem passar silenciosamente.\
A menos que sejam explicitamente silenciados.\
Diante da ambiguidade, recuse a tentação de adivinhar.\
Deveria haver uma — e preferencialmente só uma — maneira óbvia de fazer algo.\
Embora essa maneira possa não ser óbvia a princípio a menos que você seja holandês.\
Agora é melhor que nunca.\
Embora nunca seja frequentemente melhor que agora mesmo.\
Se a implementação é difícil de explicar, é uma má ideia.\
Se a implementação é fácil de explicar, pode ser uma boa ideia.\
Namespaces são uma grande ideia — vamos fazer mais dessas!\
```

Para conseguir acessar esse poema sempre que quiser, basta acessar o terminal interativo do python e utilizar o comando:
```py
import this
```

Ao adotar as boas práticas indicadas pelo **The Zen of Python**, as pessoas desenvolvedoras não apenas melhoram a qualidade do código, mas também facilitam a colaboração em projetos, tornando o código mais acessível para outros programadores. A clareza e simplicidade promovidas por essas diretrizes não são apenas estéticas como também têm implicações profundas na manutenção, extensão e compreensão do código ao longo do tempo.

---

# 2. Módulos e funções: O que aprendemos?
- Exploramos o conceito de condicionais if-else e compreendemos a importância do seu uso para estabelecer o funcionamento do nosso código de acordo com uma condição;
- Compreendemos a importância de utilizar funções para organizar e melhorar o funcionamento de nosso projeto;
- Entendemos como podemos aproveitar funções já criadas através do uso do import de um módulo para limpar nosso terminal a fim de melhorar a visualização das informações;
- Aprendemos o conceito de casting para indicar o tipo de uma variável ao receber uma informação do usuário, melhorando a segurança e eficácia do nosso código.
## Código
```py
import os

def exibir_nome_do_programa():
    print('Sabor Express\n')

def exibir_opcoes():
    print('1. Cadastrar restaurante')
    print('2. Listar restaurante')
    print('3. Ativar restaurante')
    print('4. Sair\n')

def finalizar_app():
    os.system('cls')
    # os.system('clear') # Mac
    print('Finalizando o app')

def escolher_opcao():
    opcao_escolhida = int(input('Escolha uma opção: '))
    # opcao_escolhida = int(opcao_escolhida)
    
    if opcao_escolhida == 1:
        print('Cadastrar restaurante')
    elif opcao_escolhida == 2:
        print('Listar restaurante')
    elif opcao_escolhida == 3:
        print('Ativar restaurante')
    else:
        finalizar_app()

def main():
    exibir_nome_do_programa()
    exibir_opcoes()
    escolher_opcao()

if __name__ == '__main__':
    main()
```

## Para saber mais: instrução match
Ao explorarmos as instruções `if else` percebemos que elas são uma poderosa e fundamental construção da linguagem, que nos permite controlar o fluxo do código com base em condições lógicas que determinamos de acordo com a necessidade de nosso projeto.

Com o surgimento de novas versões do Python, a linguagem de programação continua a evoluir e se aprimorar, trazendo consigo uma variedade de novas funcionalidades que enriquecem a experiência de desenvolvimento. Essas inovações não apenas aprimoram a eficiência e a legibilidade do código, mas também oferecem aos desenvolvedores ferramentas mais poderosas e expressivas para lidar com desafios diversos.

Dentre as funcionalidades mais recentes, destaca-se a introdução da instrução `match` no Python 3.10, oferecendo uma abordagem mais elegante para a correspondência de padrões em dados. Essa adição não apenas simplifica a lógica do código, mas também proporciona uma alternativa expressiva e legível às construções tradicionais de controle de fluxo, como `if elif else`, que são necessários para adaptar o comportamento do programa, como vimos anteriormente.

A principal finalidade da instrução `match` é simplificar a lógica de código ao facilitar o trabalho com diferentes padrões de dados. Isso pode tornar o código mais legível e conciso em situações onde uma cadeia de `if elif else `pode se tornar complicada e difícil de manter.

### Sintaxe do Match
Durante o projeto, fizemos uma cadeia de condicionais em que cada uma indicava uma opção do nosso aplicativo, como adicionar restaurante, listar restaurantes, ativar restaurante e finalizar o app, além de colocarmos uma condicional para caso a opção informada não fosse válida (através do uso do `else`).

Utilizando as instruções `if elif` else tivemos esse resultado:
```py
opcao_escolhida = int(input('Escolha uma opção: '))
if opcao_escolhida == 1:
    print('Adicionar restaurante')
elif opcao_escolhida == 2:
    print('Listar restaurantes')
elif opcao_escolhida == 3:
    print('Ativar restaurante')
elif opcao_escolhida == 4:
    print('Finalizar app')
else:
    print('Opção inválida!')
```

Se decidirmos utilizar a instrução `match` nesse caso, obteríamos o seguinte resultado:
```py
opcao_escolhida = int(input('Escolha uma opção: '))
match opcao_escolhida:
    case 1:
        print('Adicionar restaurante')
    case 2:
        print('Listar restaurantes')
    case 3:
        print('Ativar restaurante')
    case 4:
        print('Finalizar app')
    case _:
        print('Opção inválida!')
```

Perceba que recebemos a variável `opção_escolhida` como parâmetro da instrução match e será feito um comparativo com todos os valores determinados pelos blocos de case, e no final temos uma instrução `case _`, que é um padrão curinga, que corresponde a qualquer valor que não tenha sido correspondido pelos casos anteriores, ou seja, equivalente ao `else` da condicional anterior.

Tendo esse exemplo, podemos entender a sintaxe padrão do `match`. Dentro de um bloco `match`, você pode utilizar a instrução `case` para definir padrões específicos que serão comparados com a expressão que está sendo correspondida.

A estrutura básica é a seguinte:
```py
match expressão:
    case padrão_1:
        # Código a ser executado se expressão corresponder a padrão_1
    case padrão_2:
        # Código a ser executado se expressão corresponder a padrão_2
    # ... outros casos ...
    case _:
        # Código a ser executado se nenhum dos padrões anteriores corresponder. Isso é útil para tratar casos não específicos.
```
### Qual instrução devo usar?
O `if` nos proporciona uma maneira eficaz de tomar decisões simples ou complexas em nosso código, adaptando o comportamento do programa de acordo com as circunstâncias determinadas. Ao usar `match`, podemos simplificar a lógica do código em situações que envolvem múltiplos padrões complexos. Ela oferece uma estrutura mais legível, especialmente quando temos diversos casos a serem tratados.

Podemos ver na tabela a seguir quando podemos utilizar cada uma dessas instruções, de acordo com suas vantagens:

<table><thead><tr><th><strong>Vantagens da Instrução <code>match</code></strong></th><th><strong>Vantagens da Estrutura <code>if</code></strong></th></tr></thead><tbody><tr><td>Lidar com condições complexas e múltiplos padrões de maneira mais intuitiva.</td><td>Implementação clássica e amplamente conhecida.</td></tr><tr><td>Sintaxe concisa melhora a legibilidade do código, especialmente em casos complexos.</td><td>Amplamente suportada em todas as versões do Python.</td></tr><tr><td>Permite desestruturação direta, evitando repetição excessiva de variáveis.</td><td>Estrutura simples e direta para lógica condicional básica.</td></tr><tr><td>Adiciona expressividade ao código, especialmente em situações de correspondência de padrões.</td><td>Pode ser mais intuitiva para devs familiarizados com estruturas de controle convencionais.</td></tr></tbody></table>

No geral, tanto o `if` quanto o `match` são ferramentas poderosas à disposição de pessoas desenvolvedoras de Python. A escolha entre elas depende das necessidades específicas do seu código e das preferências da pessoa que está a desenvolver o código. A instrução `match` oferece uma nova abordagem elegante para a correspondência de padrões, abrindo novas possibilidades e aprimorando a expressividade do código.

Experimente ambas as opções e escolha aquela que melhor se alinha com o seu estilo de programação e os requisitos do projeto.

Para saber mais sobre a instrução `match`, acesse a documentação do python que aborda esse tema:

- [Instrução Match](https://docs.python.org/pt-br/3/tutorial/controlflow.html#match-statements)

---

# 3. Lista, laços e exceções: O que aprendemos?
- Aprendemos a abordagem de utilizar o conjunto lista para armazenar diversos valores de um restaurante dentro de uma variável para organizar e manipular um conjunto de dados de forma mais dinâmica e simplificada;
- Compreendemos a importância de validar as informações que estamos recebendo do usuário através do bloco try except para capturar possíveis erros ao invés de travar o funcionamento de nosso projeto;
- Exploramos o uso do bloco de repetição for e entendemos a necessidade de seu uso para iterar de maneira eficaz uma sequência de dados e manter nosso código legível e de fácil manutenção.

## Código
```py
import os

restaurantes = ['Pizza', 'Sushi']

def exibir_nome_do_programa():
    print('Sabor Express')

def exibir_opcoes():
    print('1. Cadastrar restaurante')
    print('2. Listar restaurante')
    print('3. Ativar restaurante')
    print('4. Sair\n')

def finalizar_app():
    exibir_subtitulo('Finalizando o app...')

def voltar_ao_menu_principal():
    input('\nDigite uma tecla para voltar ao menu principal... ')
    main()

def opcao_invalida():
    print('Opcão inválida!\n')
    voltar_ao_menu_principal()

def exibir_subtitulo(texto):
    os.system('cls')
    print(texto)

def cadastrar_novo_restaurante():
    exibir_subtitulo('Cadastro de novos restaurantes...')

    nome_do_restaurante = input('Digite o nome do restaurante que deseja cadastrar: ')
    restaurantes.append(nome_do_restaurante)

    print(f'O restaurante {nome_do_restaurante} foi cadastrado com sucesso!')

    voltar_ao_menu_principal()

def listar_restaurantes():
    exibir_subtitulo('Listando os restaurantes cadastrados...')

    for restaurante in restaurantes:
        print(f'.{restaurante}')

    voltar_ao_menu_principal()

def escolher_opcao():
    try:
        opcao_escolhida = int(input('Escolha uma opção: '))
        # opcao_escolhida = int(opcao_escolhida)
        
        if opcao_escolhida == 1:
            cadastrar_novo_restaurante()
        elif opcao_escolhida == 2:
            listar_restaurantes()
        elif opcao_escolhida == 3:
            print('Ativar restaurante')
        elif opcao_escolhida == 4:
            finalizar_app()
        else:
            opcao_invalida()
    except:
        opcao_invalida()

def main():
    os.system('cls')
    exibir_nome_do_programa()
    exibir_opcoes()
    escolher_opcao()

if __name__ == '__main__':
    main()
```

## Para saber mais: Tuplas vs Listas
As **tuplas** são estruturas de dados que nos permitem armazenar elementos de maneira ordenada e sequencial, assim como as listas. Dessa forma, ambas mantêm a ordem dos elementos e oferecem índices para acessar esses valores.

Contudo, existem diferenças fundamentais entre tuplas e listas que as tornam adequadas para diferentes situações.

Vamos entender como cada uma se comporta e quais são os cenários que devemos escolher cada tipo de estrutura:

### Sintaxe:
O primeiro ponto que diferencia esses dois arranjos é a sintaxe de cada um. Como vimos, as listas são definidas utilizando colchetes `[ ]`, enquanto as tuplas são definidas utilizando parênteses `( )`, como mostra o exemplo a seguir:
```py
lista = [1,’olá mundo’,True,9.7]
tupla = (1,’olá mundo’,True,9.7)
```

### Mutabilidade:
A maior diferença entre essas duas configurações são suas propriedades de mutabilidade!

As listas são estruturas mutáveis, o que significa que é possível modificar seus elementos, adicionar novos itens ou remover existentes após a criação da lista, podendo inclusive utilizar funções próprias para isso como `append()`, `remove()`, `pop()`, e `insert()`.

Ao contrário das listas, tuplas são imutáveis. Uma vez que uma tupla é criada, seus elementos não podem ser alterados, adicionados ou removidos.

### Desempenho:
Devido à sua imutabilidade, as tuplas têm um desempenho melhor do que listas para algumas operações. Elas são mais eficientes em termos de espaço e processamento em determinados cenários.

Sendo assim, listas podem ser menos eficientes em termos de desempenho para operações específicas, especialmente quando se trata de manipulação de grandes conjuntos de dados, devido à sua mutabilidade.

### Quando devo utilizar cada estrutura?
As listas são ideais quando você precisa de uma coleção de elementos que pode ser modificada ao longo do tempo. Por exemplo, ao criar uma lista de tarefas que pode ser atualizada com novos itens ou marcada como concluída.

Além disso, se você precisa adicionar, remover ou modificar elementos com frequência, as listas oferecem métodos próprios convenientes, como mencionado anteriormente. Podemos ver isso com uma lista de compras, como mostrado no código a seguir:
```py
# Criando uma lista de compras
lista_de_compras = ["Maçã", "Banana", "Leite", "Pão", "Queijo"]

# Adicionando um item à lista
lista_de_compras.append("Ovos")

# Removendo um item da lista
lista_de_compras.remove("Banana")

# Exibindo a lista
print("Lista de Compras:")
for item in lista_de_compras:
    print("- " + item)
```
Já as tuplas são apropriadas quando se deseja garantir que os elementos não sejam alterados após a criação. Isso é útil para dados que devem permanecer constantes ao longo do tempo. Como as tuplas são imutáveis, elas podem ter um desempenho ligeiramente melhor em operações de leitura e acesso a elementos. Isso também as tornam adequadas para situações em que a eficiência é crucial.

Podemos ver um exemplo de uma tupla que armazena as coordenadas geográficas de uma localização específica, que são dados imutáveis que queremos ter acesso, como mostrado a seguir:
```py
# Definindo uma tupla de coordenadas geográficas
coordenadas_gps = (40.7128, -74.0060)

# Exibindo as coordenadas
print("Coordenadas GPS:")
print("Latitude:", coordenadas_gps[0])
print("Longitude:", coordenadas_gps[1])
```
Lembre-se de sempre avaliar as condições de seu projeto e escolher qual das duas estruturas é mais adequada para cada situação.

Quer saber um pouco mais sobre Tuplas no Python? Recomendamos as seguintes leituras:
- [Documentação Python - Tuplas;](https://docs.python.org/pt-br/3/tutorial/datastructures.html#tuples-and-sequences)
- [Tupla no Python: o que é, como criar e manipular e suas diferenças com as Listas.](https://www.alura.com.br/artigos/conhecendo-as-tuplas-no-python)

## Para saber mais: While
Imagine que estamos desenvolvendo um programa para uma aplicação de entrada de dados em que precisamos coletar informações do usuário. Uma das informações que precisamos é um número positivo, e queremos garantir que o usuário forneça um valor válido.

Nosso desafio é criar um código que solicite ao usuário que insira um número positivo. No entanto, como não podemos confiar no usuário para fornecer um valor válido na primeira tentativa, precisamos criar uma lógica que permita solicitar novamente até que o usuário finalmente insira um número válido.

Como aprendemos, podemos utilizar a estrutura de repetição `for` para solicitar esse valor até que essa condição seja satisfeita, como mostrado no código a seguir:
```py
numero = -1
for _ in range(3):  # Supondo um número máximo de tentativas (3) arbitrário
    numero = int(input("Digite um número positivo: "))
    if numero > 0:
        break

print("Você digitou:", numero)
```

Perceba que, para criar esse loop, precisamos definir um número arbitrário de tentativas para que o usuário inserisse esse valor. Isso acontece porque o loop `for` é utilizado quando se conhece previamente o número de iterações que devem ser realizadas.

Contudo, nós queremos que o usuário digite diversas vezes até que ele coloque um valor positivo e não tenha nenhuma limitação.

Neste caso, a estrutura `for` não consegue satisfazer o que desejamos para nosso código. E agora? O Python tem outra estrutura que podemos utilizar? A resposta é sim!

Essa linguagem oferece duas estruturas de controle de fluxo fundamentais para a execução de blocos de repetição: o **for** e o **while**. Ambas são utilizadas para a implementação de loops, permitindo que um bloco de código seja executado repetidamente enquanto determinadas condições são atendidas.

Como vimos, o loop `for` é utilizado quando se conhece previamente o número de iterações que devem ser realizadas. Ele é especialmente eficaz ao percorrer elementos em sequências, como listas, tuplas, strings ou ranges.

O loop `while`, diferente do `for`, é utilizado quando o número de iterações não é conhecido de antemão, mas ainda assim depende de uma condição específica para manter o bloco de código em repetição. Ele continua a executar o bloco de código enquanto a condição fornecida for avaliada como verdadeira.

A sintaxe do loop `while` é a seguinte:
```py
while condição:
    # Bloco de código a ser repetido
```

O bloco de código dentro do `while` continuará a ser executado até que a condição se torne falsa, ou seja, ele apenas será executado quando a condição assumir o valor booleano de `true`. Isso significa que é essencial e necessário garantir que a condição eventualmente se torne falsa para evitar um loop infinito em seu projeto.

Então podemos adaptar nosso projeto anterior para utilizar o while ao invés do for, como vemos no código a seguir:
```py
numero = -1
while numero <= 0:
    numero = int(input("Digite um número positivo: "))

print("Você digitou:", numero)
```

Enquanto o número digitado for menor ou igual a zero, o programa continuará pedindo ao usuário que insira um número positivo. Quando o usuário finalmente fornecer um número positivo, o loop `while` será encerrado e o programa exibirá o número digitado.

Sendo assim, esse é um cenário em que um loop `while` é mais apropriado, pois não sabemos com antecedência quantas vezes precisaremos solicitar ao usuário que insira um número.

Ou seja, a escolha entre `for` e `while` dependerá da natureza específica do problema que você está resolvendo. Entender as nuances e aplicar a estrutura de controle de fluxo mais apropriada contribuirá para um código mais claro e eficiente a depender do seu projeto.

Quer saber um pouco mais sobre while no Python? Recomendamos a seguinte leitura:
- [Documentação Python - While](https://docs.python.org/3/reference/compound_stmts.html#the-while-statement)

---

# 4. Dicionários: O que aprendemos?
- Exploramos o conceito de dicionários e compreendemos sua capacidade de representar informações de maneira estruturada e de fácil acesso;
- Compreendemos a importância de utilizar operadores ternários para expressar decisões em uma única linha, tornando o código mais compacto e fácil de entender, melhorando a performance e manutenção do nosso projeto;
- Construímos nosso projeto com todas as opções de cadastro, listagem e alteração de estado do restaurante, assim como a possibilidade de sair da aplicação.

## Código
```py
import os

restaurantes = [
    {'nome': 'Praça', 'categoria': 'Japonesa', 'ativo': False},
    {'nome': 'Pizza Suprema', 'categoria': 'Pizza', 'ativo': True},
    {'nome': 'Cantina', 'categoria': 'Italiano', 'ativo': False},
]

def exibir_nome_do_programa():
    print('Sabor Express')

def exibir_opcoes():
    print('1. Cadastrar restaurante')
    print('2. Listar restaurante')
    print('3. Alternar estado do restaurante')
    print('4. Sair\n')

def finalizar_app():
    exibir_subtitulo('Finalizando o app...')

def voltar_ao_menu_principal():
    input('\nDigite uma tecla para voltar ao menu principal... ')
    main()

def opcao_invalida():
    print('Opcão inválida!\n')
    voltar_ao_menu_principal()

def exibir_subtitulo(texto):
    os.system('cls')
    # linha = '*' * (len(texto))
    # print(linha)
    print(texto)
    # print(linha)

def cadastrar_novo_restaurante():
    exibir_subtitulo('Cadastro de restaurante...')

    nome_do_restaurante = input('Digite o nome do restaurante que deseja cadastrar: ')
    categoria = input(f'Digite a categoria do restaurante {nome_do_restaurante}: ')

    dados_do_restaurante = {'nome':nome_do_restaurante, 'categoria':categoria, 'ativo':False}
    restaurantes.append(dados_do_restaurante)

    print(f'O restaurante {nome_do_restaurante} foi cadastrado com sucesso!')

    voltar_ao_menu_principal()

def listar_restaurantes():
    exibir_subtitulo('Listando os restaurantes cadastrados...')
    print(f"{'Nome do restaurante'.ljust(22)} | {'Categoria'.ljust(20)} | Status")
    for restaurante in restaurantes:
        nome_restaurante = restaurante['nome']
        categoria = restaurante['categoria']
        ativo = 'Ativado' if restaurante['ativo'] else 'Desativado' # Ternário
        print(f'- {nome_restaurante.ljust(20)} | {categoria.ljust(20)} | {ativo}')

    voltar_ao_menu_principal()

def alternar_estado_restaurante():
    exibir_subtitulo('Alternando o estado do restaurante...')

    nome_restaurante = input('Digite o nome do restaurante que alternar o estado: ')
    restaurante_encontrado = False

    for restaurante in restaurantes:
        if nome_restaurante == restaurante['nome']:
            restaurante_encontrado = True
            restaurante['ativo'] = not restaurante['ativo']
            mensagem = f'o restaurante {nome_restaurante} foi ativado com sucesso' if restaurante['ativo'] else f'o restaurante {nome_restaurante} foi desativado com sucesso'
            print(mensagem)

    if not restaurante_encontrado:
        print('O restaurante não foi encontrado')

    voltar_ao_menu_principal()

def escolher_opcao():
    try:
        opcao_escolhida = int(input('Escolha uma opção: '))
        # opcao_escolhida = int(opcao_escolhida)
        
        if opcao_escolhida == 1:
            cadastrar_novo_restaurante()
        elif opcao_escolhida == 2:
            listar_restaurantes()
        elif opcao_escolhida == 3:
            alternar_estado_restaurante()
        elif opcao_escolhida == 4:
            finalizar_app()
        else:
            opcao_invalida()
    except:
        opcao_invalida()

def main():
    os.system('cls')
    exibir_nome_do_programa()
    exibir_opcoes()
    escolher_opcao()

if __name__ == '__main__':
    main()
```

---

# 5. Consolidando os conhecimentos: O que aprendemos?
- Exploramos o conceito de docstrings e como elas desempenham um papel crucial na documentação de um código Python, proporcionando uma forma estruturada e incorporada de explicar as funcionalidades de módulos, funções, classes ou métodos presentes em nosso projeto;
- Compreendemos a importância do uso de docstring no dia a dia de um dev python inserido no mercado, destacando quando devemos utilizar esses conceitos e o impacto na colaboração de projetos.

## Código
```py
import os

restaurantes = [
    {'nome': 'Praça', 'categoria': 'Japonesa', 'ativo': False},
    {'nome': 'Pizza Suprema', 'categoria': 'Pizza', 'ativo': True},
    {'nome': 'Cantina', 'categoria': 'Italiano', 'ativo': False},
]

def exibir_nome_do_programa():
    ''' Exibe o nome estilizado do programa na tela '''
    print('Sabor Express')

def exibir_opcoes():
    ''' Exibe as opções disponíveis no menu principal '''
    print('1. Cadastrar restaurante')
    print('2. Listar restaurante')
    print('3. Alternar estado do restaurante')
    print('4. Sair\n')

def finalizar_app():
    ''' Exibe mensagem de finalização do aplicativo '''
    exibir_subtitulo('Finalizando o app...')

def voltar_ao_menu_principal():
    ''' Solicita uma tecla para voltar ao menu principal 
    
    Outputs:
    - Retorna ao menu principal
    '''
    input('\nDigite uma tecla para voltar ao menu principal... ')
    main()

def opcao_invalida():
    ''' Exibe mensagem de opção inválida e retorna ao menu principal 
    
    Outputs:
    - Retorna ao menu principal
    '''
    print('Opcão inválida!\n')
    voltar_ao_menu_principal()

def exibir_subtitulo(texto):
    ''' Exibe um subtítulo estilizado na tela 
    
    Inputs:
    - texto: str - O texto do subtítulo
    '''
    os.system('cls')
    # linha = '*' * (len(texto))
    # print(linha)
    print(texto)
    # print(linha)

def cadastrar_novo_restaurante():
    ''' Essa função é responsável por cadastrar um novo restaurante 
    
    Inputs:
    - Nome do restaurante
    - Categoria

    Outputs:
    - Adiciona um novo restaurante a lista de restaurantes
    '''
    exibir_subtitulo('Cadastro de restaurante...')

    nome_do_restaurante = input('Digite o nome do restaurante que deseja cadastrar: ')
    categoria = input(f'Digite a categoria do restaurante {nome_do_restaurante}: ')

    dados_do_restaurante = {'nome':nome_do_restaurante, 'categoria':categoria, 'ativo':False}
    restaurantes.append(dados_do_restaurante)

    print(f'O restaurante {nome_do_restaurante} foi cadastrado com sucesso!')

    voltar_ao_menu_principal()

def listar_restaurantes():
    ''' Lista os restaurantes presentes na lista 
    
    Outputs:
    - Exibe a lista de restaurantes na tela
    '''
    exibir_subtitulo('Listando os restaurantes cadastrados...')
    print(f"{'Nome do restaurante'.ljust(22)} | {'Categoria'.ljust(20)} | Status")
    for restaurante in restaurantes:
        nome_restaurante = restaurante['nome']
        categoria = restaurante['categoria']
        ativo = 'Ativado' if restaurante['ativo'] else 'Desativado' # Ternário
        print(f'- {nome_restaurante.ljust(20)} | {categoria.ljust(20)} | {ativo}')

    voltar_ao_menu_principal()

def alternar_estado_restaurante():
    ''' Altera o estado ativo/desativado de um restaurante 
    
    Outputs:
    - Exibe mensagem indicando o sucesso da operação
    '''
    exibir_subtitulo('Alternando o estado do restaurante...')

    nome_restaurante = input('Digite o nome do restaurante que alternar o estado: ')
    restaurante_encontrado = False

    for restaurante in restaurantes:
        if nome_restaurante == restaurante['nome']:
            restaurante_encontrado = True
            restaurante['ativo'] = not restaurante['ativo']
            mensagem = f'o restaurante {nome_restaurante} foi ativado com sucesso' if restaurante['ativo'] else f'o restaurante {nome_restaurante} foi desativado com sucesso'
            print(mensagem)

    if not restaurante_encontrado:
        print('O restaurante não foi encontrado')

    voltar_ao_menu_principal()

def escolher_opcao():
    ''' Solicita e executa a opção escolhida pelo usuário 
    
    Outputs:
    - Executa a opção escolhida pelo usuário
    '''
    try:
        opcao_escolhida = int(input('Escolha uma opção: '))
        # opcao_escolhida = int(opcao_escolhida)
        
        if opcao_escolhida == 1:
            cadastrar_novo_restaurante()
        elif opcao_escolhida == 2:
            listar_restaurantes()
        elif opcao_escolhida == 3:
            alternar_estado_restaurante()
        elif opcao_escolhida == 4:
            finalizar_app()
        else:
            opcao_invalida()
    except:
        opcao_invalida()

def main():
    ''' Função principal que inicia o programa '''
    os.system('cls')
    exibir_nome_do_programa()
    exibir_opcoes()
    escolher_opcao()

if __name__ == '__main__':
    main()
```

---

# Referências
### 1. [Documentação oficial do Python (gratuito, português, texto)](https://docs.python.org/pt-br/3/)
`Fonte oficial de informações sobre a linguagem Python. Aqui você encontra informações sobre os conceitos relacionados ao desenvolvimento da linguagem, tutoriais, referências, informações de atualizações, boas práticas e exemplos.`

### 2. [Artigo O que é Python? História, Sintaxe e um Guia para iniciar na Linguagem (gratuito, português, texto)](https://www.alura.com.br/artigos/python)

`Artigo focado em informar tudo sobre a linguagem Python, de primeiros passos até conceitos mais avançados e informações importantes sobre o mercado.`

`Referências, explicações e exemplos importantes sobre os diversos conceitos da linguagem python.`
