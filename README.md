# easy_bip39
Easy way to find a BIP39 word and its binary representation - 100% client-side, zero dependencies, zero external requests.

BIP39 English Wordlist — Tabela interativa de referência
Ferramenta offline de consulta à wordlist oficial do BIP39 (2048 palavras), com índice binário de 12 bits, navegação por letra e filtro visual.
O que é
Um arquivo HTML que exibe a lista completa de palavras BIP39 em formato de tabela com 4 colunas. Cada palavra é acompanhada do seu índice decimal e da representação binária de 12 bits dividida em 3 grupos de 4 bits.
Arquivos
ArquivoDescriçãoindex.htmlFerramenta interativa (abrir no navegador)english.txtLista de 2048 palavras BIP39 (uma por linha)
Sobre o arquivo english.txt
O repositório inclui uma cópia da lista oficial de palavras BIP39 para conveniência.
Recomendamos que você baixe o arquivo diretamente da fonte primária e substitua a cópia incluída:
🔗 https://raw.githubusercontent.com/bitcoin/bips/refs/heads/master/bip-0039/english.txt
Salve como english.txt no mesmo diretório do index.html.

Não confie, verifique. A fonte primária é o repositório oficial do Bitcoin. Você pode comparar o hash SHA-256 do arquivo baixado de cada fonte para confirmar que são idênticos.

Se o arquivo não estiver presente, a página exibirá um aviso explicando o que são seed phrases e como obter a lista de palavras, incluindo a opção de selecionar o arquivo manualmente (útil ao abrir localmente via file://, onde o navegador bloqueia o carregamento automático por segurança).
Funcionalidades

Tabela completa — 2048 palavras em 4 colunas com índice decimal e binário (espaçamento simétrico entre # e último grupo de bits)
Prefixo de 4 letras destacado — as 4 primeiras letras (suficientes para identificação unívoca) em laranja; restante em offwhite
Toggle maiúsculas — alterna entre exibir apenas as 4 primeiras letras em maiúsculas ou a palavra inteira em maiúsculas (cores preservadas)
Navegação por centenas — links rápidos para os índices 100, 200 ... 2000; linhas de referência com fundo destacado; ao clicar, a linha alvo pisca em laranja para facilitar a localização visual
Navegação por letra — links A-Z que saltam para a primeira palavra de cada inicial; ao clicar, a linha alvo pisca em laranja (letras inexistentes na lista ficam desabilitadas)
Filtro por letra — ao selecionar uma letra e ativar o toggle "FILTRAR LETRA", exibe apenas as palavras daquela inicial redistribuídas em 4 colunas; ao desativar, reseta a seleção e retorna ao topo da tabela completa
Header fixo — título, link para explicação, navegação por números, navegação por letras e toggles sempre visíveis ao rolar a página
Carregamento externo da wordlist — as palavras são carregadas do arquivo english.txt (não estão embutidas no HTML), permitindo que o usuário substitua pela versão baixada diretamente da fonte primária
Fallback para uso local — ao abrir via file://, onde o fetch é bloqueado pelo navegador, a página oferece um botão para selecionar o english.txt manualmente
Explicação didática — seção ao final com tabela de pesos binários de cada bit, exemplo prático (POTATO = índice 1350) e explicação de por que 4 letras são suficientes para identificar qualquer palavra da lista

Segurança e privacidade

Zero dependências externas — nenhum CDN, nenhuma fonte externa, nenhum JavaScript de terceiros
Zero requisições de rede — funciona 100% offline após download (o carregamento do english.txt é local)
Sem cookies, sem tracking, sem analytics
Código auditável — HTML/CSS/JS legíveis, sem ofuscação nem minificação

Como usar

Baixe index.html e english.txt (ou baixe o english.txt da fonte primária do Bitcoin)
Coloque ambos no mesmo diretório
Abra index.html no navegador
Pronto — funciona offline, sem instalação

Por que esta ferramenta existe
O BIP39 define as 2048 palavras usadas para gerar seed phrases de carteiras Bitcoin. Cada palavra corresponde a um índice binário de 11 bits (0 a 2047). Entender essa relação entre palavra e índice é fundamental para quem quer compreender como funciona a autocustódia em nível técnico.
Esta ferramenta foi criada pela AIAKOS como recurso educacional para a comunidade Bitcoin.
Licença
MIT — use, modifique e distribua livremente.

AIAKOS — Autocustódia Bitcoin
Yours is yours.
