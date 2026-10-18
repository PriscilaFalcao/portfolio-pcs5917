
**Notícia** "O ASCII smuggling passa da injeção imediata de IA para a evasão de phishing". Disponível em: <https://www.microsoft.com/en-us/security/blog/2026/09/03/ascii-smuggling-crosses-over-from-ai-prompt-injection-to-phishing-evasion/>.

O caso trata da descoberta por pesquisadores da Microsoft de uso de carcteres unicode invisíveis para phising. Técnica usada para ataques de prompt injection, na qual esses caracteres especiais escondem instruções de humanos e permitem ser reconhecidos em modelos LLM ou NLP, foi reutilizada para fraudar sistemas de detecção de phishing por meio de ataque de evasão.

Foram encontrados milhões de e-mails com o uso de caracteres unicode para temas financeiros pela telemetria do Microsoft Defender para Office 365, durante o período observado (9 de fevereiro a 18 de junho de 2026). A Microsoft classificou o ataque na categoria AML.T0068 - LLM Prompt Obfuscation (MITRE ATLAS).

Apesar de ser uma publicação para exaltar a solução proposta pela empresa (Microsoft Defender), nota-se que a pesquisa trouxe luz para um problema real de segurança, na qual mesmo com um contexto limitado para observação (buscaram apenas e-mails com temas financeiros), um número expressivo de e-mails apresentava vulnerabilidade com características do ataque. Adicionado a isso, ainda percebe-se um comportamento ainda mais curioso com a redução das campanhas de ataques do tipo (não as de phishing, redução nos ataques com abordagem de ASCII smuggling) durante o período, que não necessariamente teve correlação com a solução da empresa, mas que sofreu essa mudança de comportamento, mesmo sendo tão regular (acontecia sempre nos dias úteis e em volumes similares diariamente, como se fosse tarefa automatizada).


**Artigo** "Detection and prevention of evasion attacks on machine learning models" [1]:

O trabalho explora ataques de evasão em modelos de machine learning (dando foco nos ataques FGSM e PGD), além de propor framework de defesa baseado no ciclo de vida de um modelo (etapa de pre-prcessamento do input, pós-processamento na saída e pós-produção). As avaliações eram feitas por meio de cenários adaptados de ataques white-box, usando ResNet50V2, além do Toolbox da IBM de Robustez Adversarial. 

Estas metodologias e soluções propostas pelo trabalho poderiam contribuir para a prevenção e detecção desses ataques, principalmente com o uso das tecnicas propostas no framework de spatial smoothing, feature squeezing, treinamento adversarial para aumentar a resiliência do modelo e testes para aprimorar a robustez.


[1] Muthalagu, R., Malik, J. and Pawar, P.M., 2025. Detection and prevention of evasion attacks on machine learning models. Expert Systems with Applications, 266, p.126044.
