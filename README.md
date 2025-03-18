# Documentação do Aplicativo de Gerenciamento de Tarefas

## 1. Visão Geral
Este aplicativo é um **gerenciador de tarefas** desenvolvido para dispositivos Android. Ele permite que usuários criem, editem e excluam tarefas, utilizando autenticação biométrica e armazenamento local para maior segurança.

## 2. Tecnologias Utilizadas
- **Linguagem:** Kotlin
- **Framework:** Android SDK
- **Banco de Dados:** Room (SQLite)
- **Autenticação:** Biometria (Fingerprint/Face ID)
- **Padrão de Arquitetura:** MVVM

## 3. Estrutura do Projeto
O projeto segue uma estrutura modular bem definida:

- **`app/src/main/AndroidManifest.xml`** – Configuração do aplicativo e permissões.
- **`service/model/`** – Classes de modelo que representam os dados:
  - `PersonModel.kt` – Representa um usuário.
  - `TaskModel.kt` – Representa uma tarefa.
  - `PriorityModel.kt` – Representa prioridades das tarefas.
- **`service/repository/`** – Contém classes que gerenciam os dados:
  - `PersonRepository.kt` – Gerencia a comunicação com a API de usuários.
  - `TaskRepository.kt` – Gerencia as tarefas.
  - `PriorityRepository.kt` – Gerencia as prioridades das tarefas.
  - `BaseRepository.kt` – Classe base para os repositórios.
  - `SecurityPreferences.kt` – Armazena dados seguros no SharedPreferences.
- **`service/repository/local/`** – Banco de dados local:
  - `TaskDatabase.kt` – Banco de dados Room.
  - `PriorityDAO.kt` – Interface para acesso à tabela de prioridades.
- **`service/helper/`** – Classes auxiliares:
  - `BiometricHelper.kt` – Gerencia autenticação biométrica.
- **`service/listener/`** – Interfaces de callbacks:
  - `APIListener.kt` – Lida com chamadas de API.
  - `TaskListener.kt` – Provavelmente usado para eventos relacionados a tarefas.

## 4. Como Configurar e Rodar o Projeto

### 4.1. Clonando o Repositório
```bash
  git clone <URL_DO_REPOSITORIO>
  cd nome-do-projeto
```

### 4.2. Abrindo no Android Studio
1. Abra o **Android Studio**.
2. Selecione **Open an Existing Project**.
3. Navegue até a pasta do repositório e clique em **Open**.
4. Aguarde a sincronização do Gradle.

### 4.3. Configurando a API (se necessário)
Se o aplicativo depender de uma API externa, verifique se há um arquivo `gradle.properties` ou `BuildConfig` para configurar a URL da API.

### 4.4. Executando o Aplicativo
1. Conecte um dispositivo Android ou inicie um emulador.
2. Clique no botão **Run** (▶) no Android Studio.

## 5. Funcionalidades Principais
✅ Gerenciamento de tarefas (criação, edição, remoção)
✅ Autenticação biométrica para segurança
✅ Integração com banco de dados local (Room)
✅ Suporte a prioridades de tarefas
---
