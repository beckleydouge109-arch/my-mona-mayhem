<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Crie o jogo com fluxos de trabalho agênticos

---

Nesta parte, o Copilot passa do planejamento para a implementação. Em vez de escrever código linha por linha, você descreve o que quer e deixa o Copilot trabalhar nos arquivos necessários.

## Tarefa 1: Conecte a batalha

<!-- track:vscode:start -->
1. Mude para o modo **Agent** no Copilot Chat.
2. Insira este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Retorne ao fluxo de programação padrão do Copilot CLI (ou continue no modo autopilot se quiser que o Copilot siga trabalhando até você pará-lo).
2. Se for útil, mencione o arquivo da página para dar mais contexto: `@src/pages/index.astro`.
3. Insira este prompt:
<!-- track:cli:end -->

   > Adicione JavaScript do lado do cliente à página de batalha para que:
   > 1. Ao clicar no botão Battle, obtenha os dois nomes de usuário dos campos.
   > 2. Valide se ambos foram preenchidos e exiba um erro caso contrário.
   > 3. Busque em paralelo, pela nossa API, os dados de contribuição dos dois usuários.
   > 4. Renderize os gráficos de contribuição como grades coloridas: cada dia deve ser um quadrado colorido usando a paleta do GitHub.
   > 5. Exiba um selo VS entre os dois usuários.
   > 6. Mostre o nome de usuário, o total de contribuições e o intervalo de datas de cada usuário.
   > 7. Gerencie os estados de carregamento e os erros.
   > 8. Inicie a batalha também ao pressionar Enter nos campos.
   > 9. Por enquanto, use a interface simples que já está montada.
   >
   > Use interfaces do TypeScript para a estrutura dos dados de contribuição.

<!-- track:vscode:start -->
3. Deixe o Agent Mode implementar as alterações em `index.astro`.
4. Revise as alterações propostas na visualização de diff antes de aceitá-las.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deixe o Copilot CLI trabalhar em `src/pages/index.astro`.
5. Use `/diff` para revisar as alterações geradas e, em seguida, aprove-as.
<!-- track:cli:end -->

## Tarefa 2: Teste a batalha

> **⚠️ Não está vendo as alterações?** Se a página de batalha não tiver sido atualizada, pare o servidor (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador.

1. Digite `octocat` e `torvalds` como os dois nomes de usuário e clique em **Battle**.
2. Você deve ver os dois gráficos de contribuição lado a lado, com grades coloridas.
3. Teste os casos de erro:
   - Deixe um ou ambos os campos vazios e clique em Battle: deve aparecer um erro de validação.
   - Digite um nome de usuário inválido: o app deve exibir um erro da API.
4. Pressione **Enter** em qualquer campo: isso deve iniciar a batalha como se você tivesse clicado no botão.

## Tarefa 3: Itere com o Copilot

Se algo não estiver exatamente como você quer, envie feedback diretamente ao Copilot. Por exemplo:

- *“Os quadrados de contribuição estão grandes demais; deixe-os com 12 × 12 px.”*
- *“Adicione uma dica ao passar o cursor que mostre a data e a contagem de contribuições.”*
- *“O estado de carregamento precisa de uma animação pulsante.”*

<!-- track:vscode:start -->
O Agent Mode gerencia naturalmente as alterações em vários arquivos e as iterações. Cada prompt de acompanhamento se baseia na conversa anterior, permitindo refinar a implementação aos poucos sem começar do zero.
<!-- track:vscode:end -->

<!-- track:cli:start -->
As sessões do Copilot CLI mantêm o histórico, então cada prompt de acompanhamento se baseia no anterior. Use `/session` ou `/context` para inspecionar o contexto atual e execute `/review` após uma iteração maior para procurar erros ou melhorias.
<!-- track:cli:end -->

## Dicas para esta parte

- **Seja específico sobre o que você quer**: requisitos claros levam a resultados melhores.
- **Divida tarefas grandes em prompts menores** se o Copilot sair do rumo.
- **Revise as alterações antes de aceitá-las**: é mais rápido inspecionar o código gerado do que reescrevê-lo.
- **Teste o app após cada etapa de implementação** para localizar os problemas rapidamente.

## ✅ Parte 3 concluída

Você aprendeu a:

- Usar o Copilot para **implementar alterações em vários arquivos**
- **Iterar nos resultados** com feedback objetivo
- Percorrer o **ciclo completo de uma funcionalidade**: implementação, revisão, testes e refinamento
