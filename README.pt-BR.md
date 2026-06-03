<p align="right">
<a href="./README.md">🇻🇳 Tiếng Việt</a> ·
<a href="./README.en.md">🇬🇧 English</a> ·
🇧🇷 Português ·
<a href="./README.tr.md">🇹🇷 Türkçe</a> ·
<a href="./README.zh-CN.md">🇨🇳 简体中文</a> ·
<a href="./README.hi.md">🇮🇳 हिन्दी</a> ·
<a href="./README.bn.md">🇧🇩 বাংলা</a> ·
<a href="./README.ur.md">🇵🇰 اردو</a> ·
<a href="./README.ru.md">🇷🇺 Русский</a>
</p>

<h1 align="center">G-Labs Voice Studio</h1>
<p align="center">Estúdio de voz com IA para criadores de conteúdo</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G">
    <img alt="Download Windows" src="https://img.shields.io/badge/Download%20Windows-%F0%9F%92%BB-0078D6?style=for-the-badge&logo=windows&logoColor=white">
  </a>
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta">
    <img alt="Download macOS" src="https://img.shields.io/badge/Download%20macOS-%F0%9F%8D%8E-000000?style=for-the-badge&logo=apple&logoColor=white">
  </a>
</p>

<p align="center">
  <a href="https://duckmartians.info/voice">
    <img alt="Homepage" src="https://img.shields.io/badge/Homepage-Visit-0A66C2?style=flat-square&logo=google-chrome&logoColor=white">
  </a>
  <a href="https://discord.gg/munMZEBMw5">
    <img alt="Discord" src="https://img.shields.io/badge/dynamic/json?url=https://discord.com/api/guilds/1369302820037201981/widget.json&query=$.presence_count&label=Discord&color=5865F2&logo=discord&style=flat-square">
  </a>
</p>

O **G-Labs Voice Studio** é um aplicativo de desktop para síntese de voz multilíngue: clone vozes a partir de um trecho curto de referência, crie novas vozes por atributos, escreva diálogos com vários personagens e transcreva fala em texto. Interface com tema escuro, modelos rodando localmente na sua máquina — nenhum áudio ou texto sai do dispositivo depois que o modelo é baixado.

<p align="center">
  <a href="https://duckmartians.info/voice">
    <img alt="G-Labs Voice Studio UI" width="900" src="https://github.com/user-attachments/assets/d7a08f20-3aee-43ed-bbba-b80997720fdb" />
  </a>
</p>

---

## Recursos

- **🔊 Clone de Voz** — forneça um trecho de referência de 5–10 segundos; o app lê qualquer texto naquela voz.
- **🎛️ Texto para Voz / TTS** — descreva uma voz por atributos (gênero, idade, tom, estilo, sotaque) sem precisar de áudio de referência.
- **💬 Diálogo de Várias Vozes** — escreva um roteiro com vários personagens usando a sintaxe `<Nome>: fala` e atribua uma voz da biblioteca a cada personagem.
- **📝 Voz para Texto (ASR)** — transcreva arquivos de áudio/vídeo. Suporta MP3, WAV, M4A, FLAC, MP4, MOV…
- **🗂 Biblioteca de Vozes + 30 vozes de fábrica** — o app já vem com 30 vozes prontas (masculinas/femininas, tons variados). Você também pode salvar as suas. Marque ⭐ uma voz para fixá-la no topo, e faça **backup e restauração** como arquivos `.vcp` portáteis para compartilhar.
- **🎚 Controle de velocidade + exportação que respeita a velocidade** — mude a velocidade da prévia abaixo da forma de onda; o arquivo exportado toca exatamente naquela velocidade (tom preservado).
- **📄 Exportação de legendas (SRT)** — ao exportar como um único arquivo mesclado, o `.srt` é gerado automaticamente ao lado, pronto para edição de vídeo.
- **🔤 Dicionário fonético pessoal** — encontrou `100%`, `25°C`, `m²`? Digite a pronúncia uma vez, o app lembra para a próxima (por idioma de saída).
- **✨ Sugestão de texto de amostra com IA** — o Whisper transcreve automaticamente o trecho de referência para você não ter que redigitar do zero (ainda revise antes de gerar).
- **⬇ Download por linha** — cada linha da tabela do roteiro tem seu próprio botão de download — sem esperar o lote inteiro.
- **Mais de 600 idiomas suportados** — fale em mais de 600 idiomas (vietnamita, inglês, chinês, japonês, coreano, francês, alemão, espanhol e muitos idiomas minoritários).
- **Processamento em lote** — importe roteiros `.txt` ou `.srt`, rode lotes, exporte áudio preservando os tempos.
- **Verificação inteligente de compatibilidade de GPU** — se sua GPU não consegue rodar os kernels acelerados, o app **muda automaticamente para CPU multi-core** e te avisa de forma clara, em vez de travar com um erro de CUDA.
- **Interface em 9 idiomas** — Tiếng Việt, English, Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский.

