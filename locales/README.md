# Locales (i18n)

Traduções da interface do **Squad Essential**. Cada idioma é um arquivo
`<código>.json` (BCP-47), onde as chaves são identificadores estáveis e os valores
são os textos exibidos.

- **Idioma base:** `pt-BR.json` (o app é escrito em Português do Brasil).
- Para um novo idioma, copie `pt-BR.json`, renomeie (ex.: `en.json`, `es.json`,
  `ru.json`) e traduza os **valores** — nunca as chaves.

```jsonc
{
  "schema": 1,
  "language": "pt-BR",
  "strings": {
    "nav.home": "Início",
    "nav.players": "Jogadores"
  }
}
```

> Observação: o carregador de i18n no app ainda está em desenvolvimento. Esta pasta já
> define o **formato** para que as contribuições da comunidade possam começar; as chaves
> serão consolidadas conforme a UI for instrumentada.

Contribuições são bem-vindas via Pull Request.
