# W11Customizer

Personalize a barra de tarefas e o menu Iniciar do Windows 11 com estilos ajustáveis, dock, clima e wallpapers animados.

[Baixar instalador ou ZIP portátil da preview.14](https://github.com/0Angeli/W11Customizer-Releases/releases/tag/v0.1.0-preview.14)

Este repositório público contém somente downloads e documentação. O código-fonte permanece privado.

> Esta prévia ainda não tem assinatura digital. O código-fonte, executável, instalador e ZIP foram verificados localmente pelo Microsoft Defender, com inteligência `1.461.231.0`, sem detecções nessa varredura. Isso não confirma falso positivo dos alertas anteriores e não garante ausência de bloqueios em outros PCs. Não desative a proteção para executar o programa.

## Instalar (recomendado)

1. Em **Assets**, baixe **W11Customizer-0.1.0-preview.14-setup-win-x64.exe**.
2. Abra o instalador, escolha a pasta e clique em **Instalar**. Não exige administrador. O atalho na área de trabalho é opcional.
3. Abra **W11Customizer** pelo atalho no menu Iniciar.
4. O tema inicial é XP escuro, com dock e oceano no Iniciar. Clique com o botão direito na barra para personalizar. Preferências existentes são preservadas.
5. Opcional: ative **Iniciar com o Windows** nas preferências.

Para atualizar, saia pelo menu da barra e execute o novo instalador na mesma pasta. Para remover, saia e use **Configurações do Windows → Aplicativos → Aplicativos instalados → W11Customizer → Desinstalar**. A desinstalação remove a inicialização automática e preserva suas preferências.

## Usar sem instalar (portátil)

1. Em **Assets**, baixe **W11Customizer-0.1.0-preview.14-win-x64.zip**. Ignore os links **Source code**: eles contêm apenas a documentação deste repositório.
2. Clique com o botão direito no ZIP → **Extrair Tudo** para uma pasta permanente, por exemplo `%LocalAppData%\Programs\W11Customizer-Portable`.
3. Abra **W11Customizer.exe**, mantendo **W11Customizer.exe.config** na mesma pasta. Não execute de dentro do ZIP.

Para atualizar o portátil, saia pelo menu e substitua os arquivos. Para remover, desative a inicialização automática, saia e apague sua pasta. As duas versões salvam preferências em `%AppData%\W11Customizer`.

## Requisitos e recuperação

Windows 11 x64 com Explorer e .NET Framework 4.8, já incluído no Windows 11. Internet é usada pelo clima. Não precisa de Visual Studio, Git ou Python.

O aplicativo e o instalador ainda não têm assinatura digital; não é necessário desativar as proteções do Windows. Cada download tem um arquivo `.sha256` para verificar sua integridade.

Se a barra original não voltar após um travamento, finalize W11Customizer no Gerenciador de Tarefas e execute **Restaurar-taskbar.cmd** na pasta do programa.

## Novidades

- Bibliotecas nativas são carregadas somente do System32 e ferramentas do Windows usam caminhos absolutos.
- Executável com identificação de produto, publicador, versão e nome interno corretos; compiladores verificados pela assinatura de seus fornecedores.
- Importação de configurações com limites de tamanho, rejeição de duplicatas e links e substituição atômica dos arquivos.
- Dados do clima limitados após descompressão; SVGs rejeitam DTDs, entidades externas e estruturas excessivamente grandes ou profundas.
- Fluxo preparado para assinatura digital e verificação de integridade antes da publicação. Esta prévia é disponibilizada sem assinatura por solicitação do responsável.

### Ajustes visuais mantidos

- A ação **Personalizar** usa a logo do projeto e um nome mais curto.
- **Temas** recebe um ícone de personalização da aparência; **Atalhos da bandeja** usa um ícone de vínculo.
- Todos os checks dos menus e submenus da taskbar usam o mesmo cinza claro.
- O item principal **Modo dock** também mostra o check quando o modo está ativado.

### Melhorias anteriores

- Tema inicial XP escuro com cor `#0D0F17`, sem neon na barra nem no clique dos ícones. Configurações existentes são preservadas.
- Menu de contexto reorganizado: **Modo dock** fica acima de **Temas**; o tema azul agora se chama **XP Luna**.
- Realces compartilhados, indicadores proporcionais aos ícones, atalhos da bandeja com escala ajustada e contraste suave sobre os wallpapers do Iniciar.
- **Personalizar → Cores e estilo:** prévia ao vivo, referência visual e botão para desfazer os ajustes. **Temas** permite alternar os perfis salvos, incluindo o wallpaper.
- **Personalizar → Janelas:** regras por aplicativo para manter o dock compacto, expandir quando esse programa estiver maximizado, ocultar automaticamente ou excluir o programa da animação Gênio.
- **Botão direito em uma pasta da bandeja → Explorar conteúdo:** painel com filtro, subpastas e abertura de arquivos, com leitura em segundo plano e limite de 200 itens.
- Busca do Iniciar com ações para copiar caminho, abrir localização e pesquisar dentro da pasta. O indicador de pesquisa e a seleção do teclado acompanham a chegada dos resultados.
- Economia na bateria pausa os wallpapers e reduz a frequência dos efeitos de fundo da barra. Uma cópia da configuração é criada após 30 segundos sem novos ajustes, com restauração em **Preferências**.
- Um processo auxiliar sem interface restaura a barra original após encerramento inesperado do W11Customizer, sem reiniciar o aplicativo automaticamente. Ele não detecta travamentos com o processo ainda aberto. **Preferências → Diagnóstico** permite consultar e exportar informações e erros recentes.

### Correções mantidas

- Corrigido o tamanho final do dock: o recolhimento usa apenas a largura dos elementos e remove o vão artificial entre o widget e o Iniciar.
- A centralização do Iniciar e dos programas é preservada ajustando a posição do dock compacto, sem acrescentar espaços vazios ao conteúdo. O widget continua visível e clicável durante a transição.
- Iniciar e programas permanecem centralizados mesmo com larguras diferentes do clima e da bandeja, mantendo a posição durante a expansão e o recolhimento.
- Separador da bandeja reduzido para 8 px de altura e 2 px de espaço de cada lado.
- Teste de regressão verifica os pixels do widget no início, no meio e no fim das transições, além das posições dos ícones, nos quatro estilos e em quatro escalas.
- Separador discreto entre atalhos e ícones do sistema, com indicadores de janela aberta e em foco.
- Linha de inserção durante o arraste para mostrar onde cada atalho será colocado. O dock mantém sua posição durante a operação.
- Segure arquivos sobre uma pasta por 700 ms para abri-la. Solte dentro da janela ou sobre o ícone após essa espera para copiar. A cópia usa os diálogos do Windows para progresso e conflitos; os originais são preservados. Soltar rapidamente na bandeja continua fixando atalhos.
- Botão direito → **Personalizar atalho** para escolher nome e ícone: pastas nativas, `.ico`, `.png`, `.exe` ou `.lnk`. Alterações ficam salvas entre reinícios.
- Caminhos indisponíveis recebem um aviso discreto. **Localizar novo caminho** permite corrigir o destino preservando a posição, o nome personalizado e o ícone.
- Verificação de arquivos em segundo plano e indicadores integrados aos eventos da barra, sem bloquear a interface com consultas ao disco.
- Pastas especiais fixadas na bandeja preservam os ícones coloridos nativos de Área de Trabalho, Downloads, Documentos, Imagens, Músicas e Vídeos. Também funciona com atalhos `.lnk` e pastas redirecionadas, mantendo o tamanho do botão.
- Clique novamente no atalho da bandeja para minimizar sua janela em foco; outro clique restaura. Janelas abertas em segundo plano são trazidas para frente.
- Arraste os atalhos para reorganizar a bandeja. Soltar após arrastar não abre o arquivo, e o dock permanece visível durante o arraste.
- Arraste pastas e arquivos do Explorador para a bandeja, ao lado do ícone de rede, para criar atalhos.
- Botão direito na barra ou na rede → **Atalhos da bandeja** → **Adicionar pasta** ou **Adicionar arquivos**.
- Botão direito em um atalho permite abrir, mover para a esquerda/direita ou remover. Os arquivos originais permanecem no lugar.
- Os atalhos e sua ordem são salvos entre reinícios e compartilhados entre os quatro estilos. A busca do Iniciar também oferece **Fixar na bandeja** para arquivos e pastas.
- Alterações nos atalhos aguardam o fim da animação do dock antes de atualizar o layout.

## Validação e limites

Compilação x64 e testes isolados de pesquisa, seletor de cores, fechamento de janelas, dock, configurações, ícones, clima, inicialização, wallpapers e integridade dos pacotes. Instalação, atualização e desinstalação verificadas em pasta isolada. Os testes de interface usam renderização por software; a fluidez visual em cada GPU ainda depende de uso real.
