Instalando e configurando o JDK no computador windows para desenvolver e executar programas em java.

O JDK (Java Development Kit) é o ambiente necessário para desenvolver aplicativos em Java e já possui uma cópia do JRE. Para executar uma aplicação em um cliente só é necessário o JRE instalado, pois o JRE (Java Runtime Envirorment) é o ambiente de execução do Java.

## Download

Acesse o site da oracle e faça o download da versão do [jdk](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html?ssSourceSiteId=otnpt) e [jre](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html?ssSourceSiteId=otnpt) mais recente. Atualmente estamos na versão 8.

## Instalação JDK e/ou JRE

* Executar o instalador do JDK;
* Aceite os termos de licença;
* Deixe no caminho default definido pelo seu conputador;
* Finish.

## Configurando o JDK

    01 Clique com o botão direito do mouse no ícone "Meu Computador";
    02 Clique em "Propriedades"; 
    03 Escolha a aba "Avançado";
    04 Clique no botão "Variáveis de Ambiente";
    05 Clique no botão novo na opção "Variáveis do Sistema";
    06 Nome da variável --> JAVA_HOME
	07 Valor da variavel (É o caminho onde o JDK foi instalado) --> "C:\Program Files\Java\jdk1.8.0_92";
	08 Clique em OK;
	09 Nome da variável --> CLASSPATH;
	10 Valor da variavel --> ;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\htmlconverter.jar;%JAVA_HOME%\jre\lib;%JAVA_HOME%\jre\lib\rt.jar;
	11 Clique em OK;
	12 Procure a variável chamada PATH em "Variáveis do Sistema" e clique em editar;
	13 Acrescente o valor da pasta bin --> ;%JAVA_HOME%\bin;
	14 Clique em OK até sair de todas as janelas.

## Testando o JDK

	Teste 1: Prompt de comando

		1 Pressione as teclas WINDOWS + R;
		2 Digite CMD e clique em ok;
		3 Digite java -version;
		4 Se estiver tudo configurado corretamente deve ser exibida a seguinte mensagem;
		```txt
		java version "1.8.0_92"
		Java(TM) SE Runtime Environment (build 1.8.0_92-b14)
		Java HotSpot(TM) 64-Bit Server VM (build 25.92-b14, mixed mode)
		```

	Teste 2: Código Java

		01 Abra o bloco de notas e digite o código abaixo;
		```Java
		public class Ola{
			public static void main(String[] args){
				System.out.println("Hello World !");
			}
		}
		```
		02 Salve o arquivo com o nome Ola.java;
		03 Pressione as teclas WINDOWS + R;
		04 Digite CMD e clique em ok;
		05 Navegue até a pasta onde o arquivo foi salvo;
		06 Digite o comando javac Ola.java para compilar o arquivo;
		07 Se funcionar nada será exibido na tela;
		08 Digite java Ola;
		09 Se funcionar será exibida a mensagem "Hello World !" que estava escrita no código criado.
		