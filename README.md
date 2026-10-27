# W11Customizer

Personalize a barra de tarefas e o menu Iniciar do Windows 11 com estilos ajustáveis, dock, clima e wallpapers animados.

[Baixar instalador ou portátil](https://github.com/0Angeli/W11Customizer-Releases/releases/tag/v0.1.0-preview.4)

Este repositório distribui apenas os pacotes e a documentação. O código-fonte e o histórico de desenvolvimento permanecem privados.

## Instalar (recomendado)

1. Em **Assets**, baixe **W11Customizer-0.1.0-preview.4-setup-win-x64.exe**.
2. Abra o instalador, escolha a pasta e clique em **Instalar**. Não exige administrador. O atalho na área de trabalho é opcional.
3. Abra **W11Customizer** pelo atalho no menu Iniciar.
4. O tema inicial é XP escuro, com dock e oceano no Iniciar. Clique com o botão direito na barra para personalizar. Preferências existentes são preservadas.
5. Opcional: ative **Iniciar com o Windows** nas preferências.

Para atualizar, saia pelo menu da barra e execute o novo instalador na mesma pasta. Para remover, saia e use **Configurações do Windows → Aplicativos → Aplicativos instalados → W11Customizer → Desinstalar**. A desinstalação remove a inicialização automática e preserva suas preferências.

## Usar sem instalar (portátil)

1. Em **Assets**, baixe **W11Customizer-0.1.0-preview.4-win-x64.zip**. Ignore os links **Source code**: eles contêm apenas a documentação deste repositório.
2. Clique com o botão direito no ZIP → **Extrair Tudo** para uma pasta permanente, por exemplo `%LocalAppData%\Programs\W11Customizer-Portable`.
3. Abra **W11Customizer.exe**, mantendo **W11Customizer.exe.config** na mesma pasta. Não execute de dentro do ZIP.

Para atualizar o portátil, saia pelo menu e substitua os arquivos. Para remover, desative a inicialização automática, saia e apague sua pasta. As duas versões salvam preferências em `%AppData%\W11Customizer`.

## Requisitos e recuperação

Windows 11 x64 com Explorer e .NET Framework 4.8, já incluído no Windows 11. Internet é usada pelo clima. Não precisa de Visual Studio, Git ou Python.

O aplicativo e o instalador ainda não têm assinatura digital; não é necessário desativar as proteções do Windows. Cada download tem um arquivo `.sha256` para verificar sua integridade.

Se a barra original não voltar após um travamento, finalize W11Customizer no Gerenciador de Tarefas e execute **Restaurar-taskbar.cmd** na pasta do programa.

## Correções desta versão

- A passagem para o preto no acrílico agora é gradual, sem trocar o efeito nativo ao chegar a `#000000`.
- Cinzas muito escuros e tons escuros coloridos preservam as gradações. Preto absoluto continua opaco para permanecer preto real.
- Mantém a pesquisa ampliada, o seletor com prévia ao vivo, o X centralizado e os ajustes das esperas do dock da prévia anterior.

## Validação e limites

Compilação x64 e testes isolados de pesquisa, seletor de cores, fechamento de janelas, dock, configurações, ícones, clima, inicialização, wallpapers e integridade dos pacotes. Instalação, atualização e desinstalação verificadas em pasta isolada. Os testes de interface usam renderização por software; a fluidez visual em cada GPU ainda depende de uso real.
