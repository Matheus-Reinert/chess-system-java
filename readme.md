****
#Guia de como utilizar o SonarQube em ambiente local no Windows.

####1º Passo: É necessario instalar o [Java SE 11 ou superior](https://www.oracle.com/br/java/technologies/javase-downloads.html).

####2º Passo: Baixar a última versão do [SonarQube Community](https://www.sonarqube.org/downloads/) e extrair os arquivos para C:/SonarQube 

####3º Passo: Baixar a última versão versão [SonarScanner](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner/) e extrair os aarquivos para C:/SonarScanner.

####4º Passo: Para que nosso projeto possa ser analisado pelo SonarQube precisamos  adicionar um arquivo de configuração na raiz do nosso projeto.

O arquivo deverá chamar: sonar-project.propeties
 A seguinte configuração deverá estar presente no arquivo:

>sonar.projectKey=WebView 
sonar.projectName=WebView 
sonar.projectVersion=1.0 
sonar.sources=. 
sonar.java.binaries=. 
sonar.sourceEncoding=UTF-8

####5º Passo: Você poderá iniciar o SonarQube manualmetne ou então instalar como um serviço:
>Manualmente:
Execute o CMD como administrador.
Navegue até a pasta onde se encontra o executor do SonarQube
Ex: C:\SonarWube\bin\windows-x86-64
Execute o arquivo StartSonar.bat
Neste momento, o site do SonarQube ficará disponível na porta http://localhost:9000/

####7º Você pode iniciar a analise do seu projeto com o SonarScanner:
>Executar a analise:
Execute o CMD como administrador.
Navegue até a pasta do projeto onde está o seu .sln junto com seu arquivo de configuração.
Ex.: cd C:\Projetos\MeuProjeto\scr
No mesmo CMD que navegou até a pasta do projeto, execute o Scanner
Para de o caminho até o arquivo sonar-scanner.bat
Após executar o scanner, o processo de analise do projeto será executado. O resultado de saida irá aparecer no site do SonarQube disponível na porta http://localhost:9000/ 

***

<h3> Qualidade contítua do código: Sonar avalia os riscos do projeto com base na confiabilidade, segurança e manutenção.
-

*Confiabilidade -> Incidência de bugs*
*Segurança -> Incidência de vulnerabilidades*
*Manutenção -> Incidência de code smells*
*% de linhas cobertas com teste unitário*
*% de código duplicado*

