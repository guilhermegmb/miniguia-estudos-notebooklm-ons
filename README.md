miniguia-estudos-notebooklm: Previsão de Carga Elétrica com IA
Contexto e Objetivos
Contexto
Este projeto visa atender ao desafio da DIO. A proposta é desenvolver um caderno temático no NotebookLM, utilizando a Inteligência Artificial como ferramenta de aprendizagem ativa, e documentar todo o processo em um repositório GitHub.

Aproveitando a formação em Engenharia Elétrica e o interesse em análise de dados, o projeto se concentrará na previsão de carga elétrica com dados reais do Operador Nacional do Sistema Elétrico (ONS). Esta abordagem estratégica busca unir o conhecimento técnico em engenharia com as habilidades analíticas demandadas pelo mercado financeiro, demonstrando uma compreensão aprofundada de um setor crucial para investimentos, como o de energia. A previsão de carga elétrica é um fator determinante para a precificação de energia, avaliação de ativos de geração e transmissão, e gestão de riscos em portfólios de investimento.

Objetivos de Estudo
Os objetivos de estudo com este material são:

•	Demonstrar proficiência na aplicação de técnicas de Engenharia de IA e Machine Learning para problemas do mundo real, especificamente na previsão de séries temporais.
•	Construir um portfólio técnico robusto, com um projeto de ponta a ponta que abranja desde a exploração de dados brutos até a preparação para modelos de ML.
•	Desenvolver habilidades em curadoria de fontes e organização do conhecimento, utilizando o NotebookLM como ferramenta central.
•	Aprimorar a engenharia de prompts para extrair informações relevantes e insights de modelos de linguagem, documentando o processo de iteração e resolução de problemas.
•	Criar um miniguia de estudo abrangente sobre previsão de carga elétrica, incluindo resumos estruturados, glossário de termos e prompts reutilizáveis.
•	Conectar o conhecimento técnico de Engenharia Elétrica com as necessidades do mercado financeiro, destacando a relevância da análise de dados de energia para a tomada de decisões de investimento.

Curadoria de Fontes
Para a construção deste caderno temático, foram selecionadas as seguintes fontes, que servirão de base para o estudo e aprofundamento nos conceitos de previsão de carga elétrica, engenharia de IA e Machine Learning:

1	Ebook: Engenharia de IA na Prática: Do laboratório à produção: previsão de carga elétrica com dados reais do ONS [5]
◦	Autor: Guilherme Braga
◦	Ano: Julho de 2026
◦	Descrição: Este ebook é a fonte primária do projeto, detalhando o ciclo completo de um projeto de ML, desde a exploração de dados do ONS, pipeline de limpeza, treino de modelos com MLflow, até a criação de APIs com FastAPI. Ele serve como um guia prático e conceitual, com analogias de engenharia e códigos comentados.
2	Usando IA para prever o consumo de energia no Brasil com Python [1]
◦	Fonte: AnaliseMacro.com.br
◦	Descrição: Artigo que aborda a aplicação de IA para previsão de consumo de energia no contexto brasileiro, utilizando Python. Complementa o ebook com uma perspectiva prática e focada no cenário nacional.
3	Previsão de Carga Elétrica para o Horizonte de Curto Prazo via Redes Neurais Artificiais Utilizando C++ e Python [2]
◦	Fonte: ResearchGate / SBA (Sociedade Brasileira de Automática)
◦	Descrição: Artigo científico que explora a previsão de carga elétrica de curto prazo utilizando Redes Neurais Artificiais, com implementação em Python. Oferece uma visão mais aprofundada sobre modelos específicos e sua aplicação.
4	Desenvolvimento de programa em Python para análise de qualidade de energia elétrica: análise direcionada pelos procedimentos de rede do ONS [3]
◦	Fonte: Repositório Institucional da UFSC
◦	Descrição: Trabalho de Conclusão de Curso que detalha o desenvolvimento de um programa em Python para análise de qualidade de energia elétrica, com foco nos procedimentos do ONS. Relevante para entender a manipulação e análise de dados provenientes do ONS.
5	Carga de Energia Diária - Conjunto de dados [4]
◦	Fonte: Dados Abertos ONS (Operador Nacional do Sistema Elétrico)
◦	Descrição: Portal oficial do ONS que disponibiliza os dados de carga por subsistema em base diária. Essencial para a obtenção dos dados reais que serão utilizados no projeto.

Engenharia de Prompts e "Cicatrizes"
Esta seção documenta as perguntas estratégicas elaboradas para o NotebookLM, as variações de prompts testadas, as respostas obtidas e as lições aprendidas (cicatrizes) durante o processo de interação com a IA.

