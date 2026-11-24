# RUFood

## Requisitos

- Java 21 (JDK)
- Maven

### Linux (Ubuntu/Debian)

```bash
sudo apt install openjdk-21-jdk maven
sudo update-alternatives --config java   # escolha a versão 21
```

### Windows

1. Instale o JDK 21: https://adoptium.net
2. Instale o Maven: https://maven.apache.org/download.cgi (extraia e adicione a pasta `bin` ao `PATH`)
3. Configure a variável de ambiente `JAVA_HOME` apontando para a pasta do JDK.

### Conferir a instalação

```bash
java -version   # deve mostrar 21
mvn -version    # a linha "Java version" deve mostrar 21
```

## Rodando o projeto

```bash
git clone git@github.com:yannidilly/rufood.git
mvn compile
java -cp target/classes com.rufood.Main
```

Se aparecer `Hello world!`, o ambiente está pronto.

No VSCode, instale o **Extension Pack for Java** e clique em **Run** em cima do método `main`.

## Sequência de desenvolvimento

Os cards estão no projeto **RUFood – Backlog** (aba Projects do GitHub). Cada issue tem critérios de aceite. Siga esta ordem, porque cada etapa depende da anterior.

1. **Setup** (`SET-01` a `SET-04`): repositório, projeto Maven, pacotes, cabeçalho com nome e matrícula, JUnit.
2. **Base do domínio** (`DOM-01` a `DOM-04`, `DOM-09`, `DOM-10`, `PER-01`): diagrama de classes, hierarquia de usuários, endereço e frete, cardápio, exceções, validadores e interface de persistência.
3. **Núcleo** (`DOM-05` a `DOM-08`, `PER-02`, `CON-01`, `CON-02`): pedido, situações do pedido, cupons, avaliação, persistência de usuários e cardápio, cadastro e login.
4. **Funcionalidades por perfil** (podem andar em paralelo, um perfil por dupla):
   - Restaurante: `REST-01` a `REST-07`
   - Cliente: `CLI-01` a `CLI-09`
   - Motoboy: `MOT-01` a `MOT-06`
   - Contas e persistência restantes: `CON-03`, `CON-04`, `PER-03`, `PER-04`
5. **Interface gráfica** (`GUI-01` e `GUI-02` começam junto com a etapa 3; as demais telas vêm junto com cada perfil): `GUI-03` a `GUI-06`.
6. **Fechamento** (`QUA-01` a `QUA-07`): testes, dados de exemplo, Javadoc, PDF, build em Linux e Windows, zip, apresentação e entrevista.

### Regras do grupo

- Uma issue por branch; abra um PR e peça revisão de outro membro antes de dar merge.
- Use `Closes #N` no commit ou PR para fechar o card.
- Todo membro precisa fazer commits (conta na nota) e entender todo o código (a entrevista é individual).
- O código precisa compilar com `mvn compile` em Linux e Windows. Se não compilar, a nota é zero.
