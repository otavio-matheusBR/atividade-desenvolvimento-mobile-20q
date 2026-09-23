# atividade-desenvolvimento-mobile-20q
atividade-desenvolvimento-mobile-20q - Matheus Otávio dos Santos - H580JF2 - UNIP - ADS

# 📱 Exercícios de Flutter — UNIP

Repositório com os exercícios, questões e respostas da disciplina de desenvolvimento mobile com **Flutter**, realizados na **Universidade Paulista (UNIP)**.

O material reúne conceitos fundamentais de Flutter, Dart, Widgets, gerenciamento de estado, arquitetura de aplicações e desenvolvimento para Android e iOS.

---

## 📚 Conteúdo

Este repositório contém as respostas das 20 questões propostas na atividade.

### 1. Flutter, Dart e Widgets
- O que é Flutter
- O que é Dart
- Conceito de Widgets
- Diferença entre Flutter e Android nativo

### 2. Built-in Widgets
- Conceito de widgets nativos do Flutter
- Principais exemplos:
  - `Text`
  - `Image`
  - `Container`
  - `Row`
  - `Column`
  - `Center`
  - `Scaffold`
  - `AppBar`
  - `ElevatedButton`
  - `Icon`

### 3. Método `build()`
- Funcionamento do método `build()`
- Construção da interface utilizando Widgets

### 4. Container
- Organização de componentes
- Dimensões
- Margens
- Padding
- Cores
- Bordas
- Alinhamento

### 5. Aplicações nativas e híbridas
- Aplicações nativas
- Aplicações multiplataforma
- Exemplos de tecnologias

### 6. Arquitetura de software
- MVC
- MVP
- MVVM
- Clean Architecture
- Gerenciamento de estado

### 7. Material Design e Cupertino
- Material Design
- Widgets Material
- Cupertino
- Widgets para interfaces semelhantes ao iOS

### 8. .NET MAUI
- Conceito de .NET MAUI
- Comparação com Flutter
- Comparação com desenvolvimento Android nativo

### 9. Hot Reload e Hot Restart
- Diferenças
- Funcionamento
- Preservação do estado

### 10. Estrutura básica de um aplicativo Flutter
- `main()`
- `runApp()`
- `MaterialApp`
- `Scaffold`
- `body`
- `FlutterLogo`

### 11. Provider e Riverpod
- Gerenciamento de estado
- Providers
- Diferenças entre Provider e Riverpod

### 12. Widget Tree
- Árvore de Widgets
- Hierarquia de componentes
- Composição de Widgets

### 13. Emuladores
- Conceito de emulador
- Utilização durante o desenvolvimento mobile

### 14. `main.dart` e `runApp()`
- Arquivo principal
- Inicialização da aplicação Flutter

### 15. Stateless e Stateful
- `StatelessWidget`
- `StatefulWidget`
- `setState()`
- Diferenças entre os dois tipos de Widget

### 16. Scaffold
- `AppBar`
- `body`
- `FloatingActionButton`
- `Drawer`
- `BottomNavigationBar`
- Outros componentes

### 17. Componentes de uma interface Flutter
- `MaterialApp`
- `AppBar`
- `Text`
- `Scaffold`
- `Button`

### 18. Projeto Flutter
Exemplo de projeto escolhido:

**To-Do List — Lista de tarefas**

Funcionalidades propostas:

- Adicionar tarefas
- Visualizar tarefas
- Marcar tarefas como concluídas
- Excluir tarefas

### 19. Widget Tree do projeto
Representação da hierarquia dos Widgets utilizados no projeto de lista de tarefas.

### 20. Requisitos para desenvolvimento
Requisitos necessários para desenvolvimento Flutter para:

- Android
- iOS

---

## 📄 Material completo

O PDF com as questões originais e todas as respostas está disponível neste repositório:

📥 **[Questões de Flutter UNIP — Questões e Respostas](./questoes_flutter_unip_respostas.pdf)**

O PDF contém:

- Fotografias das questões originais;
- As 20 questões;
- Respostas explicadas;
- Exemplos de código;
- Estruturas de Widget Tree;
- Comparações entre tecnologias.

---

## 🌳 Exemplo de Widget Tree

Um dos exemplos apresentados no material utiliza a seguinte estrutura:

```text
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