---

<details open>
<summary><b>🆕 Novidades na v1.0.7</b></summary>

- **🔊 A aba Clonar Voz, refeita para ser mais simples** — a biblioteca foi dividida em duas colunas claras (**Vozes integradas** / **Suas vozes**) e a caixa de texto foi reduzida a uma linha. Após clonar, o app sugere ouvir e pergunta se você quer salvar a voz — salvar é um toque. Áudio de amostra com mais de 30 segundos é **cortado automaticamente** em uma pausa para uma clonagem mais limpa.
- **🎛 Uma aba Texto → Fala mais organizada** — "Biblioteca de vozes" e "Design de voz" foram unidas em **um único quadro**; alterne entre **Usar uma voz salva** ↔ **Voz aleatória**, sem bagunça.
- **▶ Ouça as vozes integradas** — clique no ▶ ao lado de qualquer voz integrada na biblioteca para ouvi-la antes de usar.
- **⭐ Favoritos sincronizados em todo lugar** — marque uma voz com estrela em uma aba e as outras abas também a veem.
- **🐛 Corrigido: o controle de velocidade causava áudio distorcido / falha na exportação** — removemos o controle de velocidade na barra de pré-visualização (ele causava a distorção e o erro de exportação). Para ler mais rápido/devagar, use o controle **Velocidade de leitura** em *Configurações avançadas* — voz natural, sem erros.
- **✨ Pequenos ajustes** — a pausa padrão entre frases agora é mais curta (100ms) para um fluxo mais suave; os botões de excluir aparecem de forma consistente; interface mais limpa em vários lugares.
- **🎙 Aba Fala → Texto: escolha o modelo de reconhecimento** — do pequeno ao grande (Tiny → Turbo) conforme sua máquina: PCs mais fracos escolhem um modelo pequeno para velocidade, os mais fortes um grande para precisão (cada um mostra a **VRAM necessária**). O modelo padrão fica pronto logo após instalar; os outros baixam com um toque e ficam **salvos no seu computador** — da próxima vez funciona offline.
- **🌍 Escolha o idioma falado** — indicar o idioma (≈100 suportados) melhora a precisão e evita trocas de idioma no meio; além de ajustes que reduzem erros/palavras repetidas em trechos difíceis.

</details>

---

<details>
<summary><b>🆕 Novidades na v1.0.6</b></summary>

- **🔗 Webhook API (novo)** — servidor REST local permite que n8n, Zapier, Python/cURL ou qualquer cliente HTTP dispare geração de voz programaticamente. Painéis de seleção de voz + idioma integrados (clique duplo para copiar), chave de API mascarada `xxxx***xxxx`, autostart, log de requisições em tempo real.
- **🚀 Exportações muito mais rápidas + barra de progresso real** — concatenação e ajuste de velocidade rodam em paralelo nos núcleos da CPU, um projeto de 50 minutos exporta em dezenas de segundos em vez de minutos. Barra de progresso inline avança suavemente 0→100% com botão **Parar** real que cancela no meio do processo.
- **🧹 Abas Clonagem de voz + Fala-para-texto mais enxutas** — Clone removeu botões duplicados da aba Texto-para-fala. ASR junta automaticamente fragmentos curtos em frases completas, preservando a linha do tempo original.
- **💾 Sincronização de configurações entre abas** — *Frases simultâneas* (batch size) agora é compartilhado entre as três abas de geração + limite de concorrência do Webhook; mude em qualquer lugar e tudo mais é atualizado. Abas Clonagem / Texto-para-fala lembram a última predefinição selecionada após reinicialização.
- **🐛 Várias correções** — crash de exportação após timeout de sessão (`AttributeError: NoneType`), estado "modelo baixado" incorreto quando a rede cai durante download deixando safetensors incompletos, botão "Salvar voz" acendendo antes da clonagem terminar de fato.

