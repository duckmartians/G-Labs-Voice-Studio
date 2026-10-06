<h1 align="center">G-Labs Voice Studio</h1>

<p align="center"><b>Um app desktop de voz com IA que roda no seu próprio computador — clone uma voz a partir de poucos segundos de áudio, leia textos em mais de 600 idiomas, crie diálogos com várias vozes, transcreva áudio/vídeo em legendas e traduza legendas com IA.</b></p>

<p align="center">
  <a href="README.md">Tiếng Việt</a> ·
  <a href="README.en.md">English</a> ·
  <b>Português</b> ·
  <a href="README.tr.md">Türkçe</a> ·
  <a href="README.zh-CN.md">简体中文</a> ·
  <a href="README.hi.md">हिन्दी</a> ·
  <a href="README.bn.md">বাংলা</a> ·
  <a href="README.ur.md">اردو</a> ·
  <a href="README.ru.md">Русский</a>
</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G"><img alt="Baixar para Windows" src="https://img.shields.io/badge/Baixar-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"></a>&nbsp;
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta"><img alt="Baixar para macOS (Apple Silicon)" src="https://img.shields.io/badge/Baixar-macOS%20Apple%20Silicon-000000?style=for-the-badge&logo=apple&logoColor=white"></a>
</p>

---

## Instalação

### Passo 1 — Escolha a versão certa para o seu computador

As versões são distribuídas pelas pastas oficiais do Google Drive:

| Seu computador | Google Drive | Observação |
|---|---|---|
| 🪟 **Windows 10/11 (64 bits)** | [Windows](https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G) | Um `.zip` — extraia e execute, sem instalador |
| 🍎 **Mac com chip Apple (M1/M2/M3/M4…)** | [macOS Apple Silicon](https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta) | Um `.dmg`, requer macOS 12 ou mais recente |

> **Macs com Intel não são suportados** — só existe versão para Apple Silicon. Não sabe qual chip o seu Mac tem? Clique no menu  → **Sobre Este Mac**: uma linha **Chip** com "Apple M…" funciona; uma linha **Processador** com "Intel…" não.

### Passo 2 — Instalar

<details open>
<summary><b>🪟 No Windows</b></summary>

1. Baixe o `.zip` do Windows (por exemplo `G-Labs-Voice-Studio-v2.0.2-win.zip`) e **extraia** para qualquer pasta — o disco precisa de pelo menos 10 GB livres (os modelos de IA baixados depois ocupam vários GB).
2. Abra a pasta extraída e execute **`G-Labs-Voice-Studio.exe`** (todo o resto fica na subpasta `data` — não a mova).
3. Se aparecer **"O Windows protegeu o computador"** (SmartScreen): clique em **Mais informações** → **Executar assim mesmo**. *(O app não é assinado com certificado da Microsoft, por isso o Windows avisa — não é vírus.)*
4. **Crie um atalho:** clique com o botão direito em `G-Labs-Voice-Studio.exe` → **Enviar para** → **Área de trabalho (criar atalho)** para abrir rápido da próxima vez.

> ⏳ **A primeira abertura pode levar 30–60 segundos** (a tela de abertura fica parada) enquanto o Windows faz a verificação de segurança do app e das bibliotecas gráficas. Aguarde, não feche — as próximas aberturas são mais rápidas.

</details>

<details open>
<summary><b>🍎 No macOS</b></summary>

