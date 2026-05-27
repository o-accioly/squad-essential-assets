# squad-essential-assets

Assets públicos e traduções (locales) do **Squad Essential** — o app desktop de
gerenciamento de servidores Squad. Este repositório é **consumido em runtime** pelo
programa (sincronização automática) e é **aberto a contribuições da comunidade**:
modders e tradutores podem adicionar nomes de itens, mapas custom e idiomas via Pull Request,
e isso passa a aparecer no app sem precisar de uma nova versão.

> Este repo entra como **submódulo** (pasta `public/`) dentro do projeto principal
> (privado) `o-accioly/squad-essential`.

## Estrutura

```
manifests/        # game-data (JSON) — tradução de nomes crus do jogo -> rótulos amigáveis
  maps.json       #   mapas + layers (veículos por time, facções, tickets)
  vehicles.json   #   classname BP_... (sem _C) -> nome/categoria/ícone
  factions.json   #   código da facção -> nome + aliases
  weapons.json    #   armas (a preencher: ícones/nomes via Squad Wiki)
  deployables.json#   deployables (FOB, HAB, ...)
  roles.json      #   classes/kits
images/           # ícones e imagens (bandeiras, mapas, armas) — referenciados pelos manifests
locales/          # traduções da interface do app (i18n) — ver locales/README.md
version.json      # versão do dataset + fontes (para o sync detectar atualizações)
```

## Como o app consome

O app baixa `version.json` no startup; se houver versão mais nova, sincroniza os
`manifests/` e cacheia localmente. Imagens são baixadas sob demanda. Tudo funciona
offline depois do primeiro sync (e há um *seed* embutido no app para o primeiro boot).

A URL base é configurável no app, então forks/mirrors da comunidade também funcionam.

## Como contribuir

- **Tradução de itens/veículos/armas:** edite o `entries` do manifest correspondente
  (`{"BP_Nome": {"label": "Nome Amigável", ...}}`). Variações de acessório podem ir em
  `aliases` ou `suffix_strip`.
- **Mapas/mods custom:** adicione a layer em `maps.json` (`layers`) com seus veículos.
- **Idiomas:** veja [`locales/README.md`](locales/README.md).

Boa parte do `manifests/` é **gerada automaticamente** por um extrator a partir de fontes
públicas (ver [CREDITS.md](CREDITS.md)) — para dados gerados, prefira corrigir na fonte
ou sinalizar numa issue, pois uma regeração pode sobrescrever edições manuais.

## Licença / atribuição

Dados derivados de fontes públicas — veja **[CREDITS.md](CREDITS.md)**. O conteúdo de
dados deste repositório é distribuído sob **CC-BY-SA 4.0** (compatível com as fontes).