</details>

---

<details>
<summary><b>🆕 Novidades da v1.0.5</b></summary>

- **🎚 Masterização de áudio profissional (novo)** — escolha um dos 6 modos de processamento (Radiodifusão / Cinema / Podcast / Quente / Brilhante / Bruto) para deixar suas faixas de voz com qualidade de estúdio. Disponível nas 3 abas de geração (Clone de Voz / Texto para Voz / Diálogo de Várias Vozes) — mude em uma aba e as outras ficam sincronizadas.
- **🌐 Divisão de frases melhor para chinês / hindi / árabe / urdu** — antes esses idiomas viravam uma linha só; agora as frases são divididas corretamente com base na pontuação de cada escrita.
- **🧠 Liberação automática de memória quando ocioso** — se o app fica sem uso por 5 minutos (padrão), ele descarrega automaticamente o modelo de IA para liberar a sua máquina. Ajuste o tempo ou desative na aba Configuração do Ambiente.
- **⚙ Mais estável ao gerar e transcrever ao mesmo tempo** — em máquinas com pouca memória isso costumava travar no meio da execução; o app agora lida com a situação automaticamente.

> ⚠️ **Pequena mudança no áudio exportado:** A predefinição padrão **📻 Radiodifusão** + **Equalizar volume entre as falas** fazem os arquivos de voz da v1.0.5 soarem **mais altos e cheios** do que na v1.0.4. Para manter o comportamento antigo, abra qualquer aba de geração → expanda **Masterização de áudio** → escolha **🔇 Bruto** e desmarque **Equalizar volume entre as falas**.

</details>

---

<details>
<summary><b>🆕 Novidades da v1.0.4</b></summary>

- **💬 Aba Diálogo de Várias Vozes (nova)** — escreva roteiros com vários personagens, uma voz por personagem. Clique em **📋 Diálogo de exemplo** para ver um exemplo funcional.
- **🗂 30 vozes de fábrica inclusas** — prontas para usar, sem precisar gravar uma amostra primeiro.
- **⭐ Estrela de favorito** — clique na ☆ ao lado de uma voz para fixá-la no topo da biblioteca.
- **🎚 Controle de velocidade no player** — pré-visualize de 0,5x até 2x, e a exportação mantém essa velocidade exata.
- **📄 Exportação automática de SRT** — ao exportar como arquivo mesclado, o app cria um `.srt` correspondente ao lado do `.wav` (pode ser desativado).
- **🔤 Dicionário fonético para caracteres especiais** — você nunca mais precisará reescrever manualmente "100%" como "cem por cento": digite a pronúncia uma vez, o app lembra para sempre.
- **🌐 9 idiomas de interface** — adicionados Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский (além de vietnamita e inglês).
- **⏳ Tempo decorrido por linha** — veja num relance qual fala está sendo gerada e há quanto tempo está rodando.
- **🌍 O idioma de saída precisa ser selecionado explicitamente** — a opção "Automático" foi removida para evitar pronúncias erradas.

</details>

---

## Instalação

| Plataforma | Arquivo | Tamanho |
|---|---|---|
| Windows x64 | `GLabsVoiceStudio-v1.0.7-win.zip` | ~3 GB |
| macOS Apple Silicon | `GLabsVoiceStudio-v1.0.7-arm64.dmg` | ~2 GB |

### Windows (portátil, não precisa instalar)

1. Baixe `GLabsVoiceStudio-v1.0.7-win.zip`.
2. Extraia para qualquer pasta (o disco precisa ter pelo menos 10 GB livres).
3. Abra a pasta extraída e dê dois cliques em `GLabsVoiceStudio.exe`.

> Quer um atalho na área de trabalho? Clique com o botão direito em `GLabsVoiceStudio.exe` → *Enviar para* → *Área de trabalho (criar atalho)*.

> **⏳ A primeira inicialização pode levar de 30 a 60 segundos (a tela de splash vai pausar em torno de ~90%) — aguarde, não feche.** O Windows precisa escanear o app e os arquivos de GPU (uma etapa automática de segurança, lenta só na primeira vez). A partir da segunda inicialização, o app abre rapidinho.

### 🍎 macOS Apple Silicon

