# Módulo 4: Funções

Este módulo tem como objetivo ensinar os alunos a criar funções reutilizáveis em Python, entendendo conceitos como parâmetros, retorno de valores, argumentos posicionais e nomeados, escopo de variáveis e muito mais. Ao final do módulo, os alunos serão capazes de criar programas modulares e organizados utilizando funções.

---

## 🎯 Objetivo do Módulo
- Aprender a criar e utilizar funções em Python.
- Entender o uso de parâmetros e retorno de valores.
- Dominar conceitos como escopo de variáveis, argumentos posicionais e nomeados.
- Aplicar funções em programas práticos, como cálculo de notas e sistemas de login.

---

## 🏗️ Estrutura da Aula

### 1. Revisão Rápida do Módulo 3 (10 minutos)
- Breve revisão de listas, tuplas, dicionários e conjuntos.
- Resolução de dúvidas sobre o Módulo 3.

### 2. Introdução às Funções (20 minutos)
- O que são funções e por que utilizá-las?
- Sintaxe básica de uma função.
- Exemplo simples de função.

### 3. Parâmetros e Retorno de Valores (40 minutos)
- Funções com parâmetros.
- Funções com retorno de valores.
- Múltiplos retornos.

### 4. Argumentos Posicionais e Nomeados (20 minutos)
- Diferença entre argumentos posicionais e nomeados.
- Exemplos práticos.

### 5. Escopo de Variáveis (20 minutos)
- Variáveis locais e globais.
- Exemplos de escopo.

### 6. Atividade Prática (40 minutos)
- Criar um programa de cálculo de notas com funções.

### 7. Desafio Extra (20 minutos)
- Criar um sistema de login com funções.

---

## 📂 Exemplos de Código

### 1. Função Simples
**Arquivo:** `funcao_simples.py`
```python
def saudacao():
    print("Olá, mundo!")

saudacao()
```

### 2. Função com Parâmetros e Retorno
**Arquivo:** `funcao_parametros_retorno.py`
```python
def soma(a, b):
    return a + b

resultado = soma(10, 5)
print(resultado)  # 15
```

### 3. Função com Múltiplos Retornos
**Arquivo:** `funcao_multiplos_retornos.py`
```python
def calcula_media(notas):
    soma = sum(notas)
    media = soma / len(notas)
    return soma, media

notas = [8.5, 7.0, 9.0]
soma_notas, media_notas = calcula_media(notas)
print(f"Soma: {soma_notas}, Média: {media_notas}")
```

### 4. Argumentos Posicionais e Nomeados
**Arquivo:** `argumentos_posicionais_nomeados.py`
```python
def subtracao(a, b):
    return a - b

resultado1 = subtracao(10, 5)  # Argumentos posicionais
resultado2 = subtracao(b=5, a=10)  # Argumentos nomeados
print(resultado1, resultado2)  # 5 5
```

### 5. Escopo de Variáveis
**Arquivo:** `escopo_variaveis.py`
```python
x = 10  # Variável global

def minha_funcao():
    y = 5  # Variável local
    print(x + y)

minha_funcao()
# print(y)  # Erro: y não está definido fora da função
```

### 6. Atividade Prática: Cálculo de Notas
**Arquivo:** `calculo_notas.py`
```python
def calcular_media(notas):
    return sum(notas) / len(notas)

def verificar_aprovacao(media):
    return "Aprovado" if media >= 7 else "Reprovado"

def exibir_resultado(notas):
    media = calcular_media(notas)
    situacao = verificar_aprovacao(media)
    print(f"Média: {media:.2f} - Situação: {situacao}")

notas = [8.5, 7.0, 9.0]
exibir_resultado(notas)
```

### 7. Desafio Extra: Sistema de Login
**Arquivo:** `sistema_login.py`
```python
def verificar_login(usuario, senha):
    usuarios = {"admin": "1234", "user": "abcd"}
    return usuario in usuarios and usuarios[usuario] == senha

def sistema_login():
    usuario = input("Digite o usuário: ")
    senha = input("Digite a senha: ")
    if verificar_login(usuario, senha):
        print("Login bem-sucedido!")
    else:
        print("Usuário ou senha incorretos.")

sistema_login()
```

### 8. Função com Valor Padrão
**Arquivo:** `funcao_valor_padrao.py`
```python
def saudacao(nome="usuário"):
    print(f"Olá, {nome}!")

saudacao("Estevão")  # Olá, Estevão!
saudacao()           # Olá, usuário!
```

### 9. Função com Número Variável de Argumentos
**Arquivo:** `funcao_args.py`
```python
def soma(*numeros):
    return sum(numeros)

resultado = soma(10, 20, 30, 40)
print(resultado)  # 100
```

### 10. Função com Argumentos Nomeados Variáveis
**Arquivo:** `funcao_kwargs.py`
```python
def exibir_info(**kwargs):
    for chave, valor in kwargs.items():
        print(f"{chave}: {valor}")

exibir_info(nome="Estevão", idade=30, cidade="São Paulo")
```

### 11. Função Recursiva
**Arquivo:** `funcao_recursiva.py`
```python
def fatorial(n):
    return 1 if n == 1 else n * fatorial(n - 1)

print(fatorial(5))  # 120
```

### 12. Função Lambda
**Arquivo:** `funcao_lambda.py`
```python
quadrado = lambda x: x ** 2
print(quadrado(5))  # 25
```

### 13. Função com Documentação
**Arquivo:** `funcao_docstring.py`
```python
def calcular_area_retangulo(largura, altura):
    """
    Calcula a área de um retângulo.
    Parâmetros:
    largura (float): Largura do retângulo.
    altura (float): Altura do retângulo.
    Retorna:
    float: Área do retângulo.
    """
    return largura * altura

print(calcular_area_retangulo(10, 5))  # 50
```

### 14. Função com Lista de Compreensão
**Arquivo:** `funcao_lista_compreensao.py`
```python
def quadrados(numeros):
    return [x ** 2 for x in numeros]

print(quadrados([1, 2, 3, 4, 5]))  # [1, 4, 9, 16, 25]
```

### 15. Função com Manipulação de Dicionários
**Arquivo:** `funcao_dicionarios.py`
```python
def atualizar_idade(pessoas, nome, nova_idade):
    if nome in pessoas:
        pessoas[nome] = nova_idade
    return pessoas

pessoas = {"Estevão": 30, "Maria": 25}
pessoas = atualizar_idade(pessoas, "Estevão", 31)
print(pessoas)  # {'Estevão': 31, 'Maria': 25}
```

### 16. Função com Tratamento de Erros
**Arquivo:** `funcao_tratamento_erros.py`
```python
def dividir(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Erro: Divisão por zero."

print(dividir(10, 2))  # 5.0
print(dividir(10, 0))  # Erro: Divisão por zero.
```

### 17. Função com Decorador
**Arquivo:** `funcao_decorador.py`
```python
def decorador(funcao):
    def wrapper(*args, **kwargs):
        print("Antes de executar a função.")
        resultado = funcao(*args, **kwargs)
        print("Depois de executar a função.")
        return resultado
    return wrapper

@decorador
def saudacao(nome):
    print(f"Olá, {nome}!")

saudacao("Estevão")
```

---

