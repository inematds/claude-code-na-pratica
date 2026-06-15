# Banco de Prompts — "Claude Code na Prática" (INEMA.CLUB)

Banco de prompts, comandos e templates para o curso PT-BR, extraído e adaptado de material de terceiros.

**Notas de uso**
- Tudo foi **de-brandado**: removidos nomes próprios, comunidade exclusiva e links de afiliado. Onde houver personalização, use `[INSERIR ...]`.
- Prompts marcados **CANÔNICO** trazem também o original em **EN** em bloco separado — vale preservar o fraseado.
- Os prompts em PT-BR são tradução fiel pronta para colar no Claude Code.
- "Quando usar" é uma linha-guia; adapte ao seu contexto.
- Numeração estável: **P01 … P42**. As duas visões abaixo (Por módulo / Por caso de uso) referenciam os mesmos IDs.

---

# Parte 1 — Por módulo

## Boas-vindas (Nível 0)
O Nível 0 é visão geral do curso, sem prompts executáveis. Comece pela Setup.

---

## Setup (Nível 1 — Fundação e Setup)

### P01 — Instalar o Claude Code
**Quando usar:** primeira instalação numa máquina nova.
```text
Olá! Quero que você instale o Claude Code no meu computador e instale também
qualquer outra dependência necessária para rodá-lo aqui. Quando terminar, me avise.
```
> EN: "Hey there, I would like you to install Claude Code onto my computer, and install any other dependencies that are required to run that on my computer. Once that's done, let me know."

### P02 — Teste de criação de arquivos
**Quando usar:** validar que o Claude consegue criar pastas/arquivos no seu sistema.
```text
Crie para mim uma pasta chamada "cafe-gelado" na minha área de trabalho e escreva dois
arquivos dentro: um chamado "por-que-cafe-e-otimo" e outro "por-que-cafe-nao-e-otimo".
```
> EN: "Create for me a folder called iced coffee on my desktop, and write two files in that. One, why coffee is great. And the second, why coffee is not great."

### P03 — Conectar/reconectar o GitHub via CLI
**Quando usar:** quando a conexão com o GitHub caiu ou nunca foi feita.
```text
Quero que você consiga acessar meus repositórios do GitHub. Conecte-se ao GitHub pela CLI
e confirme. Se você não estiver conectado, atualize/refaça essa conexão, por favor.
```

### P04 — Estilo de comunicação (instruções para o Claude) — CANÔNICO
**Quando usar:** configurar como o Claude fala com você (vai no CLAUDE.md / system).
```text
Tom direto e informal — nada de enrolação, nada de "corporativês". Sem bullet points a
menos que eu peça. Sem travessões (entrega de texto de IA). Nunca use palavras de
preenchimento como "certamente", "com certeza", "ótima pergunta" ou "fico feliz em ajudar".
Mantenha o texto direto e focado em resultado, não em features.
Antecipe problemas (olhe além das curvas), desafie meu raciocínio, seja NÃO-bajulador
(não concorde com tudo que eu disser) e seja máximo em busca da verdade.
Eu sou: [INSERIR 2 FRASES sobre você/seu trabalho].
```
> EN: "Direct and casual tone — no fluff, no corporate speak. No bullet points unless I ask. No em dashes (dead giveaway of AI writing). Never use filler words like 'certainly', 'absolutely', 'great question', or 'I'd be happy to'. Keep copy punchy and outcome-focused, not feature-focused. Look around corners, challenge my perspective, be non-sycophantic, and be maximally truth-seeking. I'm a [INSERT 2 SENTENCES]."

---

## Memória (Nível 4 — Sistema de Memória)

### P05 — Organizar a vida em "baldes" (buckets) — CANÔNICO
**Quando usar:** estruturar memória de curto prazo a partir de tudo que você toca.
```text
Com base em tudo que você sabe sobre mim e em tudo em que eu trabalho, quero que você
organize a minha vida em seis a oito baldes/categorias.
```
> EN: "Based on everything you know about me and everything I work on, I want you to organize my life into six to eight buckets/categories."

### P06 — Materializar os baldes em pastas com CLAUDE.md
**Quando usar:** transformar os baldes em estrutura real de pastas.
```text
Crie para mim essas seis a oito pastas na minha área de trabalho, cada uma com um
arquivo CLAUDE.md dentro.
```