1. Abra o **`.dmg`** baixado e **arraste o ícone do G-Labs Voice Studio para a pasta Aplicativos**.
2. Em **Aplicativos**, **clique com o botão direito** (ou Control-clique) em **G-Labs Voice Studio** → **Abrir** → clique em **Abrir** de novo na confirmação. *(O app não é notarizado pela Apple, então você o abre assim na **primeira vez**; depois ele abre normalmente.)*
3. Se o macOS disser que o app **"está danificado / não pode ser aberto"** ou não houver botão Abrir, abra o **Terminal**, cole isto e pressione Enter:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"
   ```
   Depois abra o app de novo. Alternativa: **Ajustes do Sistema → Privacidade e Segurança**, role até o fim e clique em **Abrir Mesmo Assim** ao lado da mensagem sobre o G-Labs Voice Studio bloqueado.

> ⏳ **A primeira abertura pode levar 30–60 segundos** enquanto o macOS verifica a segurança de todo o app. As próximas são mais rápidas.

</details>

### Passo 3 — Entrar e escolher um plano

**Você precisa entrar com o Google** (Configurações ⚙️ → aba **Contas com licença** → **Entrar com Google**) para o app verificar sua licença. Uma conta roda em **um computador por vez** — entrar em outro dispositivo encerra a sessão no anterior.

| Plano | Preço | Inclui |
|---|---|---|
| **Avaliação** | Grátis | Linhas limitadas por geração (1 por padrão) — o bastante para checar se seu computador roda bem antes de comprar |
| **Plano Studio** | 1 mês $5 · 6 meses $25 · 1 ano $50 (100.000đ / 500.000đ / 1.000.000đ via VietQR) | Linhas ilimitadas, **Fila de renderização**, aba **Tradução**, **Webhook API** |

- Compre dentro do app (Configurações → **Contas com licença**) por **transferência VietQR**, **PayPal** (cartão internacional) ou **USDT**. Os planos são por período, não renovam automaticamente e são ativados na conta Google com que você entrou.
- O Plano Studio é só do Voice Studio e é **separado** do Plus/Max do G-Labs Studio.
- Reembolso disponível nas primeiras **24 horas** após o pagamento — veja a [Política de reembolso](https://duckspace.net/refunds.html#en). Rode a avaliação grátis antes para ter certeza de que seu computador dá conta.

---

## Primeira execução

1. **Abra o app e escolha o idioma da interface** na tela de boas-vindas (dá para mudar depois nas Configurações).
2. **Entre com o Google** — Configurações ⚙️ → **Contas com licença** → **Entrar com Google**.
3. **Baixe o modelo de voz** — abra a aba **Gerenciar Modelos** (ou siga o aviso do app) e baixe o modelo de voz de IA (vários GB, só uma vez). Os modelos de reconhecimento de fala são baixados separadamente na primeira vez que você os usa.
4. **Abra a aba Ler Texto**, escolha o **idioma de saída** e uma voz da biblioteca (30 vozes prontas).
5. Cole o texto → **Adicionar à tabela** → **Iniciar**. Ouça cada linha e clique em **Exportar áudio** para salvar o arquivo (com legenda `.srt` por padrão).

---

## Recursos

<p align="center">
  <img alt="Interface do G-Labs Voice Studio" width="900" src="https://github.com/user-attachments/assets/d7a08f20-3aee-43ed-bbba-b80997720fdb" />
</p>

- **Roda no seu computador** — depois de baixar os modelos, a geração de voz e a transcrição rodam localmente (GPU NVIDIA, Apple Metal ou CPU); seu áudio e texto não vão para um servidor. Só a aba de tradução envia o texto das legendas ao provedor de IA que você escolher.
- **Clonagem de voz** — a partir de uma amostra de 5–10 segundos, leia qualquer texto exatamente com aquela voz.
- **Design de voz** — crie uma voz nova por gênero, idade, tom, estilo e sotaque; sem arquivo de amostra.
- **Mais de 600 idiomas de saída** — vietnamita, inglês, chinês, japonês, coreano, francês, alemão, espanhol e muitos outros.
- **Diálogo com várias vozes** — roteiros `<Nome>: fala`, cada personagem com sua voz e velocidade.
- **Extração de legendas** — transcreve MP3, WAV, M4A, FLAC, MP4, MOV…; exporta TXT ou SRT com tempo por palavra.
- **Tradução de legendas com IA** *(Plano Studio)* — traduza ou revise `.srt`, `.vtt`, `.ass`, `.sbv`, `.txt`; tempos e número de linhas ficam exatamente iguais.
- **Biblioteca de vozes** — 30 vozes prontas, salve as suas, fixe ⭐ favoritas, faça backup/restauração em arquivo `.vcp`.
- **Ajuste fino de áudio** — 6 modos de processamento, nivelamento de volume, 13 tags de expressão e um dicionário de pronúncia que lembra como ler `100%`, `25°C`, `m²`.
- **Exportação flexível** — WAV ou MP3, um arquivo único ou um por frase, com `.srt`; baixe uma linha só pelo botão ⬇.
- **Fila de renderização** *(Plano Studio)* — enfileire vários roteiros; o app executa um após o outro e salva os arquivos.
- **Webhook API** *(Plano Studio)* — servidor REST local para n8n, Make, Zapier, Python/cURL ou agentes de IA.
- **Cuida do seu hardware** — placa de vídeo incompatível passa para CPU com aviso claro; a memória da GPU é liberada automaticamente quando ocioso.
- **9 idiomas de interface** — Tiếng Việt, English, Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский.

---

## Páginas

As páginas ficam na barra lateral esquerda. As três páginas de voz (Clonar Voz, Ler Texto, Diálogo em Grupo) seguem o mesmo ritmo: escolha o **idioma de saída** → cole o texto ou **Importar** (`.txt`, `.srt`) → **Adicionar à tabela** (o app divide as frases pelo **Modo de divisão** escolhido, com prévia do número de linhas) → **Iniciar** → ouça → **Exportar áudio**.

### 🔊 Clonar Voz

Clique em **Selecionar...** para carregar o áudio de amostra (voz clara, pouco ruído) e **arraste a caixa destacada na forma de onda** para escolher exatamente o trecho de 3–30 segundos — ao soltar, as bordas se ajustam ao silêncio mais próximo; arquivos com mais de 5 minutos / 50 MB usam os primeiros 30 segundos. O campo *Texto da amostra* é **obrigatório** e deve corresponder exatamente às palavras da amostra (pontuação e grafia incluídas); **✨ Sugerir com IA** transcreve para você, mas confira antes de gerar. Ao terminar a clonagem, o app convida você a ouvir e salvar a voz na biblioteca com um clique.

### 🎛️ Ler Texto

Escolha uma voz da biblioteca ou abra **Design de Voz** para criar uma nova por *gênero, idade, tom, estilo, sotaque*. Gostou da voz criada? Selecione a linha na tabela → **Salvar** na biblioteca para reutilizar. O modo **Mesclagem inteligente** junta frases curtas em linhas fluidas até um limite de caracteres, sempre quebrando no fim de uma frase. O botão **Etiquetas de expressão** permite consultar tags e **inseri-las** no cursor.

### 💬 Diálogo em Grupo

Escreva um roteiro com vários personagens — ótimo para podcasts, audiodramas e entrevistas:

```
<Apresentador>: Bem-vindos a todos.
<Mai>: Oi, estou muito feliz de estar no programa.
<Minh>: Eu também — sobre o que vamos falar hoje?
```

Coloque o nome do personagem entre `< >` no início da linha (o `:` é opcional, nomes não diferenciam maiúsculas). Clique em **Diálogo de exemplo** para ver um exemplo e depois em **Analisar diálogo** — o painel **Atribuição de vozes** se abre para dar a cada personagem uma voz da biblioteca e seu próprio controle de **velocidade** (0.5× → 2×).

### 📝 Extrair Legendas

Escolha um arquivo de áudio/vídeo (MP3, WAV, M4A, FLAC, MP4, MOV…), o idioma falado e um modelo de reconhecimento (Tiny → Large v3, cada um mostrando a VRAM necessária) e execute. As linhas de legenda são montadas a partir do tempo de cada palavra e quebram em pausas reais / fim de frase / limite de caracteres; altere os campos *máx. de caracteres, máx. de segundos, limiar de pausa* e a tabela se atualiza na hora, sem transcrever de novo. Edite direto na tabela e exporte `.txt` ou `.srt`.

### 🌐 Tradução *(Plano Studio)*

Traduza legendas para outro idioma ou revise ortografia e quebras de linha — **só o texto muda; tempos e número de linhas ficam iguais**.

1. Configuração única em **Gerenciar Modelos → LLM**: escolha **9Router** (um gateway rodando na sua máquina — informe endereço + chave de API), **Claude CLI**, **Antigravity** (`agy`) ou **Codex CLI** (instale e faça login). Cada linha tem um botão **Guia** com o comando de instalação; depois de instalar, clique em **Atualizar lista** e o app detecta e lista os modelos.
2. **Importar** `.srt`, `.vtt`, `.ass`, `.sbv`, `.txt` — ou **Das Legendas**. Um `.txt` não tem tempos, então o app atribui tempos provisórios e avisa.
3. Recomendado: **Organizar o texto** junta fragmentos cortados no meio da frase (comum em legendas exportadas de editores de vídeo), com prévia como *"120 linhas → 68 linhas"* antes de aplicar.
4. Escolha **Traduzir**, **Editar** ou **Traduzir + Editar**, o idioma de destino e o modelo, e clique em **Iniciar**.
5. A **Tabela de consistência** fixa nomes, termos e formas de tratamento para o arquivo inteiro e é enviada com cada trecho; você pode editá-la e, opcionalmente, parar para revisá-la antes de traduzir.
6. Confira a coluna **Resultado** (linhas que a IA deixou de fora ficam marcadas com ⚠ e mantêm o texto original), escolha **SRT / VTT / TXT** e clique em **Exportar**.

### 📚 Gerenciar Modelos

Uma linha por modelo com tamanho e status: o modelo de voz de IA e os tamanhos de reconhecimento (Tiny, Base, Small, Turbo, Large v3). Baixe só o que precisar e mude a **pasta dos modelos** (por exemplo para o disco D, poupando o C — copie a pasta antiga de modelos ou deixe o app baixar de novo). Aqui também ficam o provedor **LLM** da tradução e o temporizador **Liberar VRAM automaticamente**.

### 🗒 Fila de renderização *(Plano Studio)*

Em vez de gerar um roteiro e exportar à mão, clique em **Adicionar à fila** para salvar o roteiro + voz + configurações atuais como uma tarefa com **nome e pasta de saída próprios**. Clique em **Executar fila** e o app processa uma por uma, salvando os arquivos. Cada tarefa mostra `X/N frases` para você ver qual ficou faltando linhas por erro; **Recarregar** traz a tarefa de volta à aba para corrigir (linhas com falha marcadas com ❌). A fila sobrevive a fechar e reabrir o app.

### 🔗 Webhook API *(Plano Studio)*

Um servidor REST local para que n8n, Make, Zapier, Python/cURL ou agentes de IA gerem voz automaticamente. Padrão `127.0.0.1:8766` (só este computador), com chave de API, campo **URL** completo com botão de copiar, opção de iniciar junto com o app e log de requisições ao vivo. Troque o IP para `0.0.0.0` / IP da rede local para outros dispositivos chamarem — a chave de API então trafega por HTTP sem criptografia. Esquema completo: [`docs/WEBHOOK_INTEGRATION.en.md`](docs/WEBHOOK_INTEGRATION.en.md).

---

## Dicas

<details>
<summary><b>Masterização de áudio — 6 modos de processamento</b></summary>

Na seção **Masterização de áudio** das três abas de voz (mude em uma e as outras acompanham):

- 📻 **Radiodifusão** *(padrão)* — padrão rádio/podcast, quente, comprimido.
- 🎬 **Cinema** — reverberação ampla, compressão suave.
- 🎙️ **Podcast** — microfone próximo, compressão forte, sem reverberação.
- ☀️ **Quente** — médios-graves reforçados, aconchegante.
- ✨ **Brilhante** — agudos nítidos, arejado.
- 🔇 **Bruto** — a saída do modelo como está.

**Equalizar volume entre as falas** nivela pela intensidade percebida (RMS), acabando com linhas altas e baixas. Para a saída intocada do modelo, escolha **Bruto** e desmarque essa opção.

</details>

<details>
<summary><b>Etiquetas de expressão</b></summary>

Digite uma tag no texto (mantenha os colchetes; sozinha ou no meio da frase, ex.: `Que engraçado [laughter] não consigo parar.`) — a voz faz o som em vez de ler a palavra. Não precisa decorar: o botão **Etiquetas de expressão** permite consultar e inserir.

| Tag | Som |
|---|---|
| `[laughter]` | Risada |
| `[sigh]` | Suspiro |
| `[confirmation-en]` | Concordância — "mm-hmm" |
| `[question-en]` · `[question-ah]` · `[question-oh]` · `[question-ei]` · `[question-yi]` | Entonação de pergunta |
| `[surprise-ah]` · `[surprise-oh]` · `[surprise-wa]` · `[surprise-yo]` | Surpresa |
| `[dissatisfaction-hnn]` | Irritação — "hnn" |

A intensidade varia conforme o idioma e a voz — teste antes numa frase curta.

</details>

<details>
<summary><b>Dicionário de pronúncia</b></summary>

Texto com `%`, `$`, `°C`, `m²`, nomes de marcas…? Clique em **Ajustar pronúncia** antes de gerar: o app pergunta como ler cada símbolo/palavra, você digita a leitura uma vez (ex.: `%` → `por cento`) e ele lembra por idioma de saída.

</details>

<details>
<summary><b>Velocidade e legendas na exportação</b></summary>

- **Velocidade de leitura** fica em *Configurações avançadas*; o controle **Velocidade** do player permite ouvir mais rápido/lento, e o arquivo exportado mantém essa velocidade sem distorcer o tom.
- **Exportar legendas também** grava um `.srt` correspondente ao lado do áudio, com tempos tirados da duração real de cada frase após o ajuste de velocidade.
- **Ajustar a fala ao tempo das legendas**: quando o roteiro veio de um `.srt`, cada linha é acelerada (máx. 1.8×) para caber no seu intervalo — nunca desacelerada.

</details>

<details>
<summary><b>Liberação automática de memória</b></summary>

Deixe o app ocioso por um tempo (5 minutos por padrão) e o modelo de IA é descarregado da VRAM/RAM para aliviar o computador; ele recarrega na próxima ação. Altere o tempo ou desative em **Gerenciar Modelos → Liberar VRAM automaticamente**.

</details>

---

## Requisitos do sistema

|   | Mínimo | Recomendado |
|---|---|---|
| **Sistema operacional** | Windows 10 (64 bits), macOS 12 em Apple Silicon | Windows 11, macOS 13 ou mais recente |
| **RAM** | 8 GB | 16 GB ou mais |
| **Disco** | 10 GB livres (modelos + cache) | 20 GB ou mais, SSD |
| **GPU** | Opcional — roda na CPU | NVIDIA RTX série 20 ou mais nova, 8 GB de VRAM · Macs usam Metal |
| **Rede** | Internet para login/verificação de licença e download dos modelos | |

- **Windows:** a aceleração por GPU exige uma placa NVIDIA **RTX série 20 ou mais nova** (compute capability ≥ 7.0) e driver com suporte a CUDA 12.8. Placas mais antigas, como a série GTX 10, são detectadas automaticamente e rodam na CPU.
- **macOS:** só **Apple Silicon** (M1/M2/M3/M4…), acelerado com Metal.
- O modo CPU é cerca de 5–10× mais lento que a GPU, mas serve bem para narrações curtas.

---

## Onde ficam seus dados

| O quê | Windows | macOS |
|---|---|---|
| Áudio exportado (padrão) | `output\` dentro da pasta onde você extraiu o app | `~/Documents/G-Labs Voice Studio/output` |
| Configurações, sessão de login | `%APPDATA%\G-Labs Voice Studio` | `~/Library/Application Support/G-Labs Voice Studio` |
| Sua biblioteca de vozes | `%APPDATA%\G-Labs Voice Studio\voice_studio\voices` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/voices` |
| Modelos de IA | `%APPDATA%\G-Labs Voice Studio\voice_studio\model` (ou a pasta que você escolher) | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/model` (ou a pasta que você escolher) |
| Fila de renderização | `%APPDATA%\G-Labs Voice Studio\voice_studio\queue` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/queue` |

