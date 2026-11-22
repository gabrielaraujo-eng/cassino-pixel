# Cassino Pixel

> experiência de cassino pixel-art com fichas virtuais, criada por [Gabriel Lúcio de Araújo](https://github.com/gabrielaraujo-eng).

<p align="center">
  <a href="https://gabrielaraujo-eng.github.io/cassino-pixel/">
    <img src="./assets/cassino-pixel-banner.png" alt="Banner de Cassino Pixel" width="100%" />
  </a>
</p>

<p align="center"><strong><a href="https://gabrielaraujo-eng.github.io/cassino-pixel/">▶ Jogar Cassino Pixel</a></strong></p>

**Cassino Pixel** reúne minijogos de cassino em uma interface pixel-art. Escolha uma mesa, use fichas virtuais e jogue partidas rápidas de Blackjack, pôquer e caça-níquel, sem dinheiro real.

## Jogar

- **[Abrir a versão publicada](<https://gabrielaraujo-eng.github.io/cassino-pixel/>)**
- **[Ver o código no GitHub](https://github.com/gabrielaraujo-eng/cassino-pixel)**
- **[Abrir o Arcade Gabriel](https://gabriel-lucio-arcade-c27ec.web.app/)**

A versão atual identificada neste repositório é **1.5** e permanece na raiz do projeto.

## O que foi melhorado nesta separação

Esta versão foi organizada como um projeto independente a partir do jogo publicado, mantendo a versão atual na raiz e o histórico em pastas próprias. Além da documentação própria, foram ajustados:

- título, descrição, autoria e URL canônica para o novo repositório;
- metadados de tema e compartilhamento para navegadores e redes sociais;
- documentação de controles, compatibilidade e arquitetura;
- política transacional para encerrar mãos de pôquer interrompidas por recarga sem reembolso implícito;
- título principal semântico em `h1` para navegação por leitores de tela e mecanismos de busca;
- regiões `aria-live` para anúncios de saldo, turno, resultados e erros importantes;
- indicador de foco de alto contraste para navegação por teclado em controles e mesas;
- documentação dos snapshots versionados disponíveis no diretório `versoes-antigas/`;
- workflow preparado para publicação no GitHub Pages;
- banner e favicon próprios do jogo;
- remoção dos arquivos de coleta de dados e dos backups técnicos.

**Cassino Pixel** preserva as funcionalidades centrais do jogo: O projeto preserva o salão principal, Blackjack com objetivo de chegar a 21, pôquer, caça-níquel, fichas virtuais e navegação entre as mesas.

## Controles

| Ação | Teclado e mouse | Touch |
| --- | --- | --- |
| Escolher uma mesa | clicar no card do jogo | tocar no card |
| Jogar Blackjack | usar os botões da mesa | tocar nos botões |
| Jogar pôquer | selecionar a ação exibida | tocar na ação |
| Usar caça-níquel | clicar no controle da máquina | tocar no controle |
| Voltar ao salão | botão de retorno | botão na interface |

As fichas são virtuais e servem apenas para a experiência local do jogo. Não há apostas ou pagamentos reais.

## Rodar localmente

O projeto não precisa de build nem de dependências instaladas. Sirva a pasta por HTTP para que os recursos do navegador funcionem normalmente:

```bash
python3 -m http.server 8000
```

Depois abra <http://localhost:8000>. Também é possível usar qualquer servidor estático, como o Live Server do VS Code. Abrir o arquivo diretamente com `file://` pode limitar alguns recursos do navegador.

## Stack

- HTML, CSS e JavaScript client-side; interface pixel-art e lógica de minijogos executadas no navegador; sem backend próprio.
- Interface, regras e fluxo principal executados no cliente;
- workflow do GitHub Actions preparado para o GitHub Pages.

Não há backend próprio neste repositório.

## Estrutura

```text
.
├── index.html                 # versão atual do jogo
├── assets/                    # banner e favicon do projeto
├── versoes-antigas/           # versões históricas preservadas
├── README.md                  # documentação do projeto
└── .github/workflows/pages.yml # publicação no GitHub Pages
```

## Privacidade e dados locais

O jogo não coleta dados pessoais, não processa pagamentos e não envia resultados para serviços externos. As fichas virtuais não possuem valor monetário. O repositório não contém o bloco de coleta de atividade, ranking ou envio de estatísticas que existia em versões anteriores.

## Roadmap

- separar CSS e JavaScript em módulos menores sem alterar a experiência atual;
- adicionar testes de fumaça para a abertura e o fluxo principal;
- revisar o carregamento das dependências CDN e oferecer uma estratégia offline;
- melhorar acessibilidade de menus, diálogos e indicadores da interface;
- adicionar uma página de changelog para as próximas versões.

## Jogos relacionados

- [Aethra Online](https://github.com/gabrielaraujo-eng/aethra-online)
- [Bastião 3D](https://github.com/gabrielaraujo-eng/bastiao-3d)
- [SuperMauricio](https://github.com/gabrielaraujo-eng/super-mauricio)
- [Clicker](https://github.com/gabrielaraujo-eng/clicker)
- [Xadrez](https://github.com/gabrielaraujo-eng/xadrez)
- [5h no Banheiro](https://github.com/gabrielaraujo-eng/5h-no-banheiro)

## Créditos

Criado por **Gabriel Lúcio de Araújo**. A versão publicada neste repositório é a referência atual desta separação. Os créditos e links do autor também estão disponíveis dentro do jogo quando aplicável.

## Histórico de versões

As versões antigas preservadas foram organizadas em [`versoes-antigas/`](./versoes-antigas/), cada uma em sua própria pasta. A versão atual permanece na raiz e continua sendo a referência publicada.

- `1.5` (atual)
- `cassino1.4` (snapshot anterior à correção da documentação histórica)
- `cassino1.3` (snapshot anterior ao indicador de foco)
- `cassino1.2` (snapshot anterior às regiões live)
- `cassino1.1` (snapshot anterior à inclusão do título principal)
- `cassino1.0` (snapshot inicial)

Snapshots preservados antes de cada etapa:
- [`cassino1.0`](./versoes-antigas/cassino1.0/)
- [`cassino1.1`](./versoes-antigas/cassino1.1/)
- [`cassino1.2`](./versoes-antigas/cassino1.2/)
- [`cassino1.3`](./versoes-antigas/cassino1.3/)
- [`cassino1.4`](./versoes-antigas/cassino1.4/)