### P07 — Preencher o CLAUDE.md por projeto (briefing) — CANÔNICO
**Quando usar:** documentar o contexto completo de cada pasta/projeto.
```text
Adicione um CLAUDE.md em cada uma dessas pastas e depois me faça perguntas sobre cada
projeto, para eu te dar o briefing completo. Para cada projeto capture: o que é a pasta;
qual é o objetivo (ex.: "maximizar o valor que cada pessoa recebe, crescer a base");
por que ele existe; o stack; as decisões (ex.: "nada de posts gerados por IA");
um mapa de memória; e referências.
```
> EN: "Add this CLAUDE.md file in each of those folders, and then ask me questions about each one so I can give you the full project brief. For each: what the folder is; what the goal is; why it exists; the stack; the decisions; a memory map; and references."

### P08 — Regra de "salvar memória" no CLAUDE.md — CANÔNICO
**Quando usar:** definir onde gravar conversas quando você pedir "salvar/wrap up".
```text
Quando eu pedir explicitamente para salvar, guardar, "fechar" (wrap up) ou lembrar a
conversa, salve aqui: [INSERIR LOCAL DA PASTA/WIKI]. Haverá uma subpasta relevante para
o tema — escolha a subpasta correta e adicione essa informação nela.
(Adicione isto na seção de memória do CLAUDE.md.)
```
> EN: "When I explicitly ask you to save, store, wrap up, or remember the conversation, save it here. There will be a relevant subfolder related to the topic. Make sure you choose the correct subfolder and add that information into it."

### P09 — Skill de wrap-up para o Obsidian — CANÔNICO
**Quando usar:** ao fim de qualquer conversa, salvar a essência no wiki certo.
```text
Escreva para mim uma skill de "wrap-up": quando eu estiver tendo qualquer conversa com
qualquer modelo no meu computador, ela deve pegar a essência dessa conversa e guardá-la
no wiki relevante dentro do meu vault do Obsidian. Depois renomeie a skill para
"obsidian wrap-up".
```
> EN: "Write me a wrap-up skill: when I'm having any conversation with any model on my computer, it can take the essence of that conversation and store it in the relevant wiki within my Obsidian vault. Then change the name to 'obsidian wrap-up'."

### P10 — Skill "Obsidian Ask" (consulta ao wiki) — CANÔNICO
**Quando usar:** responder perguntas consultando seu segundo cérebro local.
```text
Tenho na minha área de trabalho uma pasta de vault do Obsidian com notas de tudo em que
trabalho. Crie uma skill chamada "obsidian ask". Sempre que eu te fizer uma pergunta
relacionada a qualquer coisa que eu faço, se for relevante consulte esse banco para uma
resposta específica e siga todas as instruções que houver dentro dele.
```
> EN: "I have on my desktop an Obsidian vault folder with notes from everything I'm working on. Create a skill called 'Obsidian Ask'. Whenever I ask you a question to do with anything I'm doing, if relevant, query this database for a specific answer and follow all the instructions within it."

### P11 — Memória de longo prazo com Pinecone — CANÔNICO
**Quando usar:** vetorizar o wiki e ter skills de wrap-up/ask vetoriais.
```text
Construa para mim uma skill com Pinecone. Vou te dar uma API key do Pinecone. Vetorize
tudo que existe dentro da minha pasta [INSERIR] do Obsidian e armazene no Pinecone
(crie um índice/vault se não existir). Depois construa uma skill de wrap-up: quando eu
acioná-la, pegue toda a essência da conversa e guarde numa pasta específica dentro do
Pinecone. Adicione uma segunda skill, "ask Pinecone": quando eu pedir, consulte esse
banco e traga a informação de volta para mim.
```
> EN: "Build me a skill with Pinecone. I'll give you a Pinecone API key. Vectorize everything within my Obsidian folder and store it in Pinecone (create a vault if it doesn't exist). Then build a wrap-up skill: when I trigger it, take the entire essence of the conversation and store it in a specific folder inside Pinecone. Add a second skill, 'ask Pinecone': when I ask, go to this database, query it, and bring back information for me."

---

## Power Features (Nível 3 — Skills, MCPs, Subagentes)

### P12 — Criar uma skill a partir de uma API — CANÔNICO
**Quando usar:** empacotar um processo repetível (ex.: encurtador de URL) como skill.
```text
Quero criar uma skill com você. O processo é: eu te dou [INSERIR ENTRADA, ex.: uma URL]
e você [INSERIR AÇÃO, ex.: converte em um link curto via Bitly]. (Se já existir uma skill
parecida e você quiser um build limpo, apague-a primeiro.) Me avise quando estiver pronto
para a minha API key. Em seguida, com essa API key, construa a skill.
```
> EN: "I would like to create a skill with you. I'd like a process in which I give you [INPUT], and you're going to [ACTION]. If a similar skill already exists, delete it first. Let me know when you're ready for my API key. Then, with this API key, create the skill."