Para levar sua biblioteca de vozes a outro computador, use **backup/restauração `.vcp`** no painel da biblioteca de vozes.

---

## Solução de problemas

**A primeira abertura é muito lenta, a tela de abertura não se mexe** — o Windows/macOS está fazendo a primeira verificação de segurança; aguarde 30–60 segundos, não feche. As próximas são mais rápidas.

**O Windows para em "O Windows protegeu o computador"** — clique em **Mais informações → Executar assim mesmo**. O app não é assinado com certificado da Microsoft; não é vírus.

**O macOS diz que o app está danificado / não pode ser aberto** — ele não é notarizado pela Apple. Botão direito → **Abrir** na primeira vez, ou rode `xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"`.

**Aviso de que passou a rodar na CPU** — sua placa de vídeo não é compatível (ex.: série GTX 10). Tudo continua funcionando, só mais devagar; para velocidade você precisa de uma NVIDIA RTX série 20 ou mais nova, ou um Mac Apple Silicon.

**Só 1 linha é gerada por vez** — você está na avaliação. Compre o Plano Studio para linhas ilimitadas.

**Saiu da conta com aviso de login em outro dispositivo** — uma conta roda em um computador por vez; entre de novo no computador que quer usar.

**A voz clonada diz palavras erradas / desvia** — o *Texto da amostra* deve corresponder exatamente às palavras da amostra; escolha uma amostra clara, com pouco ruído.

**Caracteres especiais lidos errado (`100%`, `25°C`…)** — adicione a leitura em **Ajustar pronúncia**.

**O disco C está enchendo com os modelos** — mude a pasta dos modelos em **Gerenciar Modelos** e depois copie a pasta antiga ou deixe o app baixar de novo.

**Nenhum modelo para escolher na aba Tradução** — instale e faça login num provedor LLM (9Router, Claude CLI, Antigravity, Codex) seguindo o botão **Guia** e clique em **Atualizar lista**.

**Precisa de detalhes do erro** — clique em **Logs Detalhados** na barra lateral.

---

📖 [Página do produto](https://duckspace.net/en/voice-studio/) · [Guia](https://duckmartians.info/voice/guide/en/) · [Changelog](CHANGELOG.md) · [Discord](https://discord.gg/munMZEBMw5)

© 2026 Duck Martians AI Labs. Todos os direitos reservados.
