 # 🤖 Engenharia de Prompts - Cartório-Check IA

Neste projeto, a LLM é utilizada em três momentos cruciais para garantir a eficiência e a segurança jurídica.

## 1. Módulo de Anonimização (LGPD)
**Utilização:** Antes de processar qualquer reclamação, os dados são enviados para a LLM com esta instrução:
> "Atue como um especialista em proteção de dados. Analise o texto abaixo e substitua nomes de pessoas, CPFs e números de matrículas por [DADO_PROTEGIDO]. Retorne apenas o texto limpo."

## 2. Módulo de Classificação de Criticidade
**Utilização:** Para identificar a queda do site.
> "Analise o feedback do cliente anonimizado. Se houver menção a 'site não carrega', 'erro no link' ou 'indisponibilidade', classifique como [CRÍTICO]. Caso contrário, classifique como [SUPORTE_COMUM]."

## 3. Geração de Insight para o Gestor
**Utilização:** Para criar o resumo que aparece no Dashboard do Lovable.
> "Com base nas últimas 10 reclamações críticas, gere um resumo de duas linhas para o Oficial do Cartório explicando qual a provável causa raiz da instabilidade técnica."