### P13 — Inspecionar uma skill do marketplace
**Quando usar:** avaliar uma skill antes de adotar.
```text
Me fale sobre a skill [INSERIR NOME, ex.: brand guidelines] — quero entender o que ela
faz, depois quero testá-la e descobrir se funciona.
```

### P14 — Exportar skills para portabilidade
**Quando usar:** levar suas skills para outro ambiente/modelo.
```text
Salve todas as minhas skills na minha área de trabalho em uma pasta "Claude skills", com
instruções e todos os detalhes de cada skill, para eu poder levá-las para outro ambiente.
```

### P15 — Criar um MCP local a partir de uma API — CANÔNICO
**Quando usar:** expor uma API (ex.: YouTube Data) como ferramentas do Claude.
```text
Quero criar um MCP de [INSERIR SERVIÇO, ex.: YouTube]. Você já tem uma API key de
[INSERIR SERVIÇO] neste sistema. Primeiro me dê uma lista das funcionalidades disponíveis.
Depois construa para mim um MCP local — o mais útil para mim com base em tudo que você
sabe sobre mim. Em seguida, vá em frente e construa.
```
> EN: "I would like to create a [SERVICE] MCP. You have a [SERVICE] API key on this system. Give me a list of the different functionalities you have, then create for me a local MCP — the one that would be most viable for me based on everything you know about me. Then build it."

### P16 — Três subagentes com veredito condensado — CANÔNICO
**Quando usar:** pesquisa multi-perspectiva paralela com síntese única.
```text
Quero que você pesquise sobre [INSERIR TEMA] e crie três subagentes. O subagente 1 olha
do ponto de vista de [INSERIR ÂNGULO 1]. O agente 2, da perspectiva de [INSERIR ÂNGULO 2].
O agente 3, de um ângulo holístico/todos-os-lados [INSERIR ÂNGULO 3]. Seu trabalho é olhar
todos e me dar uma visão condensada, rodando o máximo de iterações possível.
```
> EN: "I want you to do some research on [TOPIC] and create three sub-agents. Sub-agent one looks at it from a [ANGLE 1] point of view. Agent two from a [ANGLE 2] perspective. Agent three from a [ANGLE 3] angle. Your job is to look at all of them and give me a condensed view, with as many iterations as possible."

### P17 — Rotina de rascunho de e-mails
**Quando usar:** automatizar respostas da caixa de entrada.
```text
Quero que você verifique todos os meus e-mails da caixa de entrada e, para qualquer um que
não tenha resposta nem rascunho e esteja não lido, escreva um rascunho de resposta.
```

### P18 — Workflow de inquérito de cliente (gatilho via API) — CANÔNICO
**Quando usar:** reagir a leads que chegam pelo site.
```text
Você vai receber informações de um cliente que solicitou meus serviços pelo meu site.
Pegue o e-mail dele e escreva um rascunho de resposta. Depois agende um horário num slot
conveniente entre 9h e 17h no meu fuso horário.
```
> EN: "You're going to get information from a client who inquired for my services on my website. Take their email and draft them a reply for me. Then book some time at a convenient slot between 9:00 and 5:00 in my time zone."

### P19 — Loop de crítica com modelo externo — CANÔNICO
**Quando usar:** crítica e refino com uma segunda opinião.
```text
Crie um agente de crítica e revise você mesmo o trabalho. Quando terminar, traga o
[INSERIR MODELO EXTERNO] com uma perspectiva fresca para checar.
```
> EN: "Create a critique agent and review it yourself. When that's done, bring in [EXTERNAL MODEL] with a fresh perspective to check it."

---

## Website (Nível 2 — Website Masterclass)

### P20 — Pesquisa de concorrentes com matriz de julgamento — CANÔNICO
**Quando usar:** mapear e ranquear os melhores concorrentes antes de construir.
```text
Quero criar um site para [INSERIR NEGÓCIO], que [INSERIR DESCRIÇÃO]. Use a conexão do
Firecrawl e encontre os melhores/mais bem-sucedidos [INSERIR CATEGORIA]. Vou operar em
[INSERIR GEOGRAFIA] (mas pode ser internacional). Identifique uma lista grande e depois
o top 5 — pode avaliar do jeito que quiser (Google reviews, ranqueamento de SEO, etc.).
Desenvolva uma matriz de julgamento para avaliar isso. Entregue um relatório dos cinco e
uma análise profunda do que os cinco melhores têm em comum que os cinco piores não têm,
para usarmos esses princípios. Me faça as perguntas que precisar para clarear o entendimento.
```
> EN: "I would like to create a website for [BUSINESS] that [DESCRIPTION]. Use the firecrawl connection to find the very best [CATEGORY] that are the most successful. I'm operating in [GEOGRAPHY]. Identify a big list, then the top five. Develop a judging matrix to assess them. Then deliver a report on those five and a deep analysis of what the five best have in common that the worst five don't. Ask me any questions you need to clarify your understanding."

