# ANÁLISE DE DADOS E APRENDIZADO DE MÁQUINA
# Autores: Daniella Glaete, Júlio Coutinho e Marcos Antônio

O Uso de IA Generativa para Análise de Infração Eleitoral em Postagens em Redes Sociais de Agentes Políticos

Análise do desempenho da inteligência artificial generativa na 
detecção de pedidos de voto antecipados na redes sociais de 
políticos

RESUMO. Nas eleições brasileiras, um caso cada vez mais comum de denúncias é o uso das redes sociais para 
cometer infrações eleitorais. Muitos políticos utilizam seus perfis nas redes sociais como ferramentas de 
campanha para aumentar seu poder de persuasão e a conversão de eleitores. As infrações mais graves envolvem 
o pedido antecipado de votos durante um período não permitido, no qual políticos são denunciados à Justiça 
Eleitoral Brasileira para a apuração da infração, onde seu maior desafio é conseguir monitorar todas as denúncias 
e aplicar as penalidades adequadas. O objetivo desta pesquisa é investigar a eficácia de diferentes abordagens 
de IA Generativa para identificar infrações eleitorais em vídeos, nos quais as transcrições são avaliadas por vários 
modelos de IA com diferentes estruturas de prompt. Uma vez identificados a estrutura de prompt e o modelo de IA 
Generativa mais eficazes, o objetivo é auxiliar a Justiça Eleitoral brasileira e outros órgãos de fiscalização no 
processo de monitoramento e punição de violações da legislação brasileira, a fim de desencorajar políticos a 
cometer essa infração.
 Palavras chaves: Inteligência Artificial, Violação eleitoral, Redes Sociais, Supervisão eleitoral.

O projeto avalia o uso de Inteligência Artificial Generativa para detectar infrações eleitorais em vídeos. Este estudo foi baseado no trabalho de Glaete, Coutinho e Teci (2025) da UFRPE.

Nós analisamos 108 vídeos, testando 6 modelos de IA diferentes e 3 estratégias de prompt (One-shot, Few-shot e Chain of Thought, o famoso CoT).
No total, foram 18 experimentos avaliados por métricas de precisão, recall e F1-Score."

O modelo GPT-4o na estratégia Few-shot alcançou o melhor F1-Score de 0,9286.

A família de modelos GPT lidera o ranking geral de performance com um F1 médio de 0,914.

A Melhor Estratégia de Prompt: Foi o One-shot obteve a melhor média geral com 0,907, superando abordagens mais complexas como o CoT.

A Amostra: Dos 108 vídeos analisados, apenas 19 continham infrações reais e 89 eram negativos.

A Divergência: Tivemos 11 casos de divergência (10,2%) onde os modelos discordaram entre si sobre a existência de infração.

Agora, o insight mais importante deste projeto, que envolve o Desbalanceamento de Classes:

Temos quase 5 vezes mais vídeos sem infrações do que com infrações (89 contra 19). 
Em cenários jurídicos e de conformidade eleitoral, o Recall (a capacidade da IA de achar a infração e não deixar passar) 
é a métrica mais importante! Um falso negativo significa uma infração grave não detectada.

Por exemplo, o modelo Gemini na estratégia Few-shot teve um Recall de apenas 0,676. 
Isso significa que ele deixaria passar mais de 30% das infrações! Portanto, para aplicação real, focar apenas em acurácia ou precisão é um perigo. Precisamos buscar modelos com alto Recall.

Próximos Passos: Para projetos futuros, recomendo aplicar técnicas de clusterização (como K-Means) para agrupar o comportamento dos modelos e identificar outliers de performance com mais clareza.