Jornada de Engenharia de Prompt no NotebookLM
Pergunta Estratégica	Resposta e Raciocínio Obtido	"Cicatriz" / Troubleshooting
"Explique o conceito de previsão de carga elétrica para alguém da área financeira."	A IA comparou a previsão ao planejamento de demanda e gestão de ativos. Destacou o impacto no CAPEX (expansão) e OPEX (operação diária), além da importância para trading de energia [6].	Ajuste de Contexto: Inicialmente a IA focou muito em física. Foi necessário refinar o prompt para que ela usasse analogias de mercado financeiro, como "volatilidade" e "gestão de risco".
"Resuma os principais métodos de previsão de séries temporais presentes nas fontes."	Foram identificados métodos como RNAs (MLP, LSTM), Modelos Estatísticos (ARIMA, MSTL), e Algoritmos de ML (XGBoost, Random Forest). Também citou modelos oficiais como o DESSEM [6].	Refinamento de Escopo: A IA misturou modelos de mercado com modelos oficiais do ONS. Precisei pedir para ela separar o que é "Estado da Arte" (IA) do que é "Regulatório" (ONS).
"Compare as vantagens de LSTM para previsão de carga elétrica."	O LSTM foi destacado pela captura de padrões não lineares complexos, brilhou em múltiplas sazonalidades e tendências de longo prazo [6].	Troubleshooting de Dados: A IA alertou que o LSTM exige normalização rigorosa dos dados, uma "cicatriz" técnica importante de forma mais automática.
Nota de Aprendizado: O mercado valoriza o profissional que entende que a IA é uma ferramenta de suporte à decisão. Durante os testes, percebi que prompts que fornecem um papel (Persona) para a IA, como "Aja como um analista de investimentos", geram resultados muito mais acionáveis do que perguntas genéricas.

Técnicas Avançadas de Engenharia de Prompt (Baseado no Material de Apoio)
Para elevar o nível das interações com o NotebookLM, aplicamos as técnicas de Engenharia de Prompt apresentadas no material da DIO/Canva. Um prompt "Nota 10" deve ser estruturado utilizando componentes claros para guiar o modelo de IA de forma precisa.

Estrutura de um Prompt Robusto
Componente	Descrição	Aplicação no Projeto
Contexto/Configuração	Define o papel da IA e o cenário.	"Você é um Engenheiro de IA especialista no setor elétrico brasileiro."
Instruções	Especifica a tarefa a ser realizada.	"Analise o ebook e resuma o pipeline de limpeza de dados."
Conteúdo Principal	O documento ou dados a serem analisados.	O ebook "Engenharia de IA na Prática" carregado no NotebookLM.
Restrições	Limita a extensão ou o escopo da resposta.	"Responda em tópicos, focando apenas em dados do ONS."
Formato de Saída	Define como a resposta deve ser apresentada.	"Apresente a resposta em uma tabela comparativa."
Prompt Estratégico "Mestre" para o NotebookLM
Com base nessas técnicas, aqui está o prompt final utilizado para conectar a técnica ao negócio:

Contexto: Você é um Especialista em Análise de Investimentos e Engenheiro de IA. Seu objetivo é ajudar a conectar dados técnicos de energia com decisões de mercado financeiro.

Tarefa (Instrução): Com base no ebook fornecido, identifique os 3 principais padrões de carga elétrica (sazonalidade, feriados e MMGD) e explique como cada um deles impacta diretamente o risco de uma carteira de investimentos em empresas de energia.

Conteúdo de Suporte: Considere que o público-alvo desta análise são gestores de ativos de um banco que buscam entender a volatilidade do setor.

Restrições: Não use termos excessivamente técnicos sem explicá-los. Limite a resposta a 3 parágrafos objetivos.

Formato de Saída: Finalize com um "Insight para o Investidor" em destaque.

Analogias para Entender a Carga Elétrica
Para facilitar a comunicação com áreas não técnicas, utilizamos analogias que traduzem o comportamento da rede elétrica:

6	O Ritmo Circadiano (O "Sono" da Cidade): O sistema elétrico funciona como o metabolismo humano. Durante a noite, o sistema "repousa" (baixa carga) e "desperta" com o início das atividades comerciais, criando uma respiração constante de 24 horas [6].
7	A Grande Rodovia Urbana (A "Hora do Rush"): A carga elétrica é como o fluxo de veículos. Dias úteis têm "horas de pico" onde o sistema opera no limite. Finais de semana e feriados são como estradas vazias, com queda drástica na atividade industrial [6].
8	O "Lanche Escondido" (O Fenômeno da MMGD): A geração solar própria (MMGD) é como um convidado que traz o próprio lanche para a festa. Para o ONS, parece que as pessoas comem menos (carga cai), mas na verdade elas estão consumindo a própria geração, criando o "Efeito Pato" na curva de carga [5] [6].