### P21 — Internalizar o briefing antes de construir
**Quando usar:** depois de salvar a pesquisa num `melhores-principios.md` no projeto.
```text
Familiarize-se com o documento de melhores-princípios à esquerda. Vamos construir juntos
um site que é [INSERIR TIPO]. Me avise quando tiver entendido o briefing e aí começamos.
```
> EN: "Familiarize yourself with the best-principles document on the left-hand side, and we're going to build a website together that is [TYPE]. Let me know when you've understood the brief, then we can get started and get building."

### P22 — Construir o site com inspiração de um repo/HTML
**Quando usar:** usar um design system ou HTML baixado como inspiração visual.
```text
Construa um site para [INSERIR TIPO] usando os melhores-princípios à esquerda, mas com a
inspiração de design deste repo do GitHub: [INSERIR URL DO REPO].
(Alternativa: use como inspiração o HTML que eu acabei de baixar no computador.)
```

### P23 — Versões em paralelo em pastas numeradas
**Quando usar:** gerar 2-3 variações do mesmo site e escolher a melhor.
```text
Crie uma pasta à esquerda chamada "[INSERIR NÚMERO]" e coloque seus designs dentro.
(Repita com outros agentes/terminais para ter 2-3 sites em pastas diferentes.)
Quando terminar: abra para mim em um localhost.
```

### P24 — Salvar API key e gerar imagens da seção
**Quando usar:** guardar chave com segurança e gerar imagens (hero, etc.).
```text
Guarde esta API key no meu computador de forma segura, de modo que você consiga acessá-la
no futuro. Depois gere imagens lindas de [INSERIR TIPO] — ou imagens que você ache
relevantes — para esta seção que você está implementando aqui.
```

### P25 — Otimização de SEO a partir de um repo — CANÔNICO
**Quando usar:** pesquisar keywords e aplicar SEO equilibrando atenção/conversão.
```text
Quero melhorar o SEO desta página. Primeiro, entenda quais são as keywords para as quais
eu quero ranquear nesta página — busque um equilíbrio entre capturar atenção, converter
essa atenção e o ranqueamento de SEO. Use todos os insights deste repo do GitHub para
tornar isso realidade: [INSERIR URL DO REPO DE SEO]. Ao terminar, me dê uma lista detalhada
com marcações verdes do que você fez, explicando cada melhoria; depois publique no GitHub
e na Vercel.
```
> EN: "I would like to improve the SEO of my webpage. First, understand the keywords I want to rank for on this page. Try to blend capturing attention and converting that attention with SEO ranking. Use all the insights within this GitHub repo to make that a reality. When done, give me a detailed list with green tick marks per change, then push it live to GitHub and Vercel."

### P26 — Aplicar princípios de UI/UX a fundo
**Quando usar:** refinar um site existente por checklist de design (em paralelo ao SEO).
```text
Quero usar este repo para melhorar este site — é sobre UI e UX. Olhe todos os melhores
princípios e aplique-os sem dó ao meu site real. Vou ter um agente separado cuidando do
SEO, então parte do texto pode mudar no caminho.
```

### P27 — Revisão crítica/adversarial do site — CANÔNICO
**Quando usar:** numa janela limpa, achar inconsistências de copy/design/UX.
```text
Quero que você atue como uma pessoa criticamente exigente. Percorra o site e encontre
inconsistências, textos que não fazem sentido, design ruim, e volte com uma lista de
ideias classificadas em crítico, alto, médio e baixo. Você não precisa inventar bugs
críticos onde não existem, mas olhe de verdade para me ajudar a melhorar — para deixar
este site o mais eficaz, honesto e bem-desenhado possível. Traga qualquer repo do GitHub
que você ache necessário.
```
> EN: "I want you to act as a critically challenging individual. Go through the website and find inconsistencies, copy that doesn't make sense, design that looks bad, and come back with a list of critical, high, medium and low ideas. You don't have to find critical bugs where they don't exist, but really look at it to help me improve — so I can make this website as effective, honest, and well-designed as possible. Bring in any relevant GitHub repos you think are required."

