# kleberDevion

Me chamo Kleber.
Projetos uteis 'Pra mim e':
Criei uma linguagem de programação. O resto desta página é rodapé.

## Jinga

Linguagem de propósito geral, antes chamada PoolScript. O repositório ainda carrega o nome antigo: [kleberDevion/poolscript](https://github.com/kleberDevion/poolscript).

Sintaxe própria: `funct`, `Entity`/`class`, `model`, `enum`, `private`/`public`, `base(Pai)`, `async`/`await` com fibras.

- Tipagem estática conferida antes de rodar (`jinga --check`).
- Máquina virtual em C, cerca de 60 mil linhas.
- Compilação direta do fonte em duas passadas.
- Laços viram código de máquina x86-64 (JIT).
- Coletor de lixo próprio.
- Depurador com breakpoint, passo a passo e gráfico de execução.

```
funct maior(a, b) {
    if a > b {
        return a
    }
    return b
}

Entity Ponto {
    funct __init__(self, x) {
        self.x = x
    }
}

p = Ponto(maior(3, 7))
if p.x > 1 {
    post("x passou de um")
}
```

**Stdlib embutida.** os, sys, json, date, regex, dotenv, jwt, hash, bytes, sqlite3, mail, request (cliente HTTP), qrcode, psodbc (SQLite, Postgres, MySQL, Mongo), jinker (servidor HTTP e WebSocket com salas, rotas por decorador, swagger) e sockets.

**Tooling.** Servidor LSP próprio (hover rico, completion, diagnóstico, outline, signature help) usado no VS Code, IntelliJ via LSP4IJ e Neovim. Extensão do VS Code. Gerenciador de pacotes `jpkg`. Instalador de uma linha. Binário standalone com `jinga x.pr -o x`.

## Números

Medidos em 2026-09-26.

| o quê | quanto |
|---|---|
| commits desde 2026-07-31 (menos de dois meses) | 503 |
| casos de teste em C | 8.541 |
| páginas de documentação em markdown | 467 |
| versão | 16.1.3 |

A suíte roda também sob AddressSanitizer e sem JIT.

## Regras que imponho no projeto

Não são preferências, são regras.

- Erro apontado na causa, e antes de rodar. Mensagem no sintoma é bug.
- Nada de falso verde. Teste que mascara erro é pior que teste nenhum.
- Feature só entra fechada em todos os eixos: motor, editor, doc, teste. Pela metade não entra.
- Medir antes de afirmar. "Ficou mais rápido" não é frase; número medido é.
- Scripts de apoio escritos na própria linguagem. Se a Jinga não dá conta de automatizar a Jinga, o problema é dela.

## Stack

| Onde | Nível |
|---|---|
| Jinga | Criador. Motor, stdlib, LSP, gerenciador de pacotes e documentação. |
| Python | A linguagem que mais conheço. |
| React | Tenho experiência. Não muita, mas tenho. |
| JavaScript | Um pouco. |
| CSS / Tailwind | Copio e colo o componente. Funciona. |

## Sobre a preguiça

Sou preguiçoso. Na prática isso vira automatizar tudo que se repete. Automatizar cansa menos do que repetir, e o script é escrito em Jinga.

## Contato

Só aqui no GitHub.

## Repositório

https://github.com/kleberDevion/poolscript

```sh
curl -fsSL https://raw.githubusercontent.com/kleberDevion/poolscript/main/instalar.sh | sudo bash
```
