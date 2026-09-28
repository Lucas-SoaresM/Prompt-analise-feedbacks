[prompt-analise-feedbacks.md](https://github.com/user-attachments/files/32713895/prompt-analise-feedbacks.md)
# 🏦 Prompt para Análise de Feedbacks: Abertura de Conta Digital

> Desafio de engenharia de prompt da DIO: construir, em 3 passos, um prompt que transforme feedbacks de clientes bancários em insights claros e acionáveis.

## 📌 Sobre o desafio

O objetivo deste desafio é criar um prompt estruturado para que uma IA analise feedbacks de clientes de um banco. O prompt foi construído em três etapas: definição da intenção, inclusão de contexto e restrições, e união de tudo em um prompt final revisado.

## 🎯 Cenário escolhido

Em vez de analisar o banco de forma geral, escolhi um recorte específico: o processo de **abertura de conta digital pelo aplicativo** (onboarding). É uma etapa crítica, porque é o primeiro contato do cliente com o banco, e qualquer atrito pode fazer a pessoa desistir antes mesmo de virar cliente.

As etapas do processo consideradas na análise são:

1. Cadastro
2. Envio de documentos
3. Validação por selfie
4. Aprovação
5. Primeiro acesso

## 🧱 Passo 1: Definindo a intenção

Quero que a IA analise comentários de clientes sobre o processo de abertura de conta digital pelo aplicativo de um banco para identificar em quais etapas os clientes mais travam, desistem ou reclamam.

O resultado será usado pela equipe de produto responsável pelo onboarding para apoiar a decisão de quais etapas simplificar primeiro, reduzindo desistências sem comprometer a segurança.

A entrega deve conter um resumo executivo, uma tabela organizada por etapa do processo com os problemas encontrados e as ações sugeridas, e uma lista das melhorias prioritárias.

O resultado será considerado bom se mostrar com clareza onde está o maior atrito, se cada problema vier acompanhado de evidência nos comentários e se as ações forem práticas e possíveis de executar.

## 🧱 Passo 2: Contexto e restrições

**Contexto:** Estou trabalhando com feedbacks de clientes bancários relacionados à abertura de conta digital pelo aplicativo (cadastro, envio de documentos, validação por selfie, aprovação e primeiro acesso).

**Dados disponíveis:** A base contém data do comentário, sistema do celular (Android ou iOS), etapa em que o cliente estava, status da solicitação (aprovada, pendente ou recusada), texto do feedback e nota de 0 a 10.

**Critérios de análise:** A IA deve classificar os feedbacks por etapa do processo, tema, sentimento e gravidade (se impede a abertura da conta ou apenas causa incômodo).

**Cuidados e restrições:**

- Use apenas os dados fornecidos.
- Não invente números, causas ou conclusões.
- Não exponha nomes, CPF, dados de documentos ou qualquer informação pessoal que apareça nos comentários.
- Não sugira remover etapas obrigatórias de segurança ou de validação de identidade; proponha formas de torná-las mais simples ou mais claras.
- Se houver informação insuficiente, indique a limitação.
- Use linguagem simples, direta e voltada para decisões de produto.

## 🚀 Passo 3: Prompt final

```text
Atue como analista de experiência do cliente especializado em produtos digitais bancários.

Sua tarefa é analisar feedbacks de clientes sobre o processo de abertura de conta digital pelo aplicativo de um banco para identificar as etapas com mais atrito, os motivos de desistência e as oportunidades de simplificação.

Contexto: A análise será usada pela equipe de produto responsável pelo onboarding para decidir quais etapas melhorar primeiro. O objetivo é reduzir desistências e reclamações sem enfraquecer a segurança do processo.

Dados disponíveis: Serão fornecidos comentários com data, sistema do celular (Android ou iOS), etapa em que o cliente estava, status da solicitação (aprovada, pendente ou recusada), texto do feedback e nota de 0 a 10.

Instruções de análise:
1. Classifique os feedbacks por etapa do processo, tema, sentimento e gravidade (impede a abertura ou apenas incomoda).
2. Identifique os principais padrões, problemas, elogios e oportunidades, observando se algum problema aparece mais no Android ou no iOS.
3. Aponte evidências nos dados fornecidos, usando trechos curtos de comentários sem nenhum dado pessoal.
4. Sugira ações práticas para a equipe de produto e, quando o problema envolver validação de identidade, também para o time de segurança.

Formato da resposta: Entregue um resumo executivo com até 5 linhas, uma tabela com as colunas etapa, tema, sentimento, gravidade, evidência e ação sugerida, e uma lista final com as 3 melhorias mais urgentes, explicando em uma frase por que cada uma vem primeiro.

Restrições:
- Use apenas os dados fornecidos.
- Não invente números, causas ou conclusões.
- Não exponha dados pessoais ou sensíveis, como nomes, CPF ou dados de documentos.
- Não recomende eliminar etapas obrigatórias de segurança.
- Informe limitações quando os dados não forem suficientes.
- Use linguagem simples, direta e voltada para tomada de decisão.
```

## 💡 Diferenciais deste prompt

- **Organização por etapa do processo:** em vez de separar os feedbacks por produto, a análise mostra exatamente em que ponto da jornada o cliente enfrenta problemas.
- **Critério de gravidade:** diferencia o que impede a abertura da conta do que é só um incômodo, o que ajuda a priorizar melhor.
- **Comparação entre Android e iOS:** permite descobrir se um problema é técnico e específico de uma plataforma.
- **Segurança preservada:** a IA não pode sugerir cortar a validação de identidade só para deixar o processo mais rápido, o que seria um risco real em um banco.
- **Proteção de dados:** os exemplos de comentários devem aparecer sem nomes, CPF ou dados de documentos.

## 📂 Exemplo de estrutura dos dados

Exemplo fictício, apenas para ilustrar o formato esperado da base:

| Data | Sistema | Etapa | Status | Feedback | Nota |
|------|---------|-------|--------|----------|------|
| 12/09/2026 | Android | Validação por selfie | Pendente | "Tirei a selfie várias vezes e o app sempre diz que a foto ficou escura." | 3 |
| 14/09/2026 | iOS | Envio de documentos | Aprovada | "Demorou, mas deu certo. Só achei confuso saber qual lado do documento enviar primeiro." | 7 |
| 15/09/2026 | Android | Primeiro acesso | Aprovada | "Conta aprovada rápido, mas não recebi o código por SMS para entrar." | 4 |

## 🛠️ Como usar

1. Copie o prompt final da seção acima.
2. Cole em uma ferramenta de IA generativa.
3. Logo abaixo do prompt, cole ou anexe a base de feedbacks com os campos descritos.
4. Revise a resposta e confira se as evidências citadas realmente aparecem nos dados.

---

Desenvolvido por Eduardo como parte de um desafio da DIO.
