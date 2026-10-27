# W11Customizer

Personalize a barra de tarefas e o menu Iniciar do Windows 11 com estilos ajustáveis, dock, clima e wallpapers animados.

[Baixar a versão mais recente](https://github.com/0Angeli/W11Customizer-Releases/releases/tag/v0.1.0-preview.2)

Este repositório distribui apenas os instaladores, pacotes portáteis e documentação. O código-fonte permanece privado. Os arquivos automáticos **Source code** contêm apenas esta documentação.

## Instalar (recomendado)

1. Em **Assets**, baixe **W11Customizer-0.1.0-preview.2-setup-win-x64.exe**.
2. Abra o instalador, escolha a pasta e clique em **Instalar**. Não exige administrador. O atalho na área de trabalho é opcional.
3. Abra **W11Customizer** pelo atalho no menu Iniciar.
4. O tema inicial é XP escuro, com dock e oceano no Iniciar. Clique com o botão direito na barra para personalizar. Preferências existentes são preservadas.
5. Opcional: ative **Iniciar com o Windows** nas preferências.

Para atualizar, saia pelo menu da barra e execute o novo instalador na mesma pasta. Para remover, saia e use **Configurações do Windows → Aplicativos → Aplicativos instalados → W11Customizer → Desinstalar**. A desinstalação remove a inicialização automática e preserva suas preferências.

## Usar sem instalar (portátil)

1. Em **Assets**, baixe **W11Customizer-0.1.0-preview.2-win-x64.zip**. Os links **Source code** são para desenvolvedores.
2. Clique com o botão direito no ZIP → **Extrair Tudo** para uma pasta permanente, por exemplo `%LocalAppData%\Programs\W11Customizer-Portable`.
3. Abra **W11Customizer.exe**, mantendo **W11Customizer.exe.config** na mesma pasta. Não execute de dentro do ZIP.

Para atualizar o portátil, saia pelo menu e substitua os arquivos. Para remover, desative a inicialização automática, saia e apague sua pasta. As duas versões salvam preferências em `%AppData%\W11Customizer`.

## Requisitos e recuperação

Windows 11 x64 com Explorer e .NET Framework 4.8, já incluído no Windows 11. Internet é usada pelo clima. Não precisa de Visual Studio, Git ou Python.

O aplicativo e o instalador ainda não têm assinatura digital; não é necessário desativar as proteções do Windows. Cada download tem um arquivo `.sha256` para verificar sua integridade.

Se a barra original não voltar após um travamento, finalize W11Customizer no Gerenciador de Tarefas e execute **Restaurar-taskbar.cmd** na pasta do programa.

## Mudanças

- Perfil padrão incorporado, sem caminhos, localização ou programas fixados pessoais.
- Wallpapers de oceano e floresta, com correções de layout e limpeza de animações ao fechar o Iniciar.
- Correções na preparação e nas transições do dock, nos ícones e no posicionamento de janelas em tela cheia.
- Reinício com transferência entre instâncias e tratamento de falhas de inicialização.
- Menos alocações na leitura de configurações e efeitos; gravação atômica das configurações e logs limitados.
- Atalhos alterados ou recriados atualizam o executável associado; caminhos inválidos recebem um nome seguro.
- Downloads sem código-fonte, testes, ferramentas, capturas, logs ou configurações pessoais. Diagnósticos de captura da interface ficam fora do executável distribuído.

## Validação e limites

Compilação x64 e 27 verificações: configurações, ícones, dock, clima, inicialização, wallpapers, integridade do ZIP e instalação/atualização/desinstalação em pasta isolada, sem iniciar a barra. Os testes de interface usam renderização por software. Esta prévia não equivale a validação visual em todas as versões do Windows, escalas ou GPUs.
