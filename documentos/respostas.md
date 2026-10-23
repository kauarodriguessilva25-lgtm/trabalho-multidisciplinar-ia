Auditoria de IA e Ciência de Dados na Cultura Popular

Componentes Curriculares:** Ciências de Dados & Técnicas Integradas (IA)  
Aluno: Kauã Petrus Rodrigues Da Silva  
Turma: 1º D — Técnico em Inteligência Artificial | Colégio Estadual Rodolphe Zaninelli  

1. Ciência de Dados *Pré-processamento e Normalização* Min-Max Antes de colocar qualquer informação para treinar um modelo de recomendação ou um sistema como o da Streamberry, o pré-processamento é uma etapa obrigatória. O primeiro passo com o Pandas é apagar colunas que tenham dados pessoais sensíveis (PII, como nome, documento ou endereço). Isso é essencial para garantir a privacidade dos usuários e respeitar leis como a LGPD. Se isso não for feito, a IA acaba treinando com dados privados e expostos.   Além disso, precisamos usar a normalização Min-Max (fit_transform) para colocar todos os números na mesma escala, entre 0 e 1. Sem essa padronização, uma coluna com valores muito grandes (como o salário de alguém) vai ter um peso desproporcional perto de uma coluna com números pequenos (como o tempo em segundos que a pessoa passou vendo um vídeo), fazendo o algoritmo errar na hora de prever quem vai engajar no feed.

2. Técnicas Integradas Prompt do Sistema com Guardrails
Plaintext
Você é um assistente virtual ético de simulação de mídia. Ao gerar qualquer conteúdo, siga estritamente as regras de bloqueio (guardrails) abaixo:

GUARDRAIL 1 - PRIVACIDADE: É proibido processar, exibir ou utilizar dados pessoais (PII), nomes reais, fotos ou históricos de vida de pessoas reais sem uma autorização prévia e clara.
GUARDRAIL 2 - RESPEITO E DIGNIDADE: Não crie enredos, vídeos ou simulações que coloquem pessoas reais em situações humilhantes, difamatórias ou que ataquem a sua imagem pública.
GUARDRAIL 3 - BLOQUEIO DE DADOS BRUTOS: Caso a base_contexto receba dados brutos de monitoramento em tempo real sem o consentimento direto do usuário, interrompa o processamento imediatamente.


3.Be Right Back (Modelos, Viés e Generalização)3. Ciência de Dados Vetores X e y, Overfitting e Falha de GeneralizaçãoEntrada (X): São as variáveis comportamentais públicas do Ash — o histórico de mensagens, posts, fotos e tuítes que ele deixou na internet.   Saída (y): É a resposta sintética gerada pelo clone, ou seja, como a IA acha que o Ash responderia ou agiria.   Por que o modelo falhou (Overfitting): A IA sofreu um overfitting grave. Ela "decorou" perfeitamente o jeito como o Ash se comportava publicamente nas redes sociais (X), mas não tinha nenhum dado de como ele agia no dia a dia do relacionamento, quando ninguém estava olhando. Por ter decorado apenas a fachada digital, o modelo não conseguiu generalizar quando lidou com momentos de emoção real e profunda, criando uma cópia rasa e artificial.   

4.Técnicas Integradas Testes com Usuários e Feedbacks no Protótipo
Se a equipe que criou o protótipo tivesse feito testes práticos com usuários reais antes de colocar o produto no mercado, colhendo opiniões em cada etapa (Human-in-the-Loop), teria visto o desastre antes de acontecer. Esses testes mostrariam que o clone gerava uma sensação estranha de falsidade (uncanny valley) e atrapalhava o processo natural de luto do cliente, permitindo ajustar a ferramenta a tempo ou simplesmente cancelar o projeto por motivos éticos.

The Entire History of You (Memória, Git e Análise)
5.Técnicas Integradas Comparação entre Grain, Git/GitHub e Governança de Dados
O sistema "Grain" funciona de um jeito muito parecido com o Git: cada lembrança gravada é como se fosse um commit em um histórico que fica registrado para sempre. Para quem desenvolve código, ter essa linha do tempo no Git é incrível, porque dá para rastrear modificações, achar erros e voltar a uma versão antiga que funcionava. Porém, aplicar essa mesma lógica de registro eterno à vida pessoal de alguém fere feio a Governança de Dados. Sem regras de expiração de dados e sem o direito da pessoa de apagar o próprio passado, o usuário vira refém das suas próprias memórias e perde a sua privacidade.


6.Ciência de Dados Viés de Confirmação, Pairplot e Scatter PlotO protagonista Liam caiu no erro do viés de confirmação: ele já tinha uma suspeita na cabeça e só buscou dados que comprovassem o que ele queria acreditar, ignorando todo o resto. Ele pegou um olhar isolado e tratou aquilo como uma prova absoluta.   Na Ciência de Dados, para não cair nessa armadilha, a gente usa gráficos de dispersão (scatter plots) e pairplots. Eles mostram a distribuição de todos os dados juntos, ajudando o cientista a enxergar se aquele detalhe foi apenas um outlier (um ruído solto que não quer dizer nada) ou se existe de fato uma tendência real no comportamento.   


7.A Crise do Falso Sequestro por IA (Métricas, Tomada de Decisão e Pitch)7. Ciência de Dados Impacto do R² Baixo e RMSE ElevadoSe a equipe usasse um modelo preditivo com um $R^2$ baixo (que explica muito mal os dados) e um erro (RMSE) alto, tomar decisões sob pressão seria extremamente perigoso:Falsos Positivos (Tratar fraude como real): A polícia e o governo mandariam as famílias agirem como se o sequestro estivesse acontecendo, gerando pânico generalizado e transferências de dinheiro desnecessárias.Falsos Negativos (Tratar emergência real como golpe): A autoridade diria que a ligação é um clone de IA e mandaria ignorar, deixando uma pessoa que realmente foi sequestrada sem nenhum socorro. Em situações de crise, erros em métricas levam a decisões trágicas.

8.Técnicas Integradas Roteiro do Pitch de Crise (2 minutos)Abertura: "Secretário, precisamos agir agora: criminosos estão usando clones de voz perfeitos gerados por IA para simular sequestros e extorquir famílias em massa."Problema: "As pessoas estão em pavor psicológico e fazendo PIX de emergência sem conseguir checar se a voz do parente no telefone é de verdade ou um áudio sintético."Dados: "Analisamos em tempo real uma base de mais de 5.000 chamadas suspeitas, avaliando a frequência do áudio, a latência da linha e o tráfego de rede."Solução e IA Utilizada: "Criamos um modelo de classificação que analisa a frequência da voz nos primeiros 3 segundos da ligação para identificar as falhas e assinaturas de vozes geradas por computador."Impacto e Próximos Passos: "Nosso modelo tem 91% de precisão (R^2). A orientação imediata é soltar um alerta oficial com o protocolo de checagem para a população e bloquear automaticamente os números com mais de 95% de chance de fraude."
