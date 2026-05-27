# Créditos e atribuição

Os dados deste repositório derivam de fontes públicas da comunidade Squad. Agradecemos
e atribuímos:

## Dados de mapa, veículos e facções (`manifests/maps.json`, `vehicles.json`, `factions.json`)

- **Fonte:** [Squad-Wiki/squad-wiki-pipeline-map-data](https://github.com/Squad-Wiki/squad-wiki-pipeline-map-data)
  — arquivo `finished.json` (mapas, layers, veículos por time, facções).
- **Licença:** **CC-BY-SA 4.0**. Derivados (como estes manifests) mantêm a mesma licença,
  com atribuição à fonte.

## Imagens (`images/`): minimapas, bandeiras, ícones de classe/veículo e armas

- **Fonte:** [Squad Wiki (Fandom)](https://squad.fandom.com) — mantida pela comunidade e
  mais atual que alternativas paradas (cobre mapas, facções e armas recentes).
- **Licença:** **CC-BY-SA 3.0** (termos padrão do Fandom/Wikia). Imagens redistribuídas
  com atribuição; derivados mantêm a mesma licença.
- **Conteúdo:** `images/maps/` (minimapas por nível, reduzidos para ~1600 px),
  `images/flags/` (bandeira/emblema por facção), `images/roles/` (ícones de classe),
  `images/vehicles/` (ícones por categoria de veículo), `images/mapicons/` (marcadores) e
  `images/weapons/` (ícones de arma). O catálogo completo de arquivos, com o nome de
  origem no Fandom, fica em [`images/INDEX.json`](images/INDEX.json).

> Observação: o repositório [mahtoid/SquadMaps](https://github.com/mahtoid/SquadMaps)
> (AGPL-3.0) foi avaliado como fonte de minimapas, mas está ~3 anos sem atualização
> (sem mapas/facções novos), por isso optou-se pelo Fandom.

---

"Squad" é uma marca da Offworld Industries. Este projeto é um esforço **não-oficial**
da comunidade e não é afiliado nem endossado pela Offworld Industries.

A proveniência exata (commit/SHA das fontes) de cada geração fica registrada em
[`version.json`](version.json).
