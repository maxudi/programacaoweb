# programacaoweb

Instalar Tomcat no Windows

Tutorial Tomcat - Instalação de requisitos
Acesse o site java e baixe a versão mais recente do Java JDK.
Em nosso exemplo, baixamos o arquivo chamado: jdk-19

Inicie a instalação do Java JDK.

Clique no botão Next.

Aguarde a finalização da instalação Java JDK.

Em nosso exemplo, o software Java JDK foi instalado no seguinte diretório.
C:\Program Files\Java\jdk-19

Como administrador,inicie um novo prompt de linha de comando POWERSHELL.

Crie uma variável de ambiente de sistema chamada JAVA_HOME.

[Environment]::SetEnvironmentVariable("JAVA_HOME", "C:\Program Files\Java\jdk-14.0.1", "Machine")
Altere o comando acima para refletir o caminho de instalação do JDK.
Agora, precisamos editar a variável ambiente PATH.
Inclua o diretório do Java SDK chamado BIN na variável de ambiente PATH.
Copy to Clipboard
$OLDPATH = [System.Environment]::GetEnvironmentVariable('PATH','machine')
$JAVAPATH = [System.Environment]::GetEnvironmentVariable('JAVA_HOME','machine')
$NEWPATH = "$OLDPATH;$JAVAPATH\bin"
[Environment]::SetEnvironmentVariable("PATH", "$NEWPATH", "Machine")
Reinicie o computador.
Parabéns! Você terminou a instalação do Java JDK no Windows.
Tutorial Tomcat - Testando a instalação java SDK
Inicie um novo prompt de linha de comando DOS.

Verifique a existência da variável JAVA_HOME.

echo %JAVA_HOME%

Aqui está a saída de comando.
C:\Program Files\Java\jdk-14.0.1
Teste a aplicação Java usando a variável chamada JAVA_HOME.
Copy to Clipboard
"%JAVA_HOME%"\bin\java -version
Aqui está a saída de comando.
java version "14.0.1" 2020-04-14
Java(TM) SE Runtime Environment (build 14.0.1+7)
Java HotSpot(TM) 64-Bit Server VM (build 14.0.1+7, mixed mode, sharing)
Verifique se a variável de ambiente PATH inclui o diretório Java SDK chamado BIN.
echo %PATH%
Aqui está a saída de comando.
C:\Windows\system32;C:\Windows;C:\Windows\System32\Wbem;C:\Windows\System32\WindowsPowerShell\v1.0\;C:\Program Files\Amazon\cfn-bootstrap\;C:\Program Files\PowerShell\7\;C:\Program Files\Zabbix Agent\;C:\Program Files\Java\jdk-14.0.1\bin
Teste a aplicação Java sem usar a variável ambiente.
java -version
Aqui está a saída de comando.
java version "14.0.1" 2020-04-14
Java(TM) SE Runtime Environment (build 14.0.1+7)
Java HotSpot(TM) 64-Bit Server VM (build 14.0.1+7, mixed mode, sharing)
Parabéns! Você testou a instalação Java JDK no Windows.
Tutorial Windows - Instalação do Tomcat
Acesse o site apache Tomcat e baixe a versão mais recente do Tomcat.
Em nosso exemplo, baixamos o arquivo chamado: Apache-tomcat-9.0.37.exe

Inicie a instalação do Tomcat.

Selecione a opção Hostmanager e clique no botão Seguir.

Defina o nome de usuário e senha do administrador Tomcat.
Opcionalmente, você pode alterar a porta TCP.

Localize o caminho de instalação do Java JDK e clique no botão Next.

Em nosso exemplo, o instalador Tomcat detectou automaticamente o diretório de instalação do Java SDK.
Verifique o caminho de instalação do Tomcat e clique no botão Seguir.

Em nosso exemplo, o software Tomcat foi instalado no seguinte diretório.
C:\Program Files\Apache Software Foundation\Tomcat 9.0
Clique no botão Instalar e aguarde a finalização da instalação do Tomcat.
Selecione a opção para iniciar o serviço Tomcat e clique no botão Finalizar.
Abra seu navegador e insira o endereço IP do servidor Tomcat mais :8080.
Em nosso exemplo, a seguinte URL foi inserida no Navegador:
• http://172.31.7.220:8080
A página do Tomcat deve ser apresentada.

Parabéns! Você terminou a instalação do Tomcat no Windows.
Tutorial - Acessando o aplicativo Tomcat Manager
No servidor Tomcat, abra seu navegador e digite a seguinte URL:
• http://127.0.0.1:8080/host-manager
Digite o nome de usuário e senha do gerenciador criados durante a instalação do Tomcat.
Após um login bem-sucedido, o painel do host manager será apresentado.

Parabéns! Você pode acessar o servidor Tomcat
