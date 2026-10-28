<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematização com foco no design

---

Nesta parte, você vai usar os ciclos de planejamento e implementação do Copilot para projetar uma transformação completa do tema. Essa é uma abordagem de desenvolvimento com foco no design: comece com a visão, itere nos elementos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para o modo **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Insira este prompt:

> Quero transformar esta página em uma experiência completa de fliperama retrô. Planeje uma reformulação visual que inclua efeitos de linhas de varredura CRT no fundo, brilho neon pulsante no título, selo VS animado com mudanças nas cores do gradiente, camada de brilho cintilante sobre os cartões de resultado, animações de entrada flutuante nos campos, texto de carregamento que alterne entre verde e roxo e efeitos de brilho ao passar o cursor pelos quadrados de contribuição. Mantenha o fundo escuro (`#0a0a1a`) e use verde (`#5fed83`) e roxo (`#8a2be2`) como cores de destaque. Use o tema escuro e a fonte retrô Press Start 2P do Google Fonts.

O Copilot vai gerar um plano detalhado de implementação que abrange todos os efeitos visuais. **Não aceite imediatamente**: revise o plano e itere:

- Sugira ajustes no tempo das animações (por exemplo, “Deixe o pulso neon mais lento, com cerca de 3 segundos”).
- Pergunte sobre efeitos específicos (por exemplo, “Como vai funcionar a camada cintilante nos cartões?”).
- Peça mudanças na abordagem se algo não parecer adequado.

## Tarefa 2: Implemente o tema

Quando estiver satisfeito com o plano, peça ao Copilot para implementá-lo.

> Implemente o plano do tema de fliperama retrô que acabamos de criar.

O Copilot vai adicionar várias animações CSS, pseudo-elementos e transições à folha de estilos. Isso pode incluir:

- `@keyframes` para linhas de varredura, pulso neon, brilho cintilante e efeitos de entrada flutuante.
- Pseudo-elementos (`::before`, `::after`) para criar efeitos de sobreposição.
- Propriedades personalizadas do CSS para as cores do tema.
- Transições e estados ao passar o cursor pelos elementos interativos.

<!-- track:cli:start -->
Quando as alterações forem aplicadas, use `/diff` para revisar os estilos antes de aprová-los.
<!-- track:cli:end -->

## Tarefa 3: Ajuste o visual

> **⚠️ Não está vendo as alterações?** Se o novo tema ou as animações não aparecerem, pare o servidor (`Ctrl+C`), reinicie com `npm run dev` e atualize a página forçando o recarregamento (`Ctrl+Shift+R`).

Mantenha a prévia do navegador aberta e itere no design. Experimente prompts como:

> O efeito de linhas de varredura está forte demais; reduza a opacidade para 0.03.

> Adicione uma cintilação elétrica sutil ao texto do título.

> O selo VS deve pulsar com mais intensidade.

Essa é uma **abordagem de desenvolvimento com foco no design**: você está iterando no resultado visual em tempo real. Cada prompt refina a experiência até que fique do jeito certo. Não se contente com “bom o suficiente” — continue ajustando até a página parecer saída de um fliperama.

## Tarefa 4: Atualize as instruções

As instruções devem refletir as principais decisões de design para manter os próximos prompts alinhados.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Adicione ao `copilot-instructions.md` uma seção de guia de design que descreva o tema de fliperama retrô: cores, fontes e estilo das animações.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Atualize as instruções do repositório com um guia curto de design para o tema de fliperama retrô: cores, fontes, estilo das animações e a regra de que a nova interface deve manter a estética neon.
<!-- track:cli:end -->

Quando a página estiver como você quer, faça commit das instruções e das alterações de design.

## ✅ Parte 4 concluída

**O que você aprendeu:**

- Usar fluxos de planejamento para criar um **sistema de design antes da implementação**.
- **Iterar no resultado visual** com prompts de acompanhamento.
- **Atualizar as instruções após decisões importantes** para preservar a identidade visual.
