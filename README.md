# Bot auxiliar de canal

O Channel Helper Bot é um bot do Telegram que adiciona funcionalidades simples de comentários aos canais. As funções do Channel Helper Bot incluem: criar uma área de comentários em um canal, coletar comentários dos usuários e exibir comentários recentes. O Channel Helper Bot pode fornecer uma plataforma de comentários para o canal, realizar funções sociais leves e ajudar a promover trocas e comunicações diretas entre proprietários e seguidores do canal, e entre seguidores.

## Características

### Gerenciamento simples de comentários

Depois que o proprietário do canal publica uma nova mensagem, ele pode abrir a área de comentários com apenas algumas operações simples. Quando a área de comentários correspondente à mensagem do canal aparece no canal, os seguidores podem fazer comentários.

No modo automático, depois que o proprietário do canal postar uma mensagem, a área de comentários aparecerá automaticamente, sem nenhuma operação necessária.

No modo manual, depois que o proprietário do canal publica uma mensagem, ele só precisa responder à mensagem postada com o comando `/command` para que a área de comentários apareça.

### Processo de revisão conveniente

Cada área de comentários tem dois botões: "Adicionar comentário" e "Mostrar todos os comentários". Clique no botão para pular automaticamente para a página do Channel Helper Bot. Siga as instruções para concluir os comentários e a navegação.

Após clicar em "Adicionar comentário", você entrará no modo de comentário e escreverá o que deseja dizer ao bot para postar um comentário. Para sair do modo de comentário, use o comando `/cancel`.

Após clicar em "Mostrar todos os comentários", o bot exibirá uma área de comentários reversível na página de bate-papo privada, onde os usuários podem visualizar todas as informações de comentários anteriores (compatível com visualização de adesivos, fotos, vídeos, arquivos, etc.) e os administradores podem excluir mensagens e banir usuários aqui.

### Processo de configuração fácil

O processo de configuração é muito simples, e os proprietários dos canais podem facilmente concluir a configuração do Channel Helper Bot em apenas algumas etapas.

1. Adicione o bot como administrador do canal. O bot precisa de permissões suficientes para enviar e editar mensagens.

2. Envie o comando `/register` para o bot no chat privado e siga as instruções do bot para encaminhar uma mensagem do canal para registrar as informações relevantes do canal.

3. Publique uma mensagem e veja! Se a área de comentários for chamada automaticamente, significa que a configuração foi bem-sucedida. (Observação: por padrão, o bot está no modo automático)

4. Se precisar modificar a configuração (modo, número de mensagens recentes, etc.), envie o comando `/option` para o bot e siga as instruções para configurar.

### Inteligente Multiuso

O Channel Helper Bot não se contenta em servir apenas um canal. Qualquer pessoa pode adicionar e usar o Channel Helper Bot por meio da configuração. Ao mesmo tempo, o bot em si é de código aberto e você pode implantá-lo de acordo com suas necessidades. [@jogle_channel_bot](https://t.me/jogle_channel_bot) é a versão mais recente do Bot implantada pelo autor, fique à vontade para usá-la.

## Implantação

Para executar o Channel Helper Bot, você precisa preparar um ambiente Python 3 e instalar as dependências correspondentes usando pip.

### Dependências de instalação

`pip3 instala python-telegram-bot`

### Arquivo de configuração

Renomeie `helper_const.py.sample` para `helper_const.py` e preencha os itens de configuração.

| Item de configuração | Tipo | Significado
|----------------------|---------------|-------------------------------------------------
| BOT_TOKEN | (str) | Token do bot do Telegram
| PROPRIETÁRIO DO BOT | (lista de int) | ID do usuário do proprietário do bot
| INTERVALO_DE_ATUALIZAÇÃO_MIN | (int) | Intervalo mínimo de atualização em segundos
| NOME_DO_MÓDULO | (lista de str) | O nome do módulo habilitado (se não houver nenhum requisito especial, você não precisa alterar isso)
| DATABASE_DIR | (str) | Local de armazenamento do banco de dados
------------------------------------------------------------------------------------------------

### Execute o bot

`python3 helper_main.py`

## Agradecimentos

O Channel Helper Bot usa a API de bot do [python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot).
