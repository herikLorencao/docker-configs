# Configuração do Sonarqube

## Configuração da máquina

Rode os seguintes comandos com usuário **root**:

```bash
sysctl -w vm.max_map_count=262144
sysctl -w fs.file-max=65536
ulimit -n 65536
ulimit -u 4096
```

## Configuração no Java (Maven)

Adicione a seguinte configuração no arquivo **pom.xml**:

```xml
<build>
	<plugins>
        <plugin>
			<groupId>org.sonarsource.scanner.maven</groupId>
			<artifactId>sonar-maven-plugin</artifactId>
			<version>3.7.0.1746</version>
		</plugin>
    </plugins>
</build>
```