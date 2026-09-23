# 📱 Exercícios de Flutter — UNIP

Material de estudo contendo as questões e respostas sobre **Flutter, Dart e desenvolvimento mobile**.

---

## 1. O que é Flutter, Dart, Widgets e qual a diferença para Android?

### Flutter

**Flutter** é um framework de desenvolvimento de interfaces e aplicativos multiplataforma criado pelo Google. Permite desenvolver para Android, iOS, Web e Desktop utilizando principalmente uma única base de código.

### Dart

**Dart** é a linguagem de programação utilizada pelo Flutter.

### Widgets

**Widgets** são os componentes fundamentais da interface do Flutter. Textos, botões, imagens, telas, menus e estruturas de layout são representados por widgets.

### Android

**Android** é um sistema operacional/plataforma móvel. O desenvolvimento Android nativo normalmente utiliza Kotlin/Java e as APIs próprias do Android.

O Flutter é um framework multiplataforma que pode gerar aplicativos para Android e outras plataformas.

---

## 2. O que são Built-in Widgets? Cite exemplos.

**Built-in Widgets** são widgets que já vêm disponíveis no Flutter e podem ser utilizados na construção das interfaces, sem a necessidade de criá-los do zero.

### Exemplos

| Widget | Função |
|---|---|
| `Text` | Exibe textos |
| `Image` | Exibe imagens |
| `Container` | Organiza e estiliza elementos |
| `Row` | Organiza widgets horizontalmente |
| `Column` | Organiza widgets verticalmente |
| `Center` | Centraliza um widget |
| `Scaffold` | Estrutura básica de uma tela |
| `AppBar` | Barra superior da aplicação |
| `ElevatedButton` | Botão |
| `Icon` | Exibe ícones |

O Flutter utiliza a **composição de widgets**, ou seja, widgets podem conter outros widgets formando uma árvore.

---

## 3. O que é o método `build()`?

O método `build()` é responsável por **descrever e construir a interface visual de um widget**.

Ele retorna um widget que representa aquela parte da interface.

### Exemplo

