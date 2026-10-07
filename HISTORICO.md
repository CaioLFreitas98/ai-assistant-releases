# Cronograma do AI Assistant

Tudo o que foi construído e mudado na assistente, do começo até a versão atual.
As notas detalhadas de cada versão também ficam em
[Releases](https://github.com/CaioLFreitas98/ai-assistant-releases/releases).

| Quando | Marco |
|---|---|
| Maio de 2026 | Primeira versão do projeto (então chamado "Altair") |
| Julho de 2026 | Organização do código e das dependências |
| Agosto a setembro de 2026 | Roteiro de 7 fases: segurança, contas, memória, voz, integrações |
| 3 de outubro de 2026 | **1.0.0**: primeira versão estável |
| 4 de outubro de 2026 | Instalador para Windows e app Android publicados |
| 4 de outubro de 2026 | **1.0.1**: atualização automática |
| 4 de outubro de 2026 | **1.0.2**: Google Calendar |
| 4 de outubro de 2026 | **1.0.3**: vozes no tablet, resposta ao ser chamada e despedida |
| 4 de outubro de 2026 | **1.1.0**: Especialistas e navegador controlado com Playwright |
| 7 de outubro de 2026 | **1.5.0**: servidor da casa (Linux e Windows 11), PC no modo Cliente e uso fora de casa |

---

## 1.5.0 · 7 de outubro de 2026

**A assistente vira o servidor da casa.**

- **Servidor da casa.** A assistente pode rodar num computador sempre ligado, sem
  janela: um notebook com Linux (pacote com instalador e serviço que liga
  sozinho) ou um PC com Windows 11. Tablets, celulares e PCs falam com ele.
- **PC no modo Cliente.** O PC que você usa vira a janela, o microfone e a caixa
  de som do servidor. Todas as telas de configuração continuam as mesmas e
  mudam o servidor; microfone, saída de som e ativação ficam no PC.
- **Ações no PC pelo servidor.** Abrir programas, olhar a tela, clicar, mexer em
  arquivos e no navegador acontecem no PC, mesmo quando o pedido vem do tablet.
- **Voz em tempo real no Cliente**, com uma chave temporária: a chave da OpenAI
  fica só no servidor.
- **WhatsApp e agenda no servidor**, com o QR do WhatsApp no terminal ou no PC.
- **Fora de casa** com o Tailscale: o celular e o notebook falam com a
  assistente na rua, sem abrir portas no roteador; o notebook troca sozinho
  entre a rede de casa e o Tailscale.
- **Aparelhos pareados**: veja e remova tablets, celulares e PCs.
- **Atualização automática do servidor**, no Linux e no Windows.

---

## 1.1.0 · 4 de outubro de 2026

**Especialistas e um navegador mais esperto.**

- **Especialistas da casa.** Além da personalidade (o jeito de falar), ela agora
  tem jeitos de trabalhar por assunto: **Programador**, **Design** e
  **Pesquisador** já vêm prontos. Cada um sabe como trabalhar, onde pesquisar,
  quais ferramentas usar e o tamanho de modelo que precisa.
- **Escolha sozinha pelo assunto.** "Tenho um bug nesse código" chama o
  Programador; "cria um logo" chama o Design; "compare esses dois celulares"
  chama o Pesquisador. Ele continua ativo enquanto o assunto seguir.
- **"Modo design"** fixa um especialista e **"modo normal"** volta ao padrão. O
  especialista ativo aparece no topo da janela.
- **Crie os seus**: em **Especialistas** (Central de configurações ou Mais
  opções) dá para ligar, desligar, editar e criar novos (Finanças, Estudos,
  Cozinha...). Valem para todos da casa.
- **Navegador controlado com Playwright.** Quando ela precisa mexer em um site
  sozinha, usa o navegador que você usa (Opera GX, Chrome, Edge, Brave ou
  Vivaldi), numa janela própria onde os logins ficam salvos. Ela vê os botões e
  campos da página e clica pelo texto ("Entrar"), o que erra bem menos.

## 1.0.3 · 4 de outubro de 2026

**Conversa com começo e fim.**

- **Ela responde quando é chamada.** Dizendo só o nome ("Luna"), ela fala algo
  curto, como "Pode falar." ou "Oi, estou ouvindo.", antes de esperar o pedido.
  Assim você sabe que foi ouvido. Vale no PC e no tablet.
- **Encerrar falando natural.** "Tchau", "era só isso", "obrigado", "valeu,
  Luna", "pode parar de ouvir", "deixa pra lá", "até amanhã"... Ela se despede
  e para de ouvir até ser chamada de novo. "Não" e "pode parar" sozinhos não
  encerram, porque podem ser a resposta a uma pergunta ou um pedido para parar a
  música.
- **No jeito de cada pessoa.** A saudação e a despedida seguem a personalidade
  que cada usuário escolheu para a sua IA. As frases são criadas uma vez e
  guardadas, então a resposta é imediata.
- **No modo de voz em tempo real**, a despedida também fecha a conversa na hora,
  em vez de esperar o tempo sem falar acabar.
- **"Vozes da casa" vale no tablet.** No modo "só vozes cadastradas", voz
  desconhecida é recusada também pelo tablet. Quem fala pelo tablet recebe as
  próprias permissões; antes, recebia as do dono.
- Nova opção em **Voz e ativação**: "Responder quando for chamada pelo nome".
- App Android 1.0.3: necessário para a resposta ao chamado no tablet. Instale
  por cima do anterior.

## 1.0.2 · 4 de outubro de 2026

**Google Calendar.**

- Conecte o Google Calendar em **Central de configurações → Calendário**: ver a
  agenda, receber avisos e criar eventos por voz.
- Enquanto o Google não termina a verificação do app, o login mostra o aviso
  "app não verificado". Clique em **Avançado → Acessar AI Assistant**.
- Página do app e
  [Política de Privacidade](https://caiolfreitas98.github.io/ai-assistant-releases/privacidade.html)
  publicadas.
- Mensagem mais clara quando um calendário ainda não está disponível.

## 1.0.1 · 4 de outubro de 2026

**Atualização automática.**

- Ao abrir, e a cada 6 horas, o app procura uma versão nova e mostra uma barra
  no topo da janela. **Atualizar agora** baixa, confere o arquivo, instala e
  reabre sozinho, sem perder conversas, memórias ou configurações.
- "Vozes da casa" sugeria o nome do desenvolvedor como dono em todo PC; agora
  sugere o nome da sua conta do Windows.

## 1.0.0 · 3 e 4 de outubro de 2026

**Primeira versão estável, com instalador e app Android.**

- **Instalador para Windows**: não precisa de Python nem de nada instalado, não
  pede administrador e já traz voz offline, transcrição local, palavra de
  ativação, CAD/3D e WhatsApp.
- **App Android** (satélite de voz): o tablet ou celular conversa com a
  assistente do PC pelo Wi-Fi. Tem pareamento por QR code, atende pelo nome e
  tem o mesmo visual do PC.
- **Memória que aprende sozinha**: preferências, pessoas, fatos e pendências.
  Tudo pode ser visto, corrigido ou apagado em "O que ela sabe".
- **Resumo do dia**: clima com previsão, agenda, lembretes e pendências.
- **Home Assistant** entende o jeito natural de falar ("liga ele pra mim").
- **Permissões**: uma tela define o que ela pode fazer sozinha, sem pedir
  confirmação no meio da conversa.
- Ícone próprio, botões em português e várias correções de voz e conexão.

## Agosto a setembro de 2026 · o roteiro em fases

Antes da 1.0, a assistente foi reconstruída em 7 fases:

| Fase | O que trouxe |
|---|---|
| 0. Base | Instalação reproduzível, diagnóstico e testes automáticos |
| 1. Segurança | Conexão remota protegida por token, auditoria de ações sensíveis, sem comandos perigosos no sistema |
| 2. Núcleo e contas | Vários usuários no mesmo PC, cada um com dados separados; conta online opcional com sincronização |
| 3. Planejamento | Pedidos compostos viram planos com etapas, que podem ser retomados; permissões por ação |
| 4. Memória | Lembrança de conversas e documentos com a fonte (arquivo e página); exportar e apagar |
| 5. Voz e proatividade | Personalidade editável, várias vozes (Piper, OpenAI, Gemini, ElevenLabs), voz em tempo real, lembretes, modo silencioso e "não perturbe" |
| 6. Integrações | Calendários, caixa de entrada, tarefas, resumo diário, casa inteligente e aprovação remota |

No mesmo período chegou o **agente com ferramentas**: escolha automática do
modelo de IA por tarefa, pesquisa na web, geração de imagens, arquivos,
navegador controlado e análises em paralelo.

## Julho de 2026 · organização

- Código reorganizado e dependências revisadas, incluindo leitura de PDF.

## Maio de 2026 · o começo

- Primeira versão, com o nome **Altair**: assistente de PC com voz, automação do
  computador, ferramentas de matemática e ciência e criação de peças 3D.
- Primeira publicação do projeto, com README e imagem da interface.

---

## Próximos passos

- Microsoft 365 / Outlook no calendário.
- Especialistas, etapa 2: criar por voz e material de consulta por especialista.
- Especialistas, etapa 3: sugestões de aprendizado aprovadas por você e vários especialistas no mesmo pedido.
- Verificação do app pelo Google, para tirar o aviso de "app não verificado".
- Testes com mais pessoas e aparelhos.