---

## Apps (Nível 6 — Apps com Backend)

### P28 — Formulário de captura de leads — CANÔNICO
**Quando usar:** adicionar lead magnet com perguntas e salvar no banco.
```text
Adicione um formulário de captura de e-mail. Peça o nome, o e-mail e mais uma pergunta —
algo como "quanto dinheiro você está faturando", com cinco opções de R$0 até R$1 milhão+.
Depois adicione mais uma: "qual é o maior problema que você tem agora?". Quando estiver
pronto, salve todas essas informações no Supabase.
```
> EN: "Add in an email capture form. Ask for their name, their email, and one other question — something like 'how much money are you making', with five options from $0 up to $1 million plus. Then add one more: 'what is the biggest problem you have right now?' When that's done, save all of that information into Supabase."

### P29 — Sign-up, login e dashboard autenticado — CANÔNICO
**Quando usar:** construir backend autenticado com painel de valor.
```text
Agora quero uma seção de cadastro e login, toda autenticada e gerenciada no Supabase. O
usuário cria conta e entra. Ao entrar, quero ver o site dele em um dashboard lindo, no
mesmo estilo do site. Mostre métricas diferentes, raspe alguns dados do site dele com um
script em background, rode análise de SEO (procure repos no GitHub que façam isso) e deixe
essa página o mais valiosa humanamente possível — tudo autenticado e conectado ao Supabase.
```
> EN: "I'd now like a sign-up and log-in section, all authenticated and managed in Supabase. When they sign in, I want to see their website in a beautiful dashboard in the exact same style as the website. Show different metrics, scrape some stuff from their website with a background script, run SEO analysis (look for GitHub repos that let us do that), and make that page as valuable as humanly possible — all authenticated and connected to Supabase."

### P30 — Integração de pagamentos com Stripe — CANÔNICO
**Quando usar:** adicionar planos pagos (standard/premium) ao app.
```text
Quero integrar o Stripe. No dashboard quero uma seção com cores: standard e premium. O
premium é [INSERIR PREÇO] por mês. Me guie no setup do Stripe da forma mais sucinta
possível, conferindo a documentação mais recente, com instruções claras e nada mais longas
que o necessário. Eu te dou os arquivos necessários. Seu objetivo é exigir o mínimo de mim
e, ao mesmo tempo, deixar tudo o mais seguro possível.
```
> EN: "I'd like to integrate Stripe. In the dashboard I want a color-coded section: standard and premium. Premium is [PRICE] a month. Walk me through how to set up Stripe as succinctly as possible, checking the very latest documentation, with clear instructions no longer than they need to be. I'll give you the requisite files. Your objective is to require as little from me as possible while making it as secure as possible."

### P31 — Roteamento de modelo + rate limit (OpenRouter)
**Quando usar:** controlar o custo das features de IA do app.
```text
Para as features de IA, use a API key do OpenRouter. Use o modelo Sonnet até o usuário
atingir no máximo 10 mensagens por dia; a partir daí, caia para um modelo mais barato.
Implemente rate limits para não dar abuso e fique de olho no gasto total de créditos.
```

### P32 — Copy de conversão via subagentes — CANÔNICO
**Quando usar:** pesquisa profunda de copy de conversão, sintetizada criticamente.
```text
Suba alguns subagentes. Pesquise a fundo as melhores práticas de copy para este tipo de
site, com o objetivo de converter. Veja quais sites estão arrasando neste segmento, o que
dá para aprender e como melhorar o nosso copy para deixá-lo o mais eficaz possível. Use
múltiplos subagentes; analise criticamente os inputs deles e sintetize de forma que gere
um bom resultado. Seja minucioso e detalhado, mas não superanalise.
```
> EN: "Spin up a couple of subagents. Go deep on research into the best practices for copy of this kind of website, with the objective to convert. Look at which websites are crushing it, what we can learn, and how we can improve our own copy. Use multiple subagents; critically analyze their inputs and synthesize them into a good output. Be thorough and detailed, but don't over-analyze."

---

## Build Anything (Nível 7)

### P33 — Raspagem de leads (Apify) — CANÔNICO
**Quando usar:** montar lista de prospects para prospecção.
```text
Quero mirar em [INSERIR NICHO] que ficam em [INSERIR LOCAL]. Use o Apify — encontre o
melhor actor/exemplo que conseguir — e me traga, de cada um: nome, e-mail, redes sociais
que achar e um fato interessante. Me traga [INSERIR NÚMERO, ex.: 10] deles, para eu poder
conversar com eles. Coloque tudo num HTML bonito para eu visualizar.
```
> EN: "I would like to target [NICHE] that live in [LOCATION]. Use Apify, find the best example you can, and get me their name, email address, any social media, and one interesting fact about each. Get me [N] of those, so I can go have a conversation with them. Put this into a beautiful HTML for me."

### P34 — Dashboard de conteúdo "outlier" — CANÔNICO
**Quando usar:** descobrir conteúdo viral/outlier de um nicho com métricas.
```text
Quero um dashboard que faça o seguinte. Resultado que eu quero verdadeiro: entender quais
são os outliers — o conteúdo que está viralizando agora — e, a partir disso, saber quantas
visualizações teve, curtidas, comentários, engajamento, duração e quando foi postado.
Quero conseguir organizar por outlier. E quero saber quais criadores seguir — aliás, sugira
alguns para mim.
```
> EN: "I want a dashboard that does X. The outcome I want true: understand the outliers — the content going viral right now — and from that, how many views, likes, comments, engagements, how long it is, and when it was posted. Let me organize it by outlier. And tell me which creators to follow — suggest some."

### P35 — Meta-prompt de "gargalo" para destravar — CANÔNICO
**Quando usar:** quando você não sabe a solução e quer pensar o problema junto.
```text
Isto é o que eu estou tentando alcançar: [INSERIR OBJETIVO]. Me faça perguntas para clarear
minhas intenções. E este é o resultado desejado: [INSERIR RESULTADO]. Como eu devo pensar
melhor sobre o problema? E aí vamos pensar a solução juntos.
```
> EN: "This is what I am trying to achieve: [GOAL]. Ask me questions to clarify my intentions, and this is my desired outcome: [OUTCOME]. How do I best think about the problem? And then we're going to think about the solution together."

### P36 — Validar/enriquecer e-mails via API
**Quando usar:** limpar uma lista de leads antes do outreach.
```text
Use a API key do [INSERIR VERIFICADOR DE E-MAIL] e valide todos os e-mails desta lista
para mim. API key: [INSERIR].
```

---

## Design Systems (Nível 8)

### P37 — Setup do framework de design (clonar e aprender) — CANÔNICO
**Quando usar:** iniciar um sistema de design-as-code para slides/sites.
```text
Quero criar slides lindos. Use o repo abaixo: instale, clone, aprenda tudo sobre ele, e
depois me dê alguns exemplos de marcas que eu poderia usar para construir slides bonitos.
[INSERIR URL DO REPO DO DESIGN SYSTEM]
```
> EN: "I want to create gorgeous slides. Use the repo below: install it, clone it, learn everything about it, then give me a couple of different brand examples I could use to build some beautiful slides."

### P38 — Deck no estilo de uma marca + imagens — CANÔNICO
**Quando usar:** gerar apresentação alinhada à marca de referência.
```text
Vamos construir um deck de [INSERIR N] páginas sobre [INSERIR MARCA]. Vá ao site da marca
pegar alguns assets e use minha API key do [INSERIR GERADOR DE IMAGEM] para gerar algumas
imagens alinhadas ao estilo de marca perfeito deles, como você achar adequado.
```
> EN: "Let's build a [N]-page slide deck on [BRAND]. Go to the website to grab a few assets, and use my [IMAGE-GEN] API key to generate a couple of images in line with their perfect brand style, as you see appropriate."

### P39 — Rodar a skill de extração de marca
**Quando usar:** codificar cores, fontes, espaçamento e layout de uma marca.
```text
Baixe isto, descompacte e siga as instruções. (A skill vai te perguntar qual é a
marca/site e do que é o seu negócio, e então gerar um design blueprint capturando
espaçamento, cores, fontes e princípios de layout.)
```

---

## Agente Pessoal (Nível 5 — "Sistema Operacional" de agentes)

### P40 — Instalar o sistema operacional de agentes
**Quando usar:** subir o pacote do agente pessoal (zip) e configurá-lo.
```text
Acabei de baixar este sistema operacional. Abra-o e siga as instruções, e fique à
disposição para me ajudar a configurar se for preciso. (Tudo que ele precisa para se
configurar e se conectar a este computador está no CLAUDE.md dentro do pacote.)
```