```dart
class MinhaTela extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Text('Olá Flutter!');
  }
}

4. O que é Container no Flutter?

Container é um widget utilizado para organizar, dimensionar e estilizar outros widgets.

Pode controlar:

Largura e altura;
Margem (margin);
Espaçamento interno (padding);
Cor;
Bordas;
Alinhamento;
Decoração.

Exemplo:

Container(
  width: 200,
  height: 100,
  color: Colors.blue,
  child: Text('Olá'),
)

O Container cria uma área de 200 × 100 pixels, com fundo azul e contendo um texto.

5. Qual a diferença entre aplicações nativas e híbridas? Dê exemplos.
Aplicação nativa

É desenvolvida especificamente para uma plataforma utilizando suas tecnologias próprias.

Exemplos
Android → Kotlin/Java
iOS → Swift/Objective-C

Vantagem: acesso direto aos recursos da plataforma e integração muito próxima ao sistema.

Aplicação híbrida/multiplataforma

Utiliza uma tecnologia que permite compartilhar grande parte do código entre diferentes plataformas.

Exemplos
Flutter
.NET MAUI
React Native

Vantagem: maior reutilização de código para Android e iOS.

6. Quais são os principais padrões de arquitetura para aplicativos móveis?

Padrões de arquitetura organizam o código e separam responsabilidades.

MVC

Model – View – Controller

Model → dados e regras.
View → interface.
Controller → coordena as ações.
MVP

Model – View – Presenter

O Presenter concentra parte da lógica que conecta a View aos dados.

MVVM

Model – View – ViewModel

O ViewModel mantém a lógica e o estado necessários para a interface.

Clean Architecture

Divide a aplicação em camadas, separando regras de negócio, dados e apresentação.

No Flutter, também são comuns soluções baseadas em:

Provider
Riverpod
BLoC
Cubit

Essas soluções podem ser utilizadas principalmente para gerenciamento de estado.

7. O que são Material Design e Cupertino no Flutter?

São conjuntos de widgets e padrões visuais utilizados no Flutter.

Material Design

Segue as diretrizes visuais do Google/Android.

Exemplos:

MaterialApp
Scaffold
AppBar
ElevatedButton
FloatingActionButton

Cupertino

Fornece widgets com aparência e comportamento semelhantes aos utilizados no ecossistema Apple/iOS.

Exemplos:

CupertinoApp
CupertinoButton
CupertinoNavigationBar
CupertinoSwitch

Assim, o Flutter permite criar interfaces seguindo padrões de Android/Material ou iOS/Cupertino.

8. O que é .NET MAUI? Compare com Flutter e Android.

.NET MAUI (Multi-platform App UI) é um framework da Microsoft para desenvolvimento de aplicações multiplataforma utilizando principalmente C# e .NET.

| Tecnologia | Linguagem principal | Característica |
| :--- | :--- | :--- |
| Flutter | Dart | Multiplataforma |
| .NET MAUI | C# / .NET | Multiplataforma |
| Android nativo | Kotlin / Java | Específico para Android |

O Flutter utiliza seu próprio sistema de widgets para construir a interface, enquanto o .NET MAUI integra-se ao ecossistema .NET e às plataformas nativas.

O desenvolvimento Android nativo é específico para Android e possui acesso direto às APIs do sistema.

9. Qual a diferença entre Hot Reload e Hot Restart?
Hot Reload

Aplica alterações no código sem reiniciar completamente o aplicativo, preservando, em geral, o estado atual da aplicação.

Por exemplo, você pode alterar a cor de um botão e executar o Hot Reload. A alteração aparece rapidamente sem precisar começar novamente o fluxo da aplicação.

Hot Restart

Reinicia a execução da aplicação Flutter e perde o estado atual.

Resumo
Recurso	Hot Reload	Hot Restart
Atualiza o código	
Reinicia a aplicação	
Mantém o estado	Geralmente sim	

Hot Reload → mantém o estado.

Hot Restart → reinicia e perde o estado.

10. Explique o código

O código apresentado é aproximadamente:

import 'package:flutter/material.dart';

void main() => runApp(
  MaterialApp(
    title: 'WhatsApp Clone',
    home: Scaffold(
      body: FlutterLogo(
        size: double.infinity,
      ),
    ),
  ),
);

Explicação
import 'package:flutter/material.dart';

Importa os widgets e recursos do Material Design do Flutter.

void main()

É a função principal do programa. A execução começa nela.

runApp()

Inicializa o aplicativo Flutter e coloca o widget informado na árvore de widgets.

MaterialApp

É o widget responsável pela configuração básica da aplicação utilizando Material Design.

title

Define o título da aplicação.

home

Define a tela inicial.

Scaffold

Fornece a estrutura básica de uma tela, como área de conteúdo, AppBar, FloatingActionButton etc.

body

Representa o conteúdo principal do Scaffold.

FlutterLogo

Exibe o logotipo do Flutter.

size: double.infinity

Solicita que o widget utilize o máximo de espaço disponível dentro das restrições recebidas.

11. O que é e qual a diferença entre Provider e Riverpod?

Ambos são soluções utilizadas para gerenciamento de estado e disponibilização de dependências em aplicações Flutter.

Provider

É uma solução bastante conhecida no ecossistema Flutter e utiliza principalmente a árvore de widgets e BuildContext para disponibilizar e consumir estados.

Exemplo conceitual

ChangeNotifierProvider(
  create: (_) => MeuEstado(),
  child: MinhaTela(),
)

Riverpod

É uma solução baseada no conceito de providers, permitindo organizar e acessar estados de forma mais independente da árvore de widgets.

Exemplo
final contadorProvider = StateProvider<int>((ref) => 0);
Resumo

Provider: gerenciamento de estado baseado fortemente na árvore de widgets e no BuildContext.

Riverpod: abordagem baseada em providers, com maior independência da árvore de widgets.

12. Explique a Widgets Tree apresentada

A árvore apresentada é aproximadamente:

MyApp

MyApp
  │
  └── MaterialApp
        │
        └── MyHomePage
              │
              └── Scaffold
                    ├── FloatingActionButton
                    │      └── Icon
                    │
                    ├── AppBar
                    │      └── Text
                    │
                    └── Center
                           │
                           └── Column
                                ├── Text
                                └── Text

Ela representa a hierarquia dos widgets utilizados para construir a interface.

O widget no topo contém widgets filhos, que por sua vez podem conter outros widgets.

Por exemplo, o Scaffold possui três componentes principais mostrados na imagem:

AppBar
Center
FloatingActionButton

O Center contém uma Column, que contém dois widgets Text.

Essa estrutura é chamada de Widget Tree (árvore de widgets).

13. Qual o objetivo de um emulador?

Um emulador simula um dispositivo ou sistema operacional em um computador.

No desenvolvimento Flutter, por exemplo, podemos utilizar um emulador Android para:

Executar o aplicativo;
Testar telas;
Simular diferentes dispositivos;
Testar diferentes resoluções;
Verificar comportamentos sem possuir fisicamente aquele dispositivo.
Exemplo

Android Emulator

14. O que são main.dart e runApp()?
main.dart

É normalmente o arquivo de entrada principal de um projeto Flutter.

Nele geralmente encontramos:

void main() {
  runApp(MyApp());
}

runApp()

É responsável por iniciar a aplicação Flutter e inserir o widget raiz na árvore de widgets.

Exemplo
void main() {
  runApp(MyApp());
}

Nesse caso, MyApp é o widget raiz da aplicação.

15. Stateless e Stateful: o que são e qual a diferença?
StatelessWidget

É um widget cujo estado não muda durante sua execução.

Exemplo
class MeuTexto extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Text('Olá');
  }
}

É adequado para componentes que dependem apenas dos dados recebidos.

StatefulWidget

É utilizado quando o widget precisa possuir um estado que pode mudar durante a execução.

Um exemplo clássico é um contador.

setState(() {
  contador++;
});

Quando setState() é chamado, o Flutter reconstrói a parte necessária da interface.

Resumo
StatelessWidget → sem estado interno mutável.
StatefulWidget → possui estado que pode ser alterado.
16. O que é Scaffold e quais são seus componentes?

Scaffold fornece a estrutura básica de uma tela Material Design.

Entre seus principais componentes/propriedades estão:

Scaffold
 ├── appBar
 ├── body
 ├── floatingActionButton
 ├── drawer
 ├── endDrawer
 ├── bottomNavigationBar
 └── bottomSheet
Exemplo
Scaffold(
  appBar: AppBar(
    title: Text('Minha aplicação'),
  ),
  body: Center(
    child: Text('Olá!'),
  ),
  floatingActionButton: FloatingActionButton(
    onPressed: () {},
    child: Icon(Icons.add),
  ),
)
17. Explique cada componente da interface

A imagem apresenta uma estrutura semelhante a:

MaterialApp
    │
    └── Scaffold
          ├── AppBar
          │     └── Text
          │
          ├── body
          │     └── Text
          │
          └── Button
MaterialApp

É o widget raiz que configura a aplicação utilizando Material Design.

AppBar

É a barra superior da aplicação.

Text

Exibe textos na interface.

Scaffold

Fornece a estrutura principal da tela.

Button

É utilizado para permitir uma ação do usuário, como clicar, enviar ou confirmar algo.

18. Escolha um projeto e reproduza-o

Uma opção simples para realizar o trabalho é criar um aplicativo de lista de tarefas (To-Do List).

Estrutura possível
MyApp
 └── MaterialApp
      └── TodoPage
           └── Scaffold
                ├── AppBar
                │    └── Text("Minhas tarefas")
                │
                ├── Body
                │    └── ListView
                │         ├── ListTile
                │         ├── ListTile
                │         └── ListTile
                │
                └── FloatingActionButton
                     └── Icon(Icons.add)
Funcionalidades

O aplicativo pode permitir:

Adicionar uma tarefa;
Visualizar tarefas;
Marcar uma tarefa como concluída;
Excluir tarefas.
19. Widgets Tree do projeto anterior

Para o aplicativo de tarefas sugerido na questão 18, o diagrama poderia ser:

MyApp
│
└── MaterialApp
    │
    └── TodoPage
        │
        └── Scaffold
            │
            ├── AppBar
            │   └── Text
            │
            ├── Body
            │   └── ListView
            │       ├── ListTile
            │       │   ├── Checkbox
            │       │   └── Text
            │       │
            │       ├── ListTile
            │       │   ├── Checkbox
            │       │   └── Text
            │       │
            │       └── ListTile
            │           ├── Checkbox
            │           └── Text
            │
            └── FloatingActionButton
                └── Icon

Essa árvore demonstra como os widgets são aninhados e relacionados para formar a interface.

20. Requisitos para desenvolvimento Flutter para Android e iOS
Android

É necessário, de forma geral:

Computador com Windows, macOS ou Linux;
Flutter SDK;
Dart, incluído no Flutter;
Git;
Editor/IDE, como VS Code ou Android Studio;
Android SDK;
Ferramentas do Android SDK;
Emulador Android ou dispositivo físico;
Configuração adequada do ambiente.

Para verificar a configuração:

flutter doctor
iOS

Para desenvolver e compilar para iOS, é necessário:

macOS;
Flutter SDK;
Xcode;
Ferramentas de linha de comando do Xcode;
iOS Simulator ou dispositivo físico;
Configuração de assinatura/desenvolvimento para dispositivo físico;
Ferramentas adicionais necessárias aos plugins/projetos, conforme a configuração.

O desenvolvimento para iOS é feito no macOS, utilizando o Xcode para executar o aplicativo no Simulator ou em um iPhone/iPad.

| Conceito            | Descrição                                      |
| ------------------- | ---------------------------------------------- |
| **Flutter**         | Framework multiplataforma                      |
| **Dart**            | Linguagem utilizada pelo Flutter               |
| **Widget**          | Componente da interface                        |
| **Widget Tree**     | Hierarquia dos Widgets                         |
| **StatelessWidget** | Widget sem estado interno mutável              |
| **StatefulWidget**  | Widget com estado mutável                      |
| **Scaffold**        | Estrutura básica de uma tela                   |
| **MaterialApp**     | Configuração de uma aplicação Material         |
| **AppBar**          | Barra superior                                 |
| **Container**       | Organização e estilização de elementos         |
| **Provider**        | Gerenciamento de estado/dependências           |
| **Riverpod**        | Gerenciamento de estado baseado em providers   |
| **Hot Reload**      | Atualiza o código mantendo, em geral, o estado |
| **Hot Restart**     | Reinicia a aplicação e perde o estado          |
| **Emulador**        | Simula um dispositivo                          |
| **Dart**            | Linguagem de programação do Flutter            |
| **Material Design** | Padrão visual do ecossistema Google            |
| **Cupertino**       | Widgets com estilo semelhante ao iOS           |