1. Baixe o **`GLabsVoiceStudio-v1.0.7-arm64.dmg`** na distribuição oficial.
2. Dê dois cliques no arquivo `.dmg` para abrir.
3. Arraste o ícone do **G-Labs Voice Studio** para a pasta **Aplicativos**.
4. Abra **Aplicativos**, **clique com o botão direito** em **G-Labs Voice Studio** → escolha **Abrir**.

> ⚠️ **Primeira inicialização:** o macOS pode mostrar *"App de um desenvolvedor não identificado"*. Clique com o botão direito no app → **Abrir** → clique em **Abrir** na caixa de diálogo. Só precisa fazer isso uma vez.

> 📁 **Arquivos de saída** (áudio, roteiros) são salvos em `~/Documents/G-Labs Voice Studio/output/` por padrão.

> **⏳ A primeira inicialização pode levar de 30 a 60 segundos (a tela de splash vai pausar em torno de ~90%) — aguarde, não feche.** O macOS faz uma verificação de segurança completa na primeira execução. A partir da segunda, o app abre rapidinho.

#### 🍎 Corrigindo *"O app está danificado"* no macOS

Quando você baixa um `.dmg` da internet, o macOS coloca automaticamente uma **flag de quarentena** no arquivo. Se o app não tiver notarização da Apple, o Gatekeeper bloqueia e pode dizer *"O app está danificado e não pode ser aberto"*.

**Método 1: Clique com o botão direito → Abrir** *(recomendado)*

1. Abra **Aplicativos**.
2. **Clique com o botão direito** em *G-Labs Voice Studio* → **Abrir**.
3. Clique em **Abrir** novamente na caixa de diálogo de aviso.

**Método 2: Use o Terminal** (se o método 1 ainda mostrar o erro)

Abra o **Terminal** (Launchpad → Outros → Terminal), cole o comando abaixo e pressione Enter:

```bash
xattr -cr "/Applications/G-Labs Voice Studio.app"
```

Isso limpa todos os atributos estendidos (incluindo a flag de quarentena) do pacote do app. Depois disso, abra o app normalmente. Você só precisa fazer isso **uma vez** por versão baixada.

**Método 3: Ajustes do Sistema → Privacidade e Segurança**

1. Tente abrir o app normalmente (ele será bloqueado).
2. Abra **Ajustes do Sistema** → **Privacidade e Segurança**.
3. Role até o final, encontre *"G-Labs Voice Studio foi bloqueado…"* → clique em **Abrir Mesmo Assim**.
4. Confirme com Touch ID ou senha de administrador.

---

## Começando

### Parte 1 — Primeira inicialização (configuração única)

1. Abra o app — uma tela de boas-vindas oferece 9 idiomas de interface. Escolha o que quiser.
2. **Faça login** — clique no ícone de engrenagem ⚙️ na barra lateral esquerda → aba *Licença* → **"Entrar com Google"**.
3. **Baixe o modelo de IA** — vá para a aba *Configuração do Ambiente* (ou deixe o app te avisar) → clique em **"Baixar modelo"**. Alguns GB; espere terminar.
4. Feche as Configurações.

> 💡 Para mudar o idioma da interface depois: Configurações → Idioma.

### Parte 2 — Clone de Voz 🔊

Clone uma voz a partir de uma gravação de amostra.

1. Abra a aba **Clone de Voz**.
2. Selecione o **idioma de saída** no topo da aba (ex.: vietnamita, inglês…).
3. No campo *Áudio de amostra*, clique em **"Selecionar…"** e escolha um trecho (5–10 segundos, voz clara, com pouco ruído de fundo).
4. **Obrigatório:** digite o *Texto da amostra* — a transcrição exata do áudio de amostra (com pontuação e ortografia corretas).
    > 💡 Clique em **"✨ Sugerir com IA"** e o Whisper transcreve para você — ainda revise antes de gerar.
5. Cole o texto-alvo em *Conteúdo do texto* (ou clique em **"📂 Importar (.txt, .srt)"** para carregar de um `.txt` / `.srt`).
6. Clique em **"📋 Adicionar à tabela"** — o app divide seu texto em frases individuais.
7. (Opcional) Clique em **🔤 Pronúncia** para revisar o dicionário fonético — se o texto contiver caracteres especiais (ex.: `100%`), o app vai te perguntar como lê-los.
8. Clique em **"▶ Iniciar processamento"** → uma caixa de confirmação aparece para verificar a transcrição da amostra → confirme para rodar.
9. Quando terminar, clique em **"💾 Exportar áudio"** (arquivo único mesclado com `.srt` companheiro), ou use o **⬇** numa linha para baixar só aquela fala.

