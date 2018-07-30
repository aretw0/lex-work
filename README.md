# lex-work
Trabalho da cadeira de compiladores.

Este trabalho consiste em fazer um analisador de código HTML usando o Flex para gerar código C++. O analisador deve receber um arquivo no formato **.html** na linha de comando, ou ler da entrada padrão, caso
nenhum arquivo seja fornecido, e exibir:

- A estrutura hierárquica do documento HTML
- As quantidades de:
    - Linhas no arquivo
    - Pares de Tags HTML
    - Caracteres do conteúdo exibido pela página

A hierarquia do documento deve ser apresentada como no exemplo abaixo:

```
+--<html>
|   +--<head>
|   |   +--<style>
|   |   +--</style>
|   |   +--<title>
|   |   |   +--Texto[3]
|   |   +--</title>
|   +--</head>
|   +--<body>
|   |   +--<h1>
|   |   |   +--Texto[20]
|   |   +--</h1>
|   |   +--<p>
|   |   |   +--<b>
|   |   |   |   +--Texto[3]
|   |   |   +--</b>
|   |   |   +--Texto[81]
|   |   |   +--Texto[134]
|   |   |   +--Texto[135]
|   |   |   +--Texto[140]
|   |   +--</p>
|   |   +--<br>
|   |   +--<img src="Images/sample.png">
|   |   +--<br>
|   |   +--<p>
|   |   |   +--Texto[37]
|   |   |   +--<a href="https://www.w3schools.com/">
|   |   |   |   +--Texto[9]
|   |   |   +--</a>
|   |   |   +--Texto[1]
|   |   +--</p>
|   |   +--<br>
|   +--</body>
+--</html>
```

Uso
-
>Configurei algumas tarefas pelo **vscode** para facilitar o uso.

Execute as tarefas nessa ordem:

1. cmake
2. make

Esta ultima deve gerar o arquivo **Htmlex** na pasta [Build](https://github.com/aretw0/lex-work/tree/master/Build) e logo você poderá executar-lo           
        
    ./Build/Htmlex < ./data/lex.html

Referências
-

- [A Lexical Analyzer for HTML and Basic SGML](https://www.w3.org/TR/WD-html-lex/)
- [A lexical analyzer for Basic+/- SGML Documents](https://www.w3.org/TR/WD-html-lex/sgml.l)