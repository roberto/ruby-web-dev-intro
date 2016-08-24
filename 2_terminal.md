# O que é o terminal, ou linha de comando?

O terminal, normalmente chamado de linha de comando ou interface de linha de
comando, é um programa baseado em texto. Ele é utilizado para visualização,
manipulação e manuseio de arquivos em seu computador \(como por exemplo,
o *Windows Explorer* ou o *Finder no Mac*, mas sem interface gráfica\),
além de também ser capaz de rodar outros programas. Outros nomes para a linha
de comando são: _cmd_, _CLI_, _prompt_, _console_ ou _terminal_.

No Windows, você pode abrir o terminal em:

**Iniciar** → **Todos os Programas** → **Acessórios** → **Prompt de comando**

No Mac:

**Applications** → **Utilities** → **Terminal**

No Linux:

**Applications** → **Accessories** → **Terminal**

Caso seu Linux seja diferente, você pode procurar no Google :\)

Agora você deve ver uma janela branca ou preta que está à espera de seus
comandos.
Se você estiver em Mac ou num Linux, você provavelmente verá um `$`, como este:

```sh
$
```

No Windows, é um sinal de `>`, como este:

```sh
>
```

## Executando comandos

Vamos começar com algo simples. Digite o seguinte comando:

```sh
$ whoami
```

Ou:

```sh
> whoami
```

Depois tecle Enter. Essa é nossa saída:

```sh
> whoami
caroline
```

Como você pode ver, esse comando mostra o seu usuário. No caso, quem é você :)

Outros comandos úteis:

| Comando (Windows) | Comando (Mac/Linux) | Descrição | Exemplo |
| --- | --- | --- | --- |
| `dir` | `ls` | Lista as pastas e arquivos | `ls` |
| `cd` | `cd` | Muda a pasta | `cd test` |
| `copy` | `cp` | Copia pastas e arquivos | `cp c:\t1\test.txt c:\t2\test.txt` |
| `move` | `mv` | Move pastas e arquivos | `mv c:\t1\test.txt c:\t2\test.txt` |
| `mkdir` | `mkdir` | Cria pastas | `mkdir test` |
| `del` | `rm` | Remove pastas e arquivos | `del c:\test\test.txt` |
| `exit` | `exit` | Fecha a janela | `exit` |

## Onde aprender mais sobre linha de comando?

Abaixo, alguns links que podem ajudar a ver mais sobre linha de comando:

* Para Windows [https://technet.microsoft.com/pt-br/library/bb978526.aspx](https://technet.microsoft.com/pt-br/library/bb978526.aspx)
* Para Mac/Linux [https://br.udacity.com/course/linux-command-line-basics--ud595/](https://br.udacity.com/course/linux-command-line-basics--ud595/)
* Para Mac/Linux [https://www.codecademy.com/pt-BR/learn/learn-the-command-line](https://www.codecademy.com/pt-BR/learn/learn-the-command-line) - está em inglês, porém é bastante simples
