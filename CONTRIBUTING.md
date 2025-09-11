# Contributing
Este é um projeto totalmente livre que aceita contribuições via pull requests no GitHub. Este documento tem a responsabilidade de alinhar as contribuições de acordo com os padrões estabelecidos no mesmo. Em caso de dúvidas, [abra uma issue](https://github.com/UnBArqDsw2025-2-Turma02/2025.2_T02_G6_AquiTemFCTE_Entrega_02/issues/new/choose).

Observe que também temos um [Código de Conduta](./CODE_OF_CONDUCT.md). Siga-o em todas as suas interações relacionadas ao projeto.

## Política de Branch's:

Para garantir a organização e a qualidade do nosso código, adotamos a política de GitHub Flow.

### Como funciona o GitHub Flow?

O GitHub Flow é uma política de desenvolvimento simples, baseada em um único branch principal, o `main`. Toda feature, correção de bug ou melhoria é desenvolvida em uma **branch separada** criada a partir da `main`. Quando o trabalho está pronto, um **Pull Request (PR)** é aberto. Após a revisão do código (Code Review) e a aprovação dos membros da equipe, o PR é **mesclado** de volta para a branch `main`. O `main` é considerado sempre a versão **pronta para deploy**, o que significa que ele deve estar sempre estável.

### Exigências para Contribuições

Para contribuir, siga os seguintes passos:

1. **Crie sua branch**: Sempre crie uma branch a partir da `main`. Para garantir a clareza, use um prefixo que descreva o tipo de alteração, seguido de um nome descritivo (separado por `/`).
- Exemplo: `feat/nova-funcionalidade` ou `fix/erro-de-login`.

2. **Prefixos mais comuns**:
- `feat/`: Para novas funcionalidades. Exemplo: `feat/adicionar-autenticacao`.
- `fix/`: Para correções de bugs. Exemplo: `fix/corrigir-validacao-formulario`.
- `docs/`: Para mudanças apenas na documentação. Exemplo: `docs/atualizar-readme`.
- `style/`: Para mudanças de formatação (espaçamento, ponto e vírgula, etc.) que não afetam a lógica do código. Exemplo: `style/formartar-codigo`.
- `refactor/`: Para refatorações de código que não adicionam funcionalidades ou corrigem bugs. Exemplo: `refactor/otimizar-funcao-de-busca`.
- `chore/`: Para atualizações na build, dependências ou tarefas de manutenção sem relação direta com o código do projeto. Exemplo: `chore/atualizar-dependencias`.
- `test/`: Para a adição ou atualização de testes (unitários, de integração, etc.). `Exemplo: test/adicionar-testes-login`.
- `perf/`: Para melhorias de performance. Exemplo:` perf/otimizar-carregamento-imagens`.

3. **Desenvolva sua funcionalidade ou correção**.

4. **Abra um Pull Request**:
- Quando seu trabalho estiver pronto e você quiser mesclá-lo, abra um Pull Request.
- No título do PR, use um prefixo que indique o tipo da sua alteração (`feat:`, `fix:`, `docs:`, etc.).
- Na descrição do PR, explique detalhadamente as mudanças realizadas, seguindo o template exibido e indicando as `issues` relacionadas (se houver).
- **Não mescle o seu próprio PR**. Aguarde a revisão de pelo menos um mantenedor do projeto.

5. **Mantenha a `main` limpa**:
- A branch `main` é sagrada! Ela representa o código que está em produção (ou pronto para ir).
- **NUNCA faça commits diretamente na `main`**.
- Não mescle Pull Requests que quebrem os testes ou o bom funcionamento do projeto.

## Política de Commits:

Para mantermos um histórico de commits claro, consistente e legível, adotamos a política de **Conventional Commits**. Essa abordagem facilita o rastreamento de mudanças, a geração automática de release notes (caso venha a ser utilizado) e a automação de outras ferramentas.

### Como funciona o Conventional Commits?

Cada commit deve ter uma estrutura bem definida, composta por **tipo**, **escopo** _(opcional)_ e **descrição**. Essa padronização permite que qualquer pessoa entenda, de forma rápida e precisa, o que foi feito em cada alteração.

### Exigências para Commits

Ao fazer um commit, siga a seguinte estrutura:

```
<tipo>(<escopo>): <descrição>
```

1. **Tipo (`<tipo>`)**

Este é o prefixo obrigatório que indica o tipo de mudança. Use os mesmos prefixos que usamos para nomear as branches, como:
- `feat`: Uma nova funcionalidade.
- `fix`: Uma correção de bug.
- `docs`: Mudanças na documentação.
- `style`: Mudanças de formatação que não alteram a lógica do código (espaçamento, ponto e vírgula, etc.).
- `refactor`: Mudança no código que não adiciona uma funcionalidade nem corrige um bug.
- `chore`: atualizações de tarefas de build, configurações de administrador ou pacotes.
- `test`: Adição ou atualização de testes.
- `perf`: Melhorias de performance.
- `ci`: Mudanças nos arquivos e scripts de integração contínua (CI).
- `revert`: Reverte um commit anterior.
- `build`: utilizados quando são realizadas modificações em arquivos de build e dependências.

2. **Escopo (`(<escopo>)`)**

O escopo é opcional e serve para especificar a parte do projeto que foi alterada. Use um nome claro para o módulo ou componente.
- **Exemplo:** `feat(autenticacao): adicionar login com email`.
- **Exemplo:** `fix(carrinho): corrigir bug ao remover item`.

3. **Descrição (`<descrição>`)**

A descrição é um breve resumo da mudança. Mantenha-a concisa (no máximo 50 caracteres) e no modo imperativo.
- **Exemplo:** feat: adicionar suporte a i18n.
- **Exemplo:** fix: corrigir erro de validação no formulário.

4. **Mensagem Completa**

Se precisar de mais detalhes, você pode adicionar um corpo de mensagem (`<body>`) e um rodapé (`<footer>`) para incluir informações como breaking changes (`BREAKING CHANGE`) ou referências a _issues_.

- **Mensagem de Exemplo:**

```
feat(autenticacao): adicionar suporte a login social

Adiciona a funcionalidade de login via Google e GitHub, utilizando o
pacote `passport-social`.

BREAKING CHANGE: O antigo sistema de autenticação de usuários foi
substituído.

Closes #123
```

## Política de Pull Requests:

Um Pull Request (PR) é a forma oficial de propor mudanças ao nosso projeto. Para garantir a organização e agilizar o processo de revisão, é **OBRIGATÓRIO** utilizar o [Template de Pull Request](./.github/pull_request_template.md) fornecido.

Siga estas instruções para preencher o template corretamente:
1. **Título do PR**: O título deve seguir o padrão de **Conventional Commits** (ex: `feat: add user authentication`). Isso garante que o título do seu PR seja consistente com o histórico de commits do projeto
2. **Tipo da sua alteração**: Marque com um `x` o prefixo que melhor descreve a sua mudança. **Atenção:** Selecione apenas os tipos que realmente se aplicam, pois isso é fundamental para a organização do nosso código.
3. **Descrição**: Descreva em detalhes as alterações que você fez. Explique o problema que você está resolvendo e por que sua solução é a melhor abordagem. Isso ajuda os revisores a entenderem o contexto da sua contribuição.
4. **Issue Relacionada**: Todo PR deve estar vinculado a uma `issue` no nosso repositório. Use a sintaxe `Closes #<número_da_issue>` para que o GitHub feche a `issue` automaticamente assim que seu PR for mesclado.
5. **Checklist de Checagem**: Antes de enviar, complete o checklist. Isso garante que sua contribuição está pronta para ser revisada, sem erros de formatação, e que os testes e a documentação foram atualizados.
6. **Capturas de Tela**: Se a sua mudança envolve a interface do usuário, adicione capturas de tela ou GIFs. Isso facilita muito a visualização da sua alteração.

**Atenção**: Seu PR **NÃO** será mesclado sem a aprovação de pelo menos um dos mantenedores do projeto ou depadronização com o [Template de Pull Request](./.github/pull_request_template.md) oferecido. O processo de **Code Review** é essencial para a qualidade do nosso código. Seja paciente e responda a qualquer feedback dos revisores.

## Obrigado pela sua contribuição!
Agradecemos imensamente por sua vontade de contribuir para este projeto. Ao seguir estas diretrizes, você não apenas melhora a qualidade do nosso código, mas também torna o processo de colaboração mais agradável e produtivo para todos. Sua dedicação e respeito aos padrões estabelecidos são fundamentais para o sucesso contínuo do projeto.