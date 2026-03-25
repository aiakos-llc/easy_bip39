# ⬡ Easy BIP39

**Tabela interativa de referência da wordlist BIP39 — 2048 palavras, índice binário, navegação por letra e filtro visual.**

Criado pela [AIAKOS](https://aiakos.com.br) — Autocustódia Bitcoin. *Yours is yours.*

---

## O que é

Uma ferramenta offline, de arquivo único, para consulta à lista oficial de 2048 palavras do padrão [BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki). Cada palavra é exibida com seu índice decimal e representação binária de 12 bits.

O BIP39 define as palavras usadas para gerar **seed phrases** — a sequência de 12 ou 24 palavras que funciona como chave mestra de uma carteira Bitcoin. Quem possui essas palavras, controla os fundos. Entender a relação entre cada palavra e seu índice binário é fundamental para quem quer compreender a autocustódia em nível técnico.

## Como usar

1. Baixe o `index.html`
2. Abra no navegador
3. Pronto

Não precisa de servidor, não precisa de internet, não precisa instalar nada.

> 🔒 **A AIAKOS recomenda fortemente o download e uso offline por medida de segurança.**

## Funcionalidades

**Tabela principal**
- 2048 palavras organizadas em 4 colunas com espaçamento simétrico
- Índice decimal e representação binária de 12 bits (3 grupos de 4 bits)
- Prefixo de 4 letras destacado em laranja (suficiente para identificação unívoca no padrão BIP39)
- Linhas de referência nos índices múltiplos de 100 com fundo diferenciado

**Navegação**
- Links rápidos por centenas (100, 200 ... 2000) com blink na linha alvo
- Links A-Z que saltam para a primeira palavra de cada inicial com blink na linha alvo
- Header fixo com todos os controles sempre visíveis
- Scroll-margin dinâmico baseado na altura real do header

**Filtros e toggles**
- Toggle maiúsculas — alterna entre 4 primeiras letras ou palavra inteira em maiúsculas (cores preservadas)
- Filtro por letra — exibe apenas as palavras de uma inicial, redistribuídas em 4 colunas

**Lista customizada**
- Botão "USAR MINHA LISTA" para carregar um arquivo `.txt` com 2048 palavras próprias
- Ao carregar, o título muda para "CUSTOMIZED WORDLIST" e um badge vermelho avisa que a lista pode não corresponder à oficial
- Para voltar à lista original, recarregue a página

**Seção didática**
- Tabela de pesos binários de cada bit
- Exemplo prático: POTATO = índice 1350
- Explicação de por que 4 letras são suficientes para identificar qualquer palavra

## Arquivos

| Arquivo | Descrição |
|---------|-----------|
| `index.html` | Ferramenta interativa com as 2048 palavras embutidas |
| `english.txt` | Cópia da lista oficial BIP39 para verificação independente |

## Verificação

As 2048 palavras já estão embutidas no `index.html`. O arquivo `english.txt` é incluído para que você possa verificar de forma independente que as palavras embutidas correspondem à lista oficial.

**Fonte primária (repositório oficial do Bitcoin):**

🔗 [github.com/bitcoin/bips/blob/master/bip-0039/english.txt](https://github.com/bitcoin/bips/blob/master/bip-0039/english.txt)

Para verificar:

```bash
# Baixe da fonte primária
curl -sO https://raw.githubusercontent.com/bitcoin/bips/refs/heads/master/bip-0039/english.txt

# Compare os hashes
sha256sum english.txt
```

O hash deve ser idêntico ao do `english.txt` incluído neste repositório.

> **Não confie, verifique.**

## Segurança e privacidade

- **Zero dependências externas** — nenhum CDN, nenhuma fonte externa, nenhum JavaScript de terceiros
- **Zero requisições de rede** — funciona 100% offline; as palavras estão embutidas no HTML
- **Sem cookies, sem tracking, sem analytics**
- **Código auditável** — HTML/CSS/JS legíveis, sem ofuscação nem minificação

## Licença

MIT — use, modifique e distribua livremente.

---

**AIAKOS** — Autocustódia Bitcoin
[aiakos.com.br](https://aiakos.com.br) · [@AiakosBTC](https://x.com/AiakosBTC)
