# Bar do Igor – Cliente do Lobby

Cliente de lobby da comunidade para **Persona 4 Arena Ultimax** (PC). Adiciona um saguão com chat ("Bar do Igor") e pareamento por cima do online do próprio jogo.

**Versão de teste atual: 0.2.31** (Windows e Linux/Proton). É uma versão de teste para a comunidade Persona Arena Brasil. Espere arestas.

> Projeto de estudo feito com ajuda de IA (vibe coding). Veja [Transparência](#transparência-feito-com-ia-vibe-coding).

## Download

Baixe os arquivos na página de [Releases](../../releases/latest):

- `BarDoIgor-windows.zip`
- `BarDoIgor-linux.tar.gz`

SHA-256:

```
e225a448acb4bbb2588b5c1c7709646d9931e9f5f1e364a77fca7f7c3f9c74b6  BarDoIgor-windows.zip
7c8089fb90fd30d923ad83f74bf0a63bb0150640e00038099762ff88a2c3f5ca  BarDoIgor-linux.tar.gz
```

## Instalação

1. Extraia o arquivo e copie tudo o que está dentro de `pasta_do_jogo/` para a pasta do P4AU, ao lado do `P4U2.exe` (Steam > botão direito no jogo > Gerenciar > Procurar arquivos locais).
2. **Windows:** abra o jogo pela Steam normalmente.
   **Linux:** rode `chmod +x p4au-lobby juntar_logs.sh` e coloque nas opções de inicialização da Steam: `WINEDLLOVERRIDES="version=n,b" %command%`.
3. No jogo, aperte **F10 > Servidores**, digite o endereço e a porta que o organizador passar e clique em **Conectar**. Quando ficar verde, o botão **LOBBY** aparece em Network.

Para jogar sem o Bar do Igor, apague `p4au-lobby(.exe)`, `version.dll` e `lobby_config.dll` da pasta do jogo. O antivírus pode bloquear, porque o cliente lê a memória do jogo: libere a pasta do jogo.

## Problema conhecido: "Failed Connect"

Depois de muitas revanches seguidas, iniciar uma nova luta pode falhar com **Failed Connect**. Ainda não provamos a causa, então o que segue é um paliativo, não uma correção.

- **Não fique martelando o botão de confirmar/READY.** Martelar logo depois da partida piora. Aperte uma vez e espere.
- Se falhar, espere alguns segundos e tente de novo **uma única vez**.
- Se falhar de novo, **troquem quem hospeda**: o outro jogador vira o 1P e inicia a luta.
- Continua falhando? Feche e abra de novo o jogo e o cliente, e nos mande os logs.

## Enviando os logs

Depois de fechar o jogo e o cliente, rode `Juntar_logs.bat` (Windows) ou `bash ./juntar_logs.sh` (Linux) na pasta do jogo e mande o `logs_bar_do_igor_<data-hora>.zip` gerado ao organizador. O `config.toml` e o `avatar_escolhido.json` ficam fora do pacote.

## Transparência: feito com IA (vibe coding)

Este projeto foi desenvolvido com **muita ajuda de inteligência artificial** (vibe coding), como **projeto de estudo**. O código, os textos e os pacotes foram escritos e revisados com assistentes de IA, e eu testo e corrijo ao longo do caminho. Por isso, espere bugs, e leia o código e os binários com o cuidado de qualquer software de terceiros.

## Estado

O código-fonte ainda não está publicado aqui; este repositório só distribui versões de teste. Sem ligação com a Atlus nem com a Arc System Works.
