<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Descrição do Projeto</title>
</head>
<body>
    <h1>Descrição do Projeto</h1>
    <p>Este projeto implementa um servidor e um cliente de eco UDP simples em Java. O servidor recebe mensagens de clientes e responde com as mesmas mensagens. O cliente envia mensagens para o servidor e exibe as respostas recebidas.</p>
    <h2>Estrutura do Projeto</h2>
    <h3>Servidor de Eco UDP</h3>
    <ul>
        <li><code>UDPEchoServer</code>: Classe principal do servidor de eco UDP. Ela inicializa o servidor, recebe mensagens de clientes e responde com as mesmas mensagens ou com uma mensagem de erro se o tamanho da mensagem for maior que o buffer permitido.</li>
        <li><code>UDPEchoServerException</code>: Classe para tratar exceções específicas do servidor de eco UDP.</li>
        <li><code>MainServer</code>: Classe que contém o método <code>main</code> para iniciar o servidor com a porta e o tamanho do buffer definidos.</li>
    </ul>
    <h3>Cliente UDP</h3>
    <ul>
        <li><code>UDPClient</code>: Classe principal do cliente UDP. Ele permite que o usuário envie mensagens para o servidor e exibe as respostas recebidas. O cliente continua a operar até que o usuário envie uma mensagem específica para sair (<code>"q"</code>).</li>
    </ul>
    <h2>Como Executar</h2>
    <h3>Servidor</h3>
    <ol>
        <li>Compile as classes do servidor:
            <pre><code>javac br/edu/ifsuldeminas/sd/sockets/server/*.java</code></pre>
        </li>
        <li>Inicie o servidor:
            <pre><code>java br.edu.ifsuldeminas.sd.sockets.server.MainServer</code></pre>
        </li>
    </ol>
    <h3>Cliente</h3>
    <ol>
        <li>Compile as classes do cliente:
            <pre><code>javac br/edu/ifsuldeminas/sd/sockets/client/*.java</code></pre>
        </li>
        <li>Inicie o cliente:
            <pre><code>java br.edu.ifsuldeminas.sd.sockets.client.UDPClient</code></pre>
        </li>
        <li>Siga as instruções no terminal para enviar mensagens ao servidor e receber respostas.</li>
    </ol>
    <h2>Detalhes Técnicos</h2>
    <ul>
        <li>O servidor escuta na porta 3000 e utiliza um buffer de 200 bytes para as mensagens.</li>
        <li>O cliente se conecta ao servidor na mesma porta e buffer, e tem um timeout de 50 segundos para receber respostas do servidor.</li>
        <li>O servidor pode ser parado manualmente e reiniciado, tratando exceções específicas para garantir robustez.</li>
    </ul>
</body>
</html>
