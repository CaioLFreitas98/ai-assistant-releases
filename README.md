<div align="center">

<img src=".github/icon.png" alt="AI Assistant" width="128" height="128">

# AI Assistant

**Uma assistente pessoal com voz para o seu PC, que você mesmo batiza.**
Conversa por voz em tempo real, controla o computador e a casa, lembra do que importa
e responde também pelo celular ou tablet.

[![Última versão](https://img.shields.io/github/v/release/CaioLFreitas98/ai-assistant-releases?label=vers%C3%A3o&color=5cc8ff&style=flat-square)](https://github.com/CaioLFreitas98/ai-assistant-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/CaioLFreitas98/ai-assistant-releases/total?label=downloads&color=3ddc97&style=flat-square)](https://github.com/CaioLFreitas98/ai-assistant-releases/releases)
![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0b0f15?style=flat-square&logo=windows)
![Android](https://img.shields.io/badge/Android-8.0%2B-0b0f15?style=flat-square&logo=android)

### [⬇️ Baixar a última versão](https://github.com/CaioLFreitas98/ai-assistant-releases/releases/latest)

[📜 Cronograma de tudo o que mudou](HISTORICO.md)

</div>

---

## Downloads

Na página da [última versão](https://github.com/CaioLFreitas98/ai-assistant-releases/releases/latest), em **Assets**:

| Arquivo | Para quê | Tamanho |
|---|---|---|
| `AI-Assistant-<versão>-Setup.exe` | **PC com Windows**: a assistente completa | ~600 MB |
| `AI-Assistant-<versão>-Android.apk` | **Celular ou tablet** (opcional): fala com a assistente do PC pelo Wi-Fi | ~80 MB |
| `AI-Assistant-<versão>-Setup.exe.sha256` | Checksum do instalador (usado pelas atualizações automáticas) | — |

> [!NOTE]
> Versão beta. O app do Android **não funciona sozinho**: ele é um "satélite" da assistente
> que roda no PC. Instale primeiro no Windows.

---

## O que ela faz

<table>
<tr>
<td width="50%" valign="top">

### 🎙️ Voz
- Conversa por voz em tempo real, que pode ser interrompida no meio da fala
- Atende quando você diz o nome dela e responde ("Pode falar.") para você saber que foi ouvido
- Encerra quando você se despede ("tchau", "era só isso", "valeu")
- Reconhece quem está falando (**Vozes da casa**), também pelo tablet
- Fala com Piper (offline), OpenAI, Gemini ou ElevenLabs
- Português do Brasil e de Portugal, inglês, espanhol, francês, alemão e italiano

### 🧠 Memória
- Aprende sozinha suas preferências, pessoas e fatos importantes
- Lembra de pendências e pergunta como ficaram
- Retoma a conversa de onde parou
- Tudo pode ser visto, corrigido ou apagado em **O que ela sabe**

### ☀️ Seu dia
- Resumo da manhã com clima, agenda, lembretes e pendências
- Lembretes, tarefas e calendário (local, Google, iCloud ou CalDAV)
- Caixa de entrada com as mensagens não lidas do WhatsApp

### 🧑‍💼 Especialistas
- **Programador**, **Design** e **Pesquisador** já vêm prontos
- Escolhidos sozinhos pelo assunto, cada um com seu jeito de trabalhar
- "Modo design" fixa um; "modo normal" volta ao padrão
- Crie os seus (Finanças, Estudos, Cozinha...)

</td>
<td width="50%" valign="top">

### 💻 Computador
- Abre programas, sites e pesquisas no navegador que já está aberto
- Mexe em sites sozinha pelo seu navegador (Opera GX, Chrome, Edge...), clicando pelo texto dos botões
- Vê a tela, clica, digita e usa atalhos
- Controla música e volume
- Organiza pastas e lê PDF, Word e TXT
- Grava e repete **macros** de teclado e mouse

### 🏠 Casa e mensagens
- **Home Assistant**: luzes, interruptores e aparelhos ("liga a luz da sala")
- **WhatsApp**: envia mensagens, áudios com a voz dela e arquivos

### 🧮 Ciência e criação
- Equações, sistemas, derivadas e integrais
- Gráficos e simulações físicas
- Peças **CAD/3D** a partir de uma frase
- Clima, previsão, distâncias e mapas

</td>
</tr>
</table>

---

## Requisitos

| | PC | Celular / tablet |
|---|---|---|
| **Sistema** | Windows 10 ou 11, 64 bits | Android 8.0 ou mais novo |
| **Espaço** | ~2 GB livres | ~150 MB |
| **Outros** | Microfone e alto-falante. Internet para conversar | Mesmo Wi-Fi do PC |
| **Conta** | Uma chave de API própria (ver abaixo) | — |

Não precisa ter Python, Node nem nada instalado: vai tudo dentro do instalador.

---

## Instalação no Windows

1. Baixe o `AI-Assistant-<versão>-Setup.exe` da [última versão](https://github.com/CaioLFreitas98/ai-assistant-releases/releases/latest).
2. Abra o arquivo. Ele instala só para o seu usuário e **não pede administrador**.
3. Se aparecer **"O Windows protegeu o computador"**, clique em **Mais informações** e depois em
   **Executar assim mesmo**. O aviso aparece porque o instalador ainda não tem assinatura
   digital. Alguns antivírus também pedem confirmação.
4. No fim, deixe marcado **Abrir o AI Assistant**.

> [!TIP]
> A **primeira abertura demora até 1 minuto**, porque ela prepara arquivos internos uma única vez.
> As próximas são rápidas.

---

## Primeira configuração

### 1. Dê um nome para ela
Na primeira abertura você escolhe o nome da sua IA, entre 2 e 30 letras. O nome também é a
palavra para chamá-la: *"Luna, que horas são?"*. Dá para mudar depois em **⋯ Mais opções → Alterar nome da IA**.

### 2. Conecte o "cérebro" (chave de API)
A assistente usa **a sua própria chave**. O uso é cobrado direto na sua conta do provedor.

1. Crie uma chave em <https://platform.openai.com/api-keys>. A conta precisa ter créditos.
2. No app: **⋯ Mais opções → API e modelos**.
3. Cole a chave e salve. Ela fica guardada no **Cofre de credenciais do Windows**, só neste PC.

> [!IMPORTANT]
> Nunca compartilhe sua chave com ninguém, nem com quem te enviou o instalador.
> Assinaturas como ChatGPT Plus ou Claude Pro **não** incluem créditos de API.

<details>
<summary><b>Outros provedores e o que funciona sem chave</b></summary>

<br>

**Com OpenAI** você tem tudo: voz em tempo real, transcrição de alta precisão, agente com
ferramentas, pesquisa na web e geração de imagens. A assistente escolhe sozinha o modelo
para cada pedido:

| Nível | Modelo | Uso |
|---|---|---|
| Rápido | `gpt-5.6-luna` | Conversas curtas |
| Equilibrado | `gpt-5.6-terra` | Explicações e tarefas comuns |
| Complexo | `gpt-5.6-sol` | Programação, pesquisa, várias etapas |
| Máximo | `gpt-6-astra` | Trabalhos completos e auditorias |

Para forçar um modelo em um pedido, comece com `/modelo astra:` (ou `luna`, `terra`, `sol`).

**Outros provedores aceitos** para conversar: Groq, Google Gemini, Anthropic Claude, Mistral,
DeepSeek, xAI Grok, OpenRouter, **Ollama** (100% local) ou qualquer API compatível.

**Sem nenhuma chave**, funcionam: cálculos, gráficos, clima, abrir aplicativos, macros,
lembretes, tarefas e transcrição/voz offline.

</details>

### 3. Ajuste a voz e o microfone
- **Áudio e microfone**: escolha o microfone e a saída, veja o nível ao vivo e calibre.
- **Voz e ativação**: voz da assistente, idioma e quanto tempo ela continua ouvindo sem
  você repetir o nome (padrão: 30 s).
- **Vozes da casa**: cadastre sua voz para ela atender só você, ou cada morador com as
  próprias permissões.

---

## Configurações

A barra lateral tem:

| Botão | O que abre |
|---|---|
| 💬 **Conversa** | Mostra ou esconde o painel de chat |
| ⌨️ **Automatizar tarefas** | Grava e executa macros de teclado e mouse |
| 📅 **Próximos compromissos** | Agenda dos próximos 7 dias |
| ⚙️ **Central de configurações** | Identidade, personalidade, **especialistas**, cérebro, voz, áudio, vozes da casa, **calendário**, WhatsApp, permissões, conta e aplicativos, tudo num lugar |
| ⋯ **Mais opções** | Os atalhos abaixo |

No **⋯ Mais opções**:

| Opção | O que faz |
|---|---|
| **Trocar conta ou sair** | Troca de usuário. Cada perfil tem dados separados |
| **Iniciar com Windows** | Abre a assistente automaticamente ao ligar o PC |
| **Escuta contínua ao iniciar** | Já começa ouvindo o nome dela ao abrir |
| **Alterar nome da IA** | Novo nome (e palavra de ativação) |
| **Editar personalidade** | Define tom, estilo e preferências dela |
| **O que ela sabe** | Ver, corrigir, adicionar e apagar memórias e pendências |
| **API e modelos** | Provedor, chave e escolha automática ou manual de modelos |
| **Voz e ativação** | Voz, idioma, tempo real, palavra de ativação, resposta ao ser chamada e casa inteligente |
| **Áudio e microfone** | Dispositivos, nível, calibração e teste da ativação |
| **Vozes da casa** | Reconhecimento de quem está falando |
| **WhatsApp** | Modo de conexão do WhatsApp |
| **Permissões** | O que ela pode fazer sozinha (ver abaixo) |
| **Especialistas** | Ligar, desligar, editar e criar especialistas |
| **Adicionar aplicativos** | Programas que ela pode abrir por comando |
| **Tablet / acesso remoto** | QR code para parear celular ou tablet |
| **Exemplos de comandos** | Lista de coisas para pedir |

### Permissões

Em vez de perguntar no meio da conversa, ela segue o que você decidir em **Permissões**.
Leitura (ver tela, ler arquivos, consultar agenda) é sempre liberada.

| Categoria | O que inclui | Padrão |
|---|---|:---:|
| **Alterações** | Controlar a casa, criar lembretes, tarefas e eventos, mexer em arquivos, clicar e digitar no navegador | ✅ Liberado |
| **Mensagens** | Enviar mensagens, áudios e arquivos pelo WhatsApp ou digitar em outros apps em seu nome | ⛔ Bloqueado |
| **Ações destrutivas** | Apagar arquivos, cancelar eventos, lembretes e tarefas, limpar a memória | ⛔ Bloqueado |
| **Serviços externos** | Usar conectores MCP que leem ou alteram dados fora do PC | ⛔ Bloqueado |

Quando algo está bloqueado, ela avisa e indica onde liberar.

---

## Exemplos do que pedir

<details open>
<summary><b>Dia a dia</b></summary>

```text
como está meu dia?
vai chover hoje?
crie um lembrete para 18:30 beber água
crie um evento amanhã às 14:00 chamado reunião
crie uma tarefa revisar contrato no projeto Trabalho
ativar modo silencioso
configurar não perturbe das 22:00 às 07:00
```
</details>

<details>
<summary><b>Computador e internet</b></summary>

```text
abra o VS Code
abra o YouTube e pesquise por inteligência artificial
pesquise as notícias de hoje e resuma
veja o que está aberto na tela
pause a música
organize a pasta Downloads
resuma este arquivo            (anexe pelo botão +)
executar tarefa preencher relatório 5x
```
</details>

<details>
<summary><b>Casa e mensagens</b></summary>

```text
ligue a luz da sala
mude a luz da sala para azul
a luz da cozinha está ligada?
apague todas as luzes
mande uma mensagem para João dizendo que chego às 18h
mande um áudio para João dizendo reunião confirmada
mensagens não lidas
```
</details>

<details>
<summary><b>Matemática, ciência e 3D</b></summary>

```text
resolva o sistema x + y = 10; x - y = 2
calcule a integral de x^2 de 0 a 2
gráfico de f(x)=x^2 - 3x + 2
simular lançamento v0=20 angulo=45
qual é a fórmula de Bhaskara?
distância entre Cuiabá e Campo Grande
modelo 3d de um cubo 40mm com furo 10mm
crie duas engrenagens com um eixo
```
</details>

<details>
<summary><b>Especialistas</b></summary>

```text
tenho um bug nesse código python        (chama o Programador)
cria um logo e uma paleta de cores      (chama o Design)
compare o iPhone e o Galaxy             (chama o Pesquisador)
modo design  /  modo programador  /  modo pesquisador
modo normal
```
</details>

<details>
<summary><b>Sobre ela mesma</b></summary>

```text
mude sua voz para marin
pare de falar  /  pode voltar a falar
mostre toda a minha memória
```

Para encerrar a conversa, é só falar natural. Ela se despede e para de ouvir
até você chamar de novo:

```text
tchau  /  até mais  /  até amanhã
obrigado, era só isso
valeu, Luna
deixa pra lá
pode parar de ouvir
```
</details>

---

## Celular e tablet (Android)

O app transforma um celular ou tablet num "satélite" da assistente: você fala com ele e quem
responde é a assistente do PC, pelo Wi-Fi de casa. No tablet deitado, a tela fica igual à do PC.
Ele também atende quando você diz **"Luna"**, sem tocar na tela.

1. **No PC:** **⋯ Mais opções → Tablet / acesso remoto**. Na primeira vez, marque
   **Permitir que tablets e celulares desta rede se conectem** e reinicie a assistente.
2. **No celular:** baixe e abra o `AI-Assistant-<versão>-Android.apk`. Se o Android pedir,
   permita instalar apps desta fonte. O aviso aparece porque o app não vem da Play Store.
3. Abra o app, informe o cômodo e toque em **Escanear QR do computador**.
4. Escaneie o QR que aparece no PC e permita **microfone** e **notificações**.
5. Aguarde o estado **Pronta**. Depois disso ele reconecta sozinho.

> [!WARNING]
> O QR vale uma única vez e expira em 5 minutos. PC e celular precisam estar **no mesmo Wi-Fi**.
> Use só em redes de confiança, como a de casa: a conexão na rede local não é criptografada.
> **Nunca** abra a porta 8000 do roteador para a internet.

---

## Integrações

<details>
<summary><b>WhatsApp</b></summary>

<br>

Precisa do **Google Chrome** ou do **Microsoft Edge** (o Edge já vem no Windows).

1. Na primeira vez que você pedir algo do WhatsApp, abre uma janela com o WhatsApp Web.
2. No celular: **WhatsApp → Aparelhos conectados → Conectar aparelho** e escaneie o QR.
3. Pronto, a sessão fica salva.

Para enviar mensagens sem confirmação, libere **Mensagens** em **Permissões**.
O modo de conexão (serviço interno, Chrome, Opera GX ou depuração remota) fica em
**⋯ Mais opções → WhatsApp**. O serviço interno, que é o padrão, é o único que lê as não lidas.

</details>

<details>
<summary><b>Home Assistant (casa inteligente)</b></summary>

<br>

1. No Home Assistant: **Perfil → Segurança → Tokens de acesso de longa duração → Criar token**.
2. No app: **Voz e ativação → Casa inteligente**.
3. Informe a URL (ex.: `http://homeassistant.local:8123`) e o token, e clique em **Testar conexão**.

Luzes (incluindo cor), interruptores e aparelhos comuns funcionam, e ela entende jeitos
naturais de falar, como "liga ele pra mim". **Portões, fechaduras e alarmes são bloqueados de
propósito**, por segurança.

</details>

<details>
<summary><b>Calendário</b></summary>

<br>

Em **⚙️ Central de configurações → Calendário**:

| Provedor | O que precisa |
|---|---|
| **Local** | Nada, funciona na hora |
| **Google Calendar** | Clique em **Conectar Google Calendar** e entre com sua conta (veja a nota abaixo) |
| **iCloud** | Usuário Apple e uma *senha específica de app* |
| **CalDAV** | URL HTTPS, usuário e senha de aplicativo |
| Microsoft 365 / Outlook | Ainda não disponível nesta versão |

> [!NOTE]
> O Google ainda não concluiu a verificação do app. No login aparece **"O Google não verificou este app"**:
> clique em **Avançado → Acessar AI Assistant (não seguro)** e depois em **Continuar**. O app só pede acesso
> aos eventos da agenda. Detalhes na [Política de Privacidade](https://caiolfreitas98.github.io/ai-assistant-releases/privacidade.html).

</details>

<details>
<summary><b>Palavra de ativação</b></summary>

<br>

Por padrão ela reconhece o próprio nome. Para uma ativação mais leve e rápida, que escuta
"Luna" sem transcrever tudo:

1. **Áudio e microfone → Palavra de ativação**.
2. Em *Detector*, escolha **Modelo local openWakeWord**.
3. Clique em **Testar ativação** e diga o nome. A pontuação deve passar do limiar (0,50).
4. **Salvar e aplicar**.

Ativa sozinha com a TV ligada? Suba o limiar para 0,6–0,7. Não ouve quando você chama?
Baixe para 0,3–0,4.

</details>

---

## Atualizações

A partir da versão **1.0.1**, a assistente procura atualizações sozinha ao abrir e a cada 6 horas.
Quando sai uma versão nova, aparece uma barra no topo da janela:

> **Nova versão disponível.** · Novidades · Depois · **Atualizar agora**

Ao clicar em **Atualizar agora**, ela baixa, confere o arquivo, instala e reabre sozinha.
Suas conversas, memórias e configurações são mantidas.

> [!NOTE]
> Quem instalou a **1.0.0** precisa baixar a próxima versão manualmente **uma vez**. Depois disso,
> as atualizações chegam sozinhas. No Android, instale o novo `.apk` por cima do antigo.

---

## Privacidade

- **Ficam só no seu PC:** conversas, memórias, configurações, macros e vozes cadastradas, em
  `%LOCALAPPDATA%\Programs\AI Assistant\` (pastas `data\` e `configs\`).
- **Chaves e senhas:** guardadas no Cofre de credenciais do Windows, nunca em arquivo de texto.
- **Vai para a internet:** o que você diz e pede é enviado ao provedor de IA que você configurou,
  para gerar as respostas. Com **Ollama** e **Piper/Whisper locais**, dá para usar tudo offline.
- Ações sensíveis ficam registradas em `data\audit\security.jsonl`.

---

## Problemas comuns

| Problema | O que fazer |
|---|---|
| "O Windows protegeu o computador" | **Mais informações → Executar assim mesmo** |
| Demora para abrir na primeira vez | Normal (até 1 min), só na primeira abertura |
| Ela só faz contas e abre apps | Falta a chave de API em **API e modelos** |
| Não ouve quando eu chamo | **Áudio e microfone**: confira o microfone e calibre |
| Ativa sozinha com barulho | Aumente o limiar da palavra de ativação ou cadastre sua voz em **Vozes da casa** |
| Celular não conecta | Mesmo Wi-Fi? Marcou **Permitir que tablets e celulares…** e reiniciou? Gere um QR novo |
| WhatsApp não abre | Instale o Chrome ou use o Edge. Escaneie o QR de novo |
| Ela diz que não tem permissão | Libere a categoria em **Permissões** |

### Reportar um erro
O registro fica em:

```text
%LOCALAPPDATA%\Programs\AI Assistant\data\logs\assistant.log
```

Ao [abrir uma issue](https://github.com/CaioLFreitas98/ai-assistant-releases/issues/new), conte o que
você fez, o que esperava e o que aconteceu, e anexe esse arquivo. **Antes de enviar, confira que ele
não tem nada pessoal** que você prefira não compartilhar.

---

## Desinstalar

**Configurações do Windows → Aplicativos → AI Assistant → Desinstalar.**

Seus dados (`data\` e `configs\`) são mantidos para uma reinstalação. Para apagar tudo, remova
também a pasta `%LOCALAPPDATA%\Programs\AI Assistant`. As chaves ficam no **Gerenciador de
Credenciais** do Windows e podem ser removidas por lá.

---

<div align="center">
<sub>O código-fonte é privado por enquanto. Este repositório guarda só os instaladores.<br>
Novidades de cada versão: <a href="https://github.com/CaioLFreitas98/ai-assistant-releases/releases">Releases</a> · <a href="HISTORICO.md">Cronograma completo</a>.</sub>
</div>
