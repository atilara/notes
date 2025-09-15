### Leitura e análise de artigos recomendados por George

##### Children’s Rights, not Deceptive Patterns by Design: a Requirements Perspective (George Valença, João Silva, et al)
###### Resumo:
- Analisa como padrões de design manipulativo impactam requisitos legais de software de proteção de crianças e bem estar online, baseado em diretrizes da UNICEF
- Indica como empresas de TI negligenciam esses requisitos
- Analisa medidas de segurança essencial para implementação de novas funcionalidades

###### Pontos importantes
Ao longo do trabalho, são apresentados os *Legal Requirements* (LRs), agrupados por algumas categorias, sendo:
- *Platform Governance*
- *Development and Well-being*
- *Security and Privacy*
- *Data management*

Utiliza taxonomia de *Harry Brignull* para avaliar quais padrões de design manipulativo são aplicados pelas empresas de TI em cada requisito legal, demonstra isso numa tabela.

Aborda quais mudanças precisam ser feitas nas aplicações para que cada categoria dos requisitos passem a ser respeitadas.

Faz protótipos de exemplo indicando mudanças que removem as práticas de design manipulativo em jogos, aplicativos, etc. utilizados por crianças.

Trabalho conclui que as empresas não tem respeito por praticar o que é melhor para as crianças pois aplicam práticas de design manipulativo de forma deliberada.

###### Trabalhos futuros
- Pesquisas em domínios mais específicos, como design manipulativo em robôs sociais, como o *Lovot*, e em redes sociais
- Interpretação de como essas práticas impactam os LRs de jogos, robôs sociais e brinquedos inteligentes
- Discussão com especialistas
- Organização de um workshop com crianças para identificar padrões de design manipulativo e criar materiais informativos sobre

##### Is My Child Safe Online?- On Requirements for ParentalControl Tools in Apps used by Children (João Assis, George Valença)

###### Resumo:
- Pesquisa destrincha vários requisitos funcionais e não funcionais para ferramenta de controle parental e analisa se o *Instagram* e *TikTok* suprem esses requisitos
- Foi conduzida uma Revisão Sistemática da Literatura (RSL) para encontrar pesquisas que destrinchassem diretrizes para requisitos importantes para o controle parental
- Com base nas diretrizes, foram criados os requisitos

###### Pontos importantes
Metodologia envolveu RSL para criação dos requisitos funcionais e não funcionais

Os dados coletados da plataforma foram baseados no uso, outros artigos, documentação das plataformas.

A lista de requisitos funcionais construídos no artigo foram categorizados em:
- *Children’s Safety*
- *Platform-Parent-Child’s Dialogue*
- *Restriction and monitoring*
- *Parent-Child Privacy*

A lista de requisitos não funcionais foram categorizados em:
- *Ethical*
- *Operational*
- *Security*
- *Usability*

Além disso, outras contribuições do artigo para literatura foram os estudos de caso do *Instagram* e *TikTok* que concluíram que eles cumprem a maioria dos requisitos de forma pacial, e não cumprem outros.

###### Trabalhos futuros:
- Analisar literatura cinza, documentos governamentais, portais de notícias de TI, especialistas
- Discutir os resultados com representantes das duas empresas

### Possíveis temas

###### Auditoria de requisitos no Metaverso
- Aplicar uma metodologia semelhante ao segundo artigo no contexto do Metaverso, como *Roblox* e *Fortnite Creative*
- Analisar tópicos como "Moderação de Conteúdo Gerado pelo Usuário" e/ou "Interações Econômicas e Microtransações"
- Estudo de caso em um dos jogos citados
- Mapear quais requisitos são atendidos, parcialmente atendidos ou não atendidos, gerando uma análise crítica e recomendações
- Preocupação com necessidade de comitê de ética, ou o tema pode ser mais voltado para o que os pais vêem como necessário para esse controle, com menos foco na criança. *Eu, como pai, preciso que...*

######  Auditoria de requisitos em plataformas educacionais
- Professores não possuem as ferramentas necessárias para avaliar se aplicações disponibilizadas por EdTechs cumprem requisitos de segurança, privacidade, ou se são pedagogicamente adequadas
- O objetivo seria levantar quais requisitos os professores teriam para que a aplicação seja adequada para uso
- Metodologia poderia envolver entrevistas, etc.
- Possível overlap que impossibilitaria esse artigo: *Ethical Design for Edtechs Platforms – an Analysis of Google Classroom via a Code of Design Practices* de Steffano

###### Auditoria dos Mecanismos de Verificação Etária para a Proteção de Crianças em Plataformas Digitais

- Revisão do tema
	- Revisão sistemática da literatura
	- Analisar documentos de órgãos reguladores, leis, notícias
- Construção de requisitos que definam uma ferramenta de verificação de idade adequada
	- Funcionais
	- Não funcionais
- Levantar tópicos como privacidade, usabilidade, segurança, transparência
- Possível estudo de caso em alguma plataforma. *TikTok*, *Roblox*, *Discord*, etc
- Conclusão com análise sobre o estado atual do processo de verificação etária