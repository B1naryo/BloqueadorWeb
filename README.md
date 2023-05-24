# BloqueadorWeb

O código acima é uma implementação de um programa em C# usando o Windows Forms que permite bloquear e desbloquear sites no sistema operacional Windows. 
Aqui está uma descrição das principais partes do código:

O código está contido no namespace "Bloquear_sites" e a classe principal é "Form1", que herda da classe "Form" do Windows Forms.

O formulário (Form1) contém dois campos de entrada de texto (textBox1 e textBox2), onde o usuário pode inserir o URL do site a ser bloqueado ou desbloqueado, e dois botões (button1 e button2) para executar as ações correspondentes.

Quando o botão "Bloquear" (button1) é clicado, o URL inserido no textBox1 é obtido e verificado para garantir que não esteja vazio. Em seguida, o código adiciona três versões do site ao arquivo "hosts" do sistema operacional, redirecionando-os para o endereço IP "127.0.0.1". Em seguida, ele realiza a limpeza do cache DNS do sistema operacional, bem como dos navegadores Google Chrome e Firefox.

Se ocorrer algum erro durante o processo de bloqueio, uma mensagem de erro é exibida ao usuário.

Quando o botão "Desbloquear" (button2) é clicado, o URL inserido no textBox2 é obtido e verificado para garantir que não esteja vazio. Em seguida, o código lê todas as linhas do arquivo "hosts", cria uma nova lista de linhas sem as entradas do site a ser desbloqueado e escreve as linhas atualizadas de volta no arquivo. Em seguida, realiza a limpeza do cache DNS do sistema operacional, do Google Chrome e do Firefox.

Se ocorrer algum erro durante o processo de desbloqueio, uma mensagem de erro é exibida ao usuário.

O código também contém alguns métodos auxiliares, como FlushDNS(), ClearChromeDNS() e ClearFirefoxDNS(), que são responsáveis por executar comandos para limpar o cache DNS do sistema operacional, do Google Chrome e do Firefox, respectivamente.

No geral, o código oferece uma funcionalidade básica para bloquear e desbloquear sites no sistema operacional Windows, manipulando o arquivo "hosts" e executando comandos para limpar o cache DNS.
