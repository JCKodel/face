# FACE

O FACE (Focus Agentic Code Environment) é a janela que um time abre para
construir software quando quem escreve o código são agentes. Você roda um
binário `face` numa pasta de projetos; ele trata cada subpasta como um
projeto, planta nele o método do
[focus-kit](https://github.com/JCKodel/focus-kit) e deixa você conversar,
pelo navegador, com o agente que você já paga (Claude Code, Codex, Copilot,
Cursor, Antigravity, OpenCode, Qwen Code). O que o método guarda em arquivo
(fila, páginas, documentos, decisões) o FACE mostra como board, marcos,
progresso e custo.

[Read in English](README.md)

O site, nas seis línguas da tela do FACE, com as telas e os downloads:
<https://face.kodel.com.br>.

## Instalar

No macOS (Apple Silicon) ou no Linux, com [Homebrew](https://brew.sh):

```sh
brew install jckodel/face/face
```

No Windows, com [winget](https://learn.microsoft.com/windows/package-manager/):

```powershell
winget install JCKodel.FACE
```

No Debian ou no Ubuntu, baixe de Releases o `.deb` da sua máquina
(`face_<v>_amd64.deb` ou `face_<v>_arm64.deb`) e instale com o `apt`, que
instala também o `git`:

```sh
sudo apt install ./face_<v>_amd64.deb
```

No Linux, ou no macOS sem Homebrew, o script do site baixa o zip da sua
máquina em Releases, confere com o `SHA256SUMS` e grava o `face` em
`~/.local/bin`, sem sudo:

```sh
curl -fsSL https://face.kodel.com.br/install.sh | sh
```

Depois, rode o `face` na pasta que tem os seus projetos, ou passe essa
pasta, de qualquer lugar:

```sh
cd ~/Projects && face
face ~/Projects
```

Para atualizar, rode `brew upgrade face` ou `winget upgrade JCKodel.FACE`,
instale o `.deb` novo do mesmo jeito, ou rode a mesma linha do `curl` de
novo.

## Baixar à mão

Este é o caminho manual. Os zips estão
[no site](https://face.kodel.com.br) e em
[Releases](https://github.com/JCKodel/face/releases), um por plataforma:

- `face-<v>-darwin-arm64.zip` (macOS, Apple Silicon)
- `face-<v>-linux-amd64.zip` (Linux x86_64)
- `face-<v>-linux-arm64.zip` (Linux arm64)
- `face-<v>-windows-amd64.zip` (Windows x86_64)

Baixe o da sua plataforma, descompacte na pasta que tem os seus projetos e
rode o `face` ali, sem renomear nada:

```sh
./face      # macOS, Linux
face.exe    # Windows
```

No Mac, se o macOS recusa abrir o `face`, é porque o arquivo baixado pelo
navegador e descompactado pelo Finder vem em quarentena. Tire a quarentena
e rode de novo:

```sh
xattr -d com.apple.quarantine face
./face
```

Cada release traz também o `SHA256SUMS`. Baixe-o ao lado do zip e confira
com:

```sh
shasum -a 256 -c --ignore-missing SHA256SUMS
```

## Termos

O FACE é gratuito para baixar e usar. O código ainda não é público; a licença vem depois.

Este repositório tem só issues e binários, então `go install` não funciona:
baixe o binário da sua plataforma.

Cada release traz o `THIRD_PARTY_NOTICES.txt`, com nome, versão, licença e
texto da licença do software de terceiros que o binário embarca.

## Issues

Relatos de bug e pedidos são bem-vindos em qualquer das seis línguas da
tela do FACE: inglês, português, espanhol, francês, alemão ou chinês
simplificado. Abra um em [Issues](https://github.com/JCKodel/face/issues/new/choose).
O link `Relatar um bug` no rodapé da home do FACE abre o formulário de bug
com a sua versão já preenchida.