### Parte 3 — Texto para Voz (TTS) 🎛️

Crie uma nova voz a partir de descrições de atributos — sem precisar de amostra.

1. Abra a aba **Texto para Voz**.
2. Selecione o **idioma de saída**.
3. Abra o painel **Design de Voz** e escolha: *Gênero*, *Idade*, *Tom*, *Estilo*, *Sotaque*.
    > 💡 Quer reutilizar uma voz salva da **Biblioteca de Vozes**? Selecione direto no menu — o app pula o aquecimento da primeira linha e começa direto na linha 1.
4. Cole seu texto e clique em **"📋 Adicionar à tabela"**.
5. Clique em **"▶ Iniciar processamento"**.
6. Depois da geração: clique numa linha da tabela que você quer guardar → clique em **"💾 Salvar"** no painel da *Biblioteca de Vozes* para reutilizar depois.
7. Clique em **"💾 Exportar áudio"** para salvar o resultado.

### Parte 4 — Diálogo de Várias Vozes 💬 *(novo)*

Gere áudio de diálogo com vários personagens, uma voz por personagem — perfeito para podcasts, audiodramas e vídeos no estilo entrevista.

1. Abra a aba **Diálogo de Várias Vozes**.
2. Selecione o **idioma de saída**.
3. Clique em **📋 Diálogo de exemplo** (canto superior direito da área de texto) para ver um exemplo funcional — o app cola o exemplo e abre o editor detalhado.
4. Escreva seu roteiro usando esta sintaxe:
    ```
    <Host>: Bem-vindos a todos, hoje temos uma conversa muito especial preparada.
    <Anna>: Olá, estou muito feliz de fazer parte do programa hoje.
    <Ben>: Igualmente, obrigado por nos receber. Qual é o tema?
    ```
    > 💡 O nome do personagem vai dentro de `< >`, seguido por `:` e depois a fala. Os dois pontos são opcionais — `<Anna> Olá pessoal` também funciona. Os nomes não diferenciam maiúsculas de minúsculas.
5. Clique em **"🎭 Analisar diálogo"** — o app divide o roteiro em linhas e mostra a coluna "Personagem".
6. O painel **Atribuição de vozes** abre automaticamente — escolha uma voz da biblioteca para cada personagem.
7. (Opcional — *novo*) Cada linha de personagem tem seu próprio controle **Velocidade** (0,5x → 2x) logo abaixo do seletor de voz. Personagens podem rodar em ritmos independentes no mesmo lote — ex.: apresentador fala devagar, convidado mais rápido.
8. Clique em **"▶ Iniciar processamento"** — cada fala é lida na voz do seu personagem atribuído.
9. Clique em **"💾 Exportar áudio"** para salvar o resultado (um `.srt` correspondente é incluído).

### Parte 5 — Voz para Texto 📝

Transcreva a fala de um arquivo de áudio/vídeo existente.

1. Abra a aba **Voz para Texto**.
2. Clique em **"Selecione um arquivo de áudio ou vídeo..."** e escolha um arquivo de áudio/vídeo (MP3, WAV, M4A, FLAC, MP4, MOV…).
3. Clique em **"▶ Iniciar extração"** — o app analisa o áudio, divide em segmentos de fala e transcreve cada um.
4. Os resultados aparecem numa tabela com tempos por frase. Você pode editá-los direto.
5. Clique em **"💾 Exportar resultado"** para salvar como `.txt` (texto puro) ou `.srt` (com tempos, pronto para legendas).

---

## 💡 Dicas para usuários avançados

### Masterização de áudio *(novo)*
- As três abas de geração (Clone de Voz / Texto para Voz / Diálogo de Várias Vozes) têm uma seção recolhível **Masterização de áudio** no meio do formulário.
- 6 predefinições embutidas:
  - 📻 **Radiodifusão** *(padrão)* — padrão de rádio/podcast, quente e comprimido.
  - 🎬 **Cinema** — reverberação ampla, compressão suave, qualidade de cinema.
  - 🎙️ **Podcast** — microfone próximo, compressão pesada, sem reverberação.
  - 🔇 **Bruto** — saída do modelo como está, sem processamento.
  - ☀️ **Quente** — médios-graves realçados, sensação aconchegante.
  - ✨ **Brilhante** — agudos cristalinos, sensação arejada.
