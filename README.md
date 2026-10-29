# Assistente de Candidaturas com IA

Agente de IA generativa que ajuda quem está se candidatando a vagas iniciais e estágios a adaptar o currículo para cada vaga.

## O problema

Cada vaga pede um currículo um pouco diferente, e é difícil saber o que destacar, o que está faltando e como se preparar para a entrevista.

## O que ele faz

Você cola a descrição de uma vaga e o seu currículo. O assistente devolve:

- compatibilidade entre os dois (de 0 a 100%)
- pontos fortes do currículo para aquela vaga
- o que falta mostrar, com sugestões práticas
- palavras-chave da vaga que podem ser usadas, se forem verdadeiras
- resumo adaptado para o topo do currículo
- carta de apresentação (até 150 palavras)
- cinco perguntas prováveis de entrevista, com dicas de resposta

## Regras do assistente

A principal regra que defini nas instruções da IA: **nunca inventar experiências, cursos, ferramentas ou resultados** que não estejam no currículo. Se algo falta, ele aponta como lacuna em vez de preencher.

## Como foi construído

- Interface em HTML, CSS e JavaScript, em um único arquivo (`assistente-candidaturas.html`)
- IA generativa (Claude) para analisar a vaga e o currículo e responder em formato JSON, que a página transforma em cartões
- Defini o problema, as instruções da IA e o formato da resposta, e testei com o meu próprio currículo e com vagas reais
- Desenvolvido com apoio de IA (Claude), como parte do meu estudo de IA generativa

## Aprendizados

- Instruções claras e regras explícitas (como "não invente") mudam muito a qualidade da resposta
- Colar a vaga inteira, com trilhas diferentes misturadas, derruba a nota: o assistente cobra requisitos de uma trilha que não é a da pessoa. Testar com o trecho certo da vaga deu um resultado bem mais realista (de 15% para 62% no meu currículo)

## Limitações

- A parte de IA funciona dentro do ambiente do Claude (artefatos). Fora dele, a página abre, mas não gera a análise
- A pontuação é uma estimativa da IA, não a nota real de nenhum processo seletivo
- Sempre revise os textos gerados antes de enviar

## Próximos passos

- Perguntar a trilha da vaga antes de analisar
- Criar automações e dashboards para completar o portfólio

## Autora

Mirella Maria dos Reis · [LinkedIn](https://www.linkedin.com/in/mirella-reis-33342b1ba)