### P41 — Mission control: planejar metas — CANÔNICO
**Quando usar:** decompor uma meta de médio prazo em passos acionáveis.
```text
Isto é o "mission control" — planejamento de meta de médio/longo prazo. Minha meta de
médio prazo é: [INSERIR META, ex.: "chegar a 500 inscritos" ou "lançar uma lista de e-mail
com 1.000 pessoas"]. Converse comigo sobre tudo e depois quebre essa meta em cerca de 4 a 10
prompts individuais e sequenciais — marque quais são para você (a IA) executar e quais são
para mim — e monte um roadmap lindo que eu possa percorrer passo a passo.
```
> EN: "This is mission control — long-term goal planning. Give it a mid-term goal, e.g. 'get to 500 subscribers, or launch an email list with 1,000 people on it.' Break that down into between 4 to 10 individual, sequential prompts — some for the AI, some for me — and build a roadmap I can go through and complete."

### P42 — Backup diário do agente no GitHub
**Quando usar:** proteger toda a configuração/memória do agente.
```text
Conecte-se ao GitHub e faça um backup diário deste sistema inteiro, todos os dias, para que
— se algo der errado no meu computador ou eu cometer um erro — a gente possa voltar no tempo
e restaurar.
```

---

## Compliance (Nível 9 — Compliance e Manutenção)

### P43 — Red-team de segurança ofensiva (mega prompt) — CANÔNICO
**Quando usar:** auditar a segurança de um codebase/projeto antes de produção.
```text
Você é um engenheiro sênior de segurança ofensiva contratado para fazer red-team neste
codebase. Seu trabalho é invadir, exfiltrar dados e quebrar o negócio. Seja paranoico e
minucioso — não assuma nada. Método: percorra o repositório inteiro de forma sistemática.
Para cada arquivo que ler, pergunte: "Se eu fosse um atacante que já tem acesso de leitura,
o que eu faria com isto?". Superfícies de ataque a cobrir: segredos e credenciais; segurança
de banco (ex.: Supabase) e autorização; LLM / prompt injection; webhooks; dependências e
cadeia de suprimentos; logging e exposição. Saída: achados ordenados por severidade, o
caminho do exploit e a correção concreta de cada um. Não escreva um scanner — recomende
poucos scanners open-source consagrados (ex.: Gitleaks, Semgrep, Trivy), diga quais três
adicionar ao meu pre-commit, e assuma que isso barra ~80% dos problemas.
```
> EN: "You are a senior offensive security engineer hired to red-team this codebase. Your job is to break in, exfiltrate data, and bankrupt the business. Be paranoid and thorough — assume nothing. Walk the entire repo systematically; for every file ask: 'If I were an attacker with read access, what would I do with this?' Cover: secrets & credentials; database security (e.g. Supabase) and authorization; LLM / prompt injection; webhooks; dependencies and supply chain; logging and exposure. Output: findings ranked by severity, the exploit path, and the concrete fix for each. Don't write a scanner — recommend battle-tested open-source scanners (e.g. Gitleaks, Semgrep, Trivy), tell me which three to add to my pre-commit, and assume that shuts down ~80% of the issues."

### P44 — API key via terminal (fora do chat)
**Quando usar:** evitar colar uma API key no log do Claude.
```text
Crie um comando de terminal para eu atualizar a minha API key de [INSERIR SERVIÇO]. (Depois
rode esse comando você mesmo no terminal, de modo que o Claude nunca veja a chave em si.)
```

### P45 — Teto fixo de gasto em API
**Quando usar:** evitar prejuízo se uma chave vazar.
```text
Para qualquer API de custo variável, defina um teto de gasto fixo e rígido. Configure a
API key com um custo total que eu aceite e defina a frequência de renovação. Limite o
gasto antes de limitar o risco.
```

### P46 — Mapa de health-check do sistema
**Quando usar:** garantir que o sistema continua funcionando ao longo do tempo.
```text
Pense no meu sistema inteiro e em toda a jornada do usuário, e defina quais devem ser os
health checks — o que um sistema funcional teria. Escreva isso como testes para eu saber
que continua funcionando. Inclua a checagem de logs de erro e do lado financeiro/pagamentos
(ex.: Stripe).
```

---

## Monetização (Nível 10 — "Making $$$")
Este módulo é majoritariamente estratégia de negócio (oferta, escada audit→build→retain, ICP, "more/better/new"), sem prompts próprios de Claude Code. Use os prompts de prospecção (P33, P36) e construção (Apps/Website) aplicados ao seu funil.

---

## Painel / OS (Nível 11 — Claude Code + Sistema Operacional de Agentes)

