 # 🤖 Engenharia de Prompts - Cartório-Check IA

Neste projeto, a LLM é utilizada em três momentos cruciais para garantir a eficiência e a segurança jurídica.

## 1. Módulo de Anonimização (LGPD)
**Utilização:** Antes de processar qualquer reclamação, os dados são enviados para a LLM com esta instrução:
> "Atue como um especialista em LGPD e proteção de dados. Analise o texto abaixo e substitua nomes de pessoas, CPFs e números de matrículas pelo marcador [DADO_PROTEGIDO]. Retorne apenas o texto anonimizado."

## 2. Módulo de Classificação de Criticidade
**Utilização:** Para identificar a queda do site.
> "Você é um analista de suporte de um Cartório de Registro de Imóveis. Analise a mensagem anonimizada. Se o cliente relatar que o site não abre, link quebrado, erro no e-protocolo ou indisponibilidade, classifique como 'CRÍTICO - SITE FORA'. Se for qualquer outro assunto, classifique como 'NORMAL'."

## 3. Geração de Insight para o Gestor
**Utilização:** Para criar o resumo que aparece no Dashboard do Lovable.
> "Crie um dashboard administrativo para um Cartório com um banner de status que muda de cor (verde para normal, vermelho para crítico) com base em alertas de IA sobre queda do site."
> "Com base nas últimas 10 reclamações críticas, gere um resumo de duas linhas para o Oficial do Cartório explicando qual a provável causa raiz da instabilidade técnica."
