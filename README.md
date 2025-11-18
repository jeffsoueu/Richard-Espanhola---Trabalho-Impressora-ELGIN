# Richard-Espanhola---Trabalho-Impressora-ELGIN

📖 Manual de Instruções: O "Controle Remoto" da Impressora 🖨️
Este programa funciona como um controle remoto para a sua impressora fiscal ou não fiscal. Ele permite que o computador envie comandos como "Imprimir Texto", "Abrir Gaveta" ou "Cortar Papel".

Para usar, você só precisa ligar o programa e digitar o número da ação que deseja fazer no menu principal.

1. 📦 Preparação Inicial: Instalando e Abrindo no IntelliJ
Se você baixou um arquivo ZIP, isso significa que todos os arquivos necessários (o código, o arquivo .dll da impressora e as bibliotecas) já estão juntos.

Passo 1: Extrair a Pasta (Descompactar)
Localize o arquivo ZIP que você baixou (o nome deve ser algo como Java-Aluno Graduacao.zip).

Clique com o botão direito do mouse no arquivo ZIP.

Selecione a opção "Extrair Tudo..." ou "Extract All...".

Escolha um local fácil de lembrar, como a sua Área de Trabalho ou a pasta Documentos, e clique em "Extrair". Isso criará uma pasta normal no seu computador (por exemplo, Java-Aluno Graduacao) com todos os arquivos prontos.

Passo 2: Verificar a DLL e o Caminho
Seu programa depende do arquivo da impressora E1_Impressora01.dll estar em um local específico e exato.

Abra a pasta que você acabou de extrair e confirme se o arquivo E1_Impressora01.dll está lá.

⚠️ IMPORTANTE (Ajuste Crítico): O código busca a DLL em um caminho fixo de outra máquina. É OBRIGATÓRIO alterar o código para que ele encontre o arquivo na sua máquina. Se você pular este passo, o programa NÃO VAI FUNCIONAR e dará erro.

Como Pegar e Colar o Novo Caminho (Passo a Passo Mais Claro)
Encontre o Novo Caminho:

Vá até a pasta no seu computador onde você extraiu o arquivo E1_Impressora01.dll.

Clique na barra de endereço (aquela barra no topo da janela do Windows Explorer que mostra o caminho, como Este Computador > Documentos > MinhaPasta).

Clique com o botão direito e selecione "Copiar Endereço como Texto". Isso copiará o caminho completo (ex: C:\Users\SeuNome\Downloads\MinhaPasta).

Edite o Código no IntelliJ:

No IntelliJ, abra o arquivo Main.java.

Procure a linha que contém o caminho antigo da DLL: "C:\\Users\\eli_nascimento\\Downloads\\Java-Aluno Graduacao\\Java-Aluno Graduacao\\E1_Impressora01.dll"

Você precisa substituir o caminho entre as aspas ("...") pelo caminho que você acabou de copiar, mas com uma regra extra do Java:

A Regra da Barra Dupla (\\): O Java exige que você use duas barras invertidas (\\) para cada uma que o seu Windows usa (\).

Seu caminho copiado: C:\Users\SeuNome\MinhaPasta\E1_Impressora01.dll

Como deve ficar no código: C:\\Users\\SeuNome\\MinhaPasta\\E1_Impressora01.dll

Finalize: Cole o novo caminho ajustado no lugar do antigo. Salve o arquivo (File > Save All) antes de executar o programa.

2. 💻 Abrindo e Executando o Projeto no IntelliJ
Com os arquivos prontos, vamos usar o IntelliJ IDEA para abrir e executar o projeto.

Passo 3: Abrir o Projeto no IntelliJ
Abra o programa IntelliJ IDEA.

Na tela inicial, clique em "Open" (Abrir).

Navegue até a pasta que você extraiu no Passo 1 (ex: Java-Aluno Graduacao).

Clique na pasta e depois no botão "Open" (Abrir).

O IntelliJ pode perguntar se você confia no projeto. Clique em "Trust Project" (Confiar no Projeto).

Passo 4: Executar o Programa Principal (Main) ▶️
O arquivo que faz o programa funcionar é o Main.java.

No lado esquerdo do IntelliJ, encontre a pasta src e clique duas vezes no arquivo Main.java para abri-lo.

Procure a pequena seta verde de "Play" ao lado da linha que diz public static void main(String[] args) {.

Clique nessa seta verde e selecione "Run 'Main'" (Executar 'Main').

O menu aparecerá na parte de baixo da tela, na aba "Run" (Executar), e o programa começará a rodar.

3. 🎯 Usando o Menu: Conexão e Comandos
Passo 1: Configurar a Impressora (Opção 1) ⚙️
Você informa ao programa como ele deve encontrar a impressora.

Digite 1 e aperte Enter.

O programa fará 4 perguntas: Tipo da conexão, Modelo, Conexão e Parâmetro. Digite as respostas corretas do seu equipamento. Se não souber, peça ajuda ao técnico.

Passo 2: Abrir a Conexão (Opção 2) ✅
Você liga a comunicação com a impressora.

Digite 2 e aperte Enter.

Se as informações estiverem certas e a impressora ligada, a mensagem "Conexão estabelecida" vai aparecer.

Atenção ao Erro: Se aparecer o erro -99999, verifique imediatamente se a impressora está ligada e conectada corretamente ao computador.

Pronto! A conexão está aberta e você pode enviar os comandos.

Comandos de Ação (Opções 3 a 10)
Com a conexão aberta, você pode usar qualquer uma dessas ações:

Opção 3 (Impressão Texto): Imprime um texto de teste, avança o papel e corta o cupom.

Opção 4 (Impressão QRCode): Imprime um Código QR de teste e corta o papel.

Opção 5 (Impressão Código de Barras): Imprime um Código de Barras de teste e corta o papel.

Opção 6 (Impressão XML SAT): Imprime um Cupom Fiscal Eletrônico. Busca o arquivo XMLSAT.xml no caminho fixo.

Opção 7 (Impressão XML Cancelamento SAT): Imprime o comprovante de cancelamento. Busca o arquivo CANC_SAT.xml no caminho fixo.

Opção 8 (Abrir Gaveta Elgin): Abre a gaveta de dinheiro (método Elgin).

Opção 9 (Abrir Gaveta): Abre a gaveta de dinheiro (método genérico).

Opção 10 (Sinal Sonoro): Faz a impressora emitir bipes.

4. 🛑 Desligar e Sair
Passo 3: Fechar a Conexão e Sair (Opção 0)
Quando terminar de usar:

Digite 0 e aperte Enter.

O programa vai fechar a comunicação ("Conexão encerrada") e finalizar.

Regra de Ouro: Sempre use a Opção 0 para fechar. Isso libera a impressora para ser usada por outros programas.