### P47 — Adicionar uma ferramenta desconhecida ao OS
**Quando usar:** quando uma ferramenta sua não foi detectada pelo agente pessoal.
```text
Eu uso [INSERIR FERRAMENTA/SISTEMA] e não vejo isso no sistema operacional. Você pode
adicioná-lo aqui para mim?
```

### P48 — Consultar o NotebookLM via agente
**Quando usar:** o agente busca/cria notebooks no Google NotebookLM.
```text
Você tem a skill do NotebookLM no "pantheon" — fique totalmente atualizado com ela. Vá ao
meu NotebookLM, encontre o último infográfico que gerei e depois crie um notebook novo
sobre [INSERIR TEMA].
```

---

## Slash commands e comandos triviais (transversais)

Não são prompts, mas fazem parte do fluxo de trabalho:
- `/init` (com effort alto) — fazer o Claude entender o codebase inteiro.
- `/clear` — resetar a conversa (evitar "context rot").
- `/context` — inspecionar o uso da janela de contexto.
- `/compact` — comprimir o contexto mantendo o essencial.
- `/model` — trocar entre Opus / Sonnet / Haiku.
- `/cost` — ver o gasto de tokens da sessão.
- `/agents` — gerenciar subagentes.
- `/memory` — abrir/editar os arquivos de memória (CLAUDE.md).
- Invocar skills com `/<nome-da-skill>`.
- `/newbot` (no BotFather do Telegram) — criar um bot para o agente pessoal.

---

# Parte 2 — Por caso de uso

> Os mesmos prompts, agrupados pela tarefa. IDs cruzados com a Parte 1.

### Pesquisa / concorrência
- **P16** — Três subagentes com veredito condensado
- **P20** — Pesquisa de concorrentes com matriz de julgamento
- **P32** — Copy de conversão via subagentes
- **P34** — Dashboard de conteúdo "outlier"

### Briefing
- **P07** — Preencher o CLAUDE.md por projeto
- **P21** — Internalizar o briefing antes de construir
- **P35** — Meta-prompt de "gargalo" para destravar

### Construção
- **P02** — Teste de criação de arquivos
- **P22** — Construir o site com inspiração de repo/HTML
- **P23** — Versões em paralelo em pastas numeradas
- **P24** — Salvar API key e gerar imagens
- **P28** — Formulário de captura de leads
- **P29** — Sign-up, login e dashboard autenticado
- **P30** — Integração de pagamentos com Stripe
- **P31** — Roteamento de modelo + rate limit (OpenRouter)

### Debugging
- **P19** — Loop de crítica com modelo externo
- **P35** — Meta-prompt de "gargalo" para destravar
- **P46** — Mapa de health-check do sistema

### Design
- **P26** — Aplicar princípios de UI/UX a fundo
- **P37** — Setup do framework de design (clonar e aprender)
- **P38** — Deck no estilo de uma marca + imagens
- **P39** — Rodar a skill de extração de marca

### SEO
- **P25** — Otimização de SEO a partir de um repo
- **P29** — Dashboard com análise de SEO (componente)

### Automação
- **P12** — Criar uma skill a partir de uma API
- **P15** — Criar um MCP local a partir de uma API
- **P17** — Rotina de rascunho de e-mails
- **P18** — Workflow de inquérito de cliente
- **P41** — Mission control: planejar metas
- **P42** — Backup diário do agente no GitHub
- **P48** — Consultar o NotebookLM via agente

### Memória / CLAUDE.md
- **P04** — Estilo de comunicação (instruções para o Claude)
- **P05** — Organizar a vida em baldes
- **P06** — Materializar os baldes em pastas
- **P07** — Preencher o CLAUDE.md por projeto
- **P08** — Regra de "salvar memória" no CLAUDE.md
- **P09** — Skill de wrap-up para o Obsidian
- **P10** — Skill "Obsidian Ask"
- **P11** — Memória de longo prazo com Pinecone

### Prospecção / vendas
- **P18** — Workflow de inquérito de cliente
- **P33** — Raspagem de leads (Apify)
- **P36** — Validar/enriquecer e-mails via API

### Red-team
- **P27** — Revisão crítica/adversarial do site
- **P43** — Red-team de segurança ofensiva (mega prompt)

### Setup
- **P01** — Instalar o Claude Code
- **P03** — Conectar/reconectar o GitHub via CLI
- **P13** — Inspecionar uma skill do marketplace
- **P14** — Exportar skills para portabilidade
- **P40** — Instalar o sistema operacional de agentes
- **P44** — API key via terminal (fora do chat)
- **P45** — Teto fixo de gasto em API
- **P47** — Adicionar uma ferramenta desconhecida ao OS