Miniguia de Estudo (Entrega Final)
O miniguia de estudo consolidará o conhecimento adquirido, contendo:

•	Resumos estruturados do assunto de previsão de carga elétrica e engenharia de IA.
•	Um glossário com os principais conceitos aprendidos.
•	Um conjunto de prompts reutilizáveis que possam apoiar futuras revisões sobre o tema.

Resumos Estruturados
Previsão de Carga Elétrica: Fundamentos e Importância
A previsão de carga elétrica é um componente crítico para a operação e planejamento de sistemas de energia. Ela envolve a estimativa do consumo futuro de eletricidade em diferentes horizontes de tempo. A precisão dessas previsões impacta diretamente a segurança energética, a eficiência econômica e a sustentabilidade do setor elétrico. A utilização de modelos de Machine Learning permite capturar padrões complexos e aumentar a acurácia, reduzindo incertezas financeiras em contratos de energia [5] [6].

Engenharia de IA e o Ciclo de Vida de um Projeto de ML
A Engenharia de IA abrange todo o ciclo de vida de um projeto de Machine Learning, desde a coleta e limpeza de dados até o deploy e monitoramento em produção. Este ciclo inclui etapas como exploração de dados, construção de pipelines de limpeza robustos (como uma estação de tratamento de água), treino e registro de modelos (MLflow) e empacotamento em containers (Docker). A reprodutibilidade e a validação na fronteira são princípios fundamentais para projetos profissionais [5].

Glossário de Termos
•	ONS (Operador Nacional do Sistema Elétrico): Órgão responsável pela coordenação e controle da operação do sistema elétrico brasileiro [4].
•	MWmed (Megawatt Médio): Unidade de medida de potência média utilizada para expressar a carga elétrica ao longo de um período.
•	Data Drift: Mudança nas características dos dados de entrada ao longo do tempo, que pode degradar o desempenho do modelo.
•	MLflow: Plataforma de código aberto para gerenciar o ciclo de vida do Machine Learning.
•	LSTM (Long Short-Term Memory): Arquitetura de rede neural recorrente ideal para dados sequenciais e séries temporais complexas [6].
•	MMGD: Micro e Minigeração Distribuída (ex: energia solar residencial), que impacta a leitura da carga líquida do sistema [5].

Conjunto de Prompts Reutilizáveis
•	"Quais são os principais padrões sazonais esperados nos dados de carga elétrica do ONS e como identificá-los com Python?"
•	"Descreva as etapas essenciais para construir um pipeline de limpeza de dados robusto para séries temporais."
•	"Explique a importância da divisão temporal (treino/teste) em séries temporais e os perigos do vazamento de dados."

Referências
[1] AnaliseMacro.com.br. Usando IA para prever o consumo de energia no Brasil com Python. Disponível em: https://analisemacro.com.br/econometria-e-machine-learning/usando-ia-para-prever-o-consumo-de-energia-no-brasil-com-python/ [2] Eugênio, M. et al. Previsão de Carga Elétrica para o Horizonte de Curto Prazo via Redes Neurais Artificiais Utilizando C++ e Python. Disponível em: https://www.researchgate.net/publication/349803357_Previsao_de_Carga_Eletrica_para_o_Horizonte_de_Curto_Prazo_via_Redes_Neurais_Artificiais_Utilizando_C_e_Python [3] Oliveira, A. G. Desenvolvimento de programa em Python para análise de qualidade de energia elétrica: análise direcionada pelos procedimentos de rede do ONS. Repositório Institucional da UFSC. Disponível em: https://repositorio.ufsc.br/bitstream/handle/123456789/257717/TCC-AndreGildeOliveira-PDFA_assinado.pdf?sequence=1&isAllowed=y [4] Operador Nacional do Sistema Elétrico (ONS). Carga de Energia Diária - Conjunto de dados. Disponível em: https://dados.ons.org.br/dataset/carga-energia [5] Braga, G. (2026). Engenharia de IA na Prática: Do laboratório à produção: previsão de carga elétrica com dados reais do ONS. Ebook. 
[6] Notas de Interação no NotebookLM (2026).Documentação de Engenharia de Prompt e Respostas da IA. 
