# W11Customizer

Personalize a barra de tarefas e o menu Iniciar do Windows 11 com estilos ajustáveis, dock, clima e wallpapers animados.

[Baixar instalador ou portátil](https://github.com/0Angeli/W11Customizer-Releases/releases/tag/v0.1.0-preview.5)

Este repositório distribui apenas os pacotes e a documentação. O código-fonte permanece privado.

## Instalar (recomendado)

1. Em **Assets**, baixe **W11Customizer-0.1.0-preview.5-setup-win-x64.exe**.
2. Abra o instalador, escolha a pasta e clique em **Instalar**. Não exige administrador. O atalho na área de trabalho é opcional.
3. Abra **W11Customizer** pelo atalho no menu Iniciar.
4. O tema inicial é XP escuro, com dock e oceano no Iniciar. Clique com o botão direito na barra para personalizar. Preferências existentes são preservadas.
5. Opcional: ative **Iniciar com o Windows** nas preferências.

Para atualizar, saia pelo menu da barra e execute o novo instalador na mesma pasta. Para remover, saia e use **Configurações do Windows → Aplicativos → Aplicativos instalados → W11Customizer → Desinstalar**. A desinstalação remove a inicialização automática e preserva suas preferências.

## Usar sem instalar (portátil)

1. Em **Assets**, baixe **W11Customizer-0.1.0-preview.5-win-x64.zip**. Ignore os links **Source code**: eles contêm apenas a documentação deste repositório.
2. Clique com o botão direito no ZIP → **Extrair Tudo** para uma pasta permanente, por exemplo `%LocalAppData%\Programs\W11Customizer-Portable`.
3. Abra **W11Customizer.exe**, mantendo **W11Customizer.exe.config** na mesma pasta. Não execute de dentro do ZIP.

Para atualizar o portátil, saia pelo menu e substitua os arquivos. Para remover, desative a inicialização automática, saia e apague sua pasta. As duas versões salvam preferências em `%AppData%\W11Customizer`.

## Requisitos e recuperação

Windows 11 x64 com Explorer e .NET Framework 4.8, já incluído no Windows 11. Internet é usada pelo clima. Não precisa de Visual Studio, Git ou Python.

O aplicativo e o instalador ainda não têm assinatura digital; não é necessário desativar as proteções do Windows. Cada download tem um arquivo `.sha256` para verificar sua integridade.

Se a barra original não voltar após um travamento, finalize W11Customizer no Gerenciador de Tarefas e execute **Restaurar-taskbar.cmd** na pasta do programa.

## Novidades

- Integração com o processador nativo do Windows Search: classificação por relevância, busca de conteúdo indexado e filtros AQS por tipo, data e tamanho.
- Categorias Tudo, Apps, Documentos, Pastas, Fotos, Música, Vídeos, Configurações e Web, com realce suave no hover e seleção preservada.
- Pesquisa web via Bing no navegador, somente após clicar. Atalho para abrir o painel original do Windows (Win+S), com os provedores adicionais disponíveis no sistema e na conta.
- Botão direito em uma pasta encontrada → **Fixar no Iniciar** ou **Fixar na barra de tarefas**. O menu também permite desafixar. Pastas fixadas ficam disponíveis mesmo antes de o catálogo de aplicativos terminar de carregar.
- As consultas continuam em segundo plano, com cancelamento ao trocar o texto ou a categoria. As categorias Apps, Configurações e Web não consultam o índice de arquivos.
- Mantém as correções anteriores de acrílico, seletor de cores e dock. Código-fonte, ferramentas e dados pessoais ficam fora dos downloads.

## Validação e limites

Compilação x64 e testes isolados de pesquisa, seletor de cores, fechamento de janelas, dock, configurações, ícones, clima, inicialização, wallpapers e integridade dos pacotes. Instalação, atualização e desinstalação verificadas em pasta isolada. Os testes de interface usam renderização por software; a fluidez visual em cada GPU ainda depende de uso real.