- Mude a predefinição em uma aba → as outras duas sincronizam automaticamente. Para obter exatamente a mesma saída da versão anterior (v1.0.4): escolha **🔇 Bruto** e desmarque **Equalizar volume entre as falas**.

### Liberação automática de memória quando ocioso *(novo)*
- Padrão: se o app fica sem uso por **5 minutos**, o modelo de IA é descarregado automaticamente da VRAM/RAM para liberar recursos do sistema.
- Da próxima vez que você gerar, o modelo recarrega (~30-60s).
- Vá para a aba **Configuração do Ambiente** → **Liberar VRAM automaticamente** para ajustar o tempo (0 = desligado, 1-120 minutos).

### Biblioteca de Vozes e estrela de favorito
- Cada voz da biblioteca tem uma ☆ no começo da linha. Clique nela → vira ★ → essa voz pula para o topo da lista (e fica lá na próxima vez também).
- Clique na ★ de novo para desfavoritar.
- Todas as 30 vozes de fábrica (Achernar, Aoede, Kore, Puck…) também podem ser favoritadas.

### Dicionário fonético
- Quando seu texto contém `%`, `$`, `°C`, `m²`, marcas… clique em **🔤 Pronúncia** antes de gerar.
- Na primeira vez que o app vê um token, ele te pergunta como ler (ex.: `%` → ` por cento`).
- Cada token só precisa ser digitado **uma vez** — o app lembra por idioma de saída. Na próxima, é aplicado automaticamente.
- O mesmo token em idiomas diferentes mantém pronúncias separadas (ex.: vietnamita vs inglês).

### Velocidade de reprodução + exportação
- Depois que o áudio é gerado, a barra abaixo da forma de onda tem um **menu de velocidade** (0,5x → 2x, em passos).
- Mude a velocidade → a prévia atualiza imediatamente no player.
- O arquivo exportado mantém exatamente aquela velocidade e o **tom é preservado** (sem efeito esquilo — usa time-stretching).

### Exportação de SRT
- No painel *Configurações de exportação*, **"Exportar legendas também (.srt)"** vem ligado por padrão.
- Ao exportar como um único arquivo mesclado, o app cria `nome.srt` ao lado de `nome.wav`.
- Os tempos no SRT refletem a duração real de cada linha (após o ajuste de velocidade).

---

## Requisitos de Sistema

|   | Mínimo | Recomendado |
|---|---|---|
| **SO** | Windows 10 (64 bits), macOS 12 Monterey | Windows 11, macOS 13 ou mais novo |
| **RAM** | 8 GB | 16 GB ou mais |
| **VRAM (GPU)** | 4 GB (transfere TTS automaticamente para CPU) | 8 GB+ (NVIDIA RTX 3060 ou superior) |
| **Disco** | 10 GB livres (modelos + cache) | 20 GB+ SSD |
| **GPU** | Opcional — CPU funciona | NVIDIA CUDA · Apple Silicon (Metal) |

> 💡 **Dica:** Em GPUs com ≤ 8 GB de VRAM, o app transfere automaticamente o TTS para a CPU durante a transcrição — sem precisar configurar. Não é obrigatório ter uma GPU dedicada; o pipeline inteiro roda na CPU (só mais devagar).

### Observações por plataforma

**Windows x64**
- **GPU NVIDIA, série RTX 20 ou mais nova** (compute capability ≥ 7.0 — RTX 20/30/40/50, Titan V, Tesla V100…). Placas mais antigas como a série GTX 10 (GTX 1060/1070/1080) **não conseguem rodar os kernels acelerados**; o app detecta isso e cai automaticamente para a CPU.
- Driver NVIDIA com suporte a CUDA 12.8.

**macOS**
- Só **Apple Silicon** (M1/M2/M3/M4…) é suportado — usa a aceleração Metal da Apple. Macs com Intel não são suportados.

> Máquinas sem uma GPU compatível **rodam automaticamente em CPU multi-core** (o app ajusta os contadores de threads do PyTorch / BLAS de acordo com a quantidade de núcleos físicos). Cerca de 5–10× mais lento que a GPU, mas ainda usável para trabalhos curtos de locução.

---

© 2026 Duck Martians AI Labs. Todos os direitos reservados.
