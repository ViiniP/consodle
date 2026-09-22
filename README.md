# Consodle

Jogo de navegador inspirado no formato DLE, com temática de consoles e videogames portáteis. A proposta é descobrir o console secreto a partir das características reveladas a cada palpite.

O Consodle é um projeto pessoal de estudo e portfólio, desenvolvido com HTML, CSS e JavaScript puro. O objetivo é construir uma experiência simples, visualmente consistente e acessível, com publicação na internet ao final do desenvolvimento.

## Status do projeto

Em desenvolvimento. A etapa atual é a construção da interface com HTML e CSS, baseada em um protótipo criado no Figma.

A página já contém a logo, a chamada do jogo, o campo de palpite, o botão de envio e a legenda dos indicadores. A busca, a comparação de consoles e o controle da partida ainda serão implementados em JavaScript; o formulário atual ainda não executa o jogo.

## Como o jogo vai funcionar

1. O jogador pesquisa e seleciona um console.
2. Ao confirmar o palpite, uma linha exibe as características do console escolhido.
3. Cores e indicadores mostram quais características correspondem à resposta.
4. O jogador usa essas pistas para fazer novos palpites até acertar.

A primeira versão terá tentativas ilimitadas. O desafio diário está planejado para uma etapa posterior à implementação da partida básica.

### Características comparadas

| Característica | Comparação |
| --- | --- |
| Fabricante | Igual ou diferente do fabricante do console secreto |
| Ano de lançamento | Igual, anterior ou posterior ao ano da resposta |
| Geração | Igual, maior ou menor que a geração da resposta |
| Tipo | Console de mesa, portátil ou híbrido |
| Mídias de jogos | Comparação entre os formatos de mídia aceitos |

O ano seguirá o primeiro lançamento mundial. Para o catálogo inicial, serão considerados os modelos principais e suas mídias, sem revisões como Slim e Pro ou mídias dependentes de acessórios.

### Indicadores

- **Verde — correto:** a característica corresponde à resposta.
- **Vermelho — incorreto:** a característica não corresponde à resposta.
- **Laranja — parcial:** as listas de mídias têm algum formato em comum, mas não são iguais.
- **Seta para cima:** o valor do console secreto é maior que o do palpite.
- **Seta para baixo:** o valor do console secreto é menor que o do palpite.

As setas serão usadas no ano de lançamento e na geração. Por exemplo: se um palpite mostra 1994 com uma seta para baixo, o console procurado foi lançado antes de 1994.

## Objetivos de aprendizado

- Praticar HTML semântico na estrutura de formulários, tabelas e conteúdo.
- Organizar CSS com variáveis globais e arquivos por área da interface.
- Desenvolver layouts responsivos com Flexbox e Grid.
- Trabalhar com objetos, arrays, funções e módulos em JavaScript.
- Manipular o DOM e responder às interações do jogador.
- Separar os dados dos consoles, as regras do jogo e a apresentação visual.
- Salvar o progresso localmente com `localStorage`.
- Melhorar a acessibilidade com navegação por teclado, identificação dos controles e pistas que não dependam apenas de cores.
- Documentar e publicar um projeto completo para o portfólio.

## Tecnologias

- **HTML5:** estrutura da página.
- **CSS3:** estilos, componentes e responsividade.
- **JavaScript:** planejado para a lógica e as interações do jogo.
- **Figma:** prototipação da interface.
- **Google Fonts:** fontes Press Start 2P e Sora.

O escopo inicial não inclui frameworks, backend, banco de dados, contas de usuário ou ranking online.

## Estrutura atual

```text
consodle/
├── index.html
├── README.md
├── assets/
│   ├── logo.svg
│   ├── icons/
│   │   └── arrow.svg
│   └── images/
│       ├── background-pattern.svg
│       └── button.png
├── css/
│   ├── index.css
│   ├── global.css
│   ├── main.css
│   ├── form.css
│   └── legend.css
├── js/
└── prints-prototipo/
    ├── Desktop - 1.png
    ├── Desktop - 2.png
    └── Desktop - 3.png
```

O arquivo `css/index.css` reúne as importações dos estilos. As variáveis e regras gerais ficam em `global.css`, enquanto os demais arquivos cuidam das áreas da interface. A pasta `js/` está reservada para a implementação da lógica.

## Como visualizar localmente

1. Abra a pasta do projeto no seu editor.
2. Inicie um servidor estático na raiz do projeto — por exemplo, com a extensão Live Server do VS Code, caso esteja instalada.
3. Acesse o endereço local fornecido pelo servidor e abra a página `index.html`.

Nesta etapa, não há dependências npm nem processo de build. As fontes são carregadas pelo Google Fonts e precisam de conexão com a internet; sem ela, o navegador usa as fontes alternativas definidas no CSS.

## Próximas etapas

- [ ] Finalizar os estilos e adaptar a interface para celular.
- [ ] Montar e conferir o catálogo inicial de consoles.
- [ ] Implementar a busca com sugestões.
- [ ] Comparar os atributos e exibir o histórico de palpites.
- [ ] Impedir palpites repetidos e mostrar a mensagem de vitória.
- [ ] Implementar o desafio diário, igual para todos, com um fuso definido.
- [ ] Salvar o progresso da partida no navegador.
- [ ] Revisar a acessibilidade e testar o fluxo completo.
- [ ] Publicar o projeto na internet.

Como a versão inicial será executada inteiramente no navegador, os dados e a resposta poderão ser inspecionados no código. Esse é um limite aceito para o escopo de estudo do projeto.
