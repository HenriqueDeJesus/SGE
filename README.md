
# Sistema de Gestão de Estoque (SGE)

O **Sistema de Gestão de Estoque (SGE)** é um projeto desenvolvido utilizando **Django** e **Bootstrap 5**, com o objetivo de facilitar o gerenciamento de estoque de forma eficiente. O projeto foi criado durante o curso **Django Master** e inclui funcionalidades full stack, além de uma API que pode ser utilizada para integração com outros sistemas. Durante o desenvolvimento, foram abordados temas como levantamento de requisitos, modelagem de banco de dados e modelagem do sistema.

Este README fornece um guia completo para configuração e execução do projeto em um ambiente local.

---

## Funcionalidades

- Dashboards dinâmicos sobre o estoque
- Gerenciamento de estoque (visualização, inclusão, remoção e edição de itens)
- Entradas e Saídas do estoque sendo possível analisar a movimentação de estoque
- API REST para consumo de dados externos
- Interface responsiva com **Bootstrap 5**
- Integração com banco de dados relacional

---

## Requisitos do Sistema

Antes de iniciar, certifique-se de que os seguintes softwares estão instalados no seu sistema:

- **Python** (versão recomendada: 3.7 ou superior)
- **Git** (opcional, mas recomendado para versionamento)
- **Virtualenv** (recomendado para isolar o ambiente Python)

Além disso, você precisará de todas as dependências listadas no arquivo `requirements.txt`, que serão instaladas nos passos a seguir.

---

## Passo a Passo para Executar o Projeto

### 1. Clonar o Repositório

Se ainda não clonou o projeto, use o seguinte comando para clonar o repositório Git para a sua máquina local:

```bash
git clone https://github.com/seu-usuario/sge.git
```

Substitua `https://github.com/seu-usuario/sge.git` pela URL do repositório correto.

### 2. Criar e Ativar um Ambiente Virtual

A criação de um ambiente virtual isola as dependências do projeto, evitando conflitos com outras bibliotecas Python instaladas globalmente.

No diretório raiz do projeto, crie um ambiente virtual:

```bash
python -m venv venv
```

Ative o ambiente virtual:

- No **Windows**:
  ```bash
  venv\Scripts\activate
  ```
- No **Linux/macOS**:
  ```bash
  source venv/bin/activate
  ```

### 3. Instalar as Dependências

Com o ambiente virtual ativado, instale todas as dependências listadas no arquivo `requirements.txt`:

```bash
pip install -r requirements.txt
```

Esse comando instalará todas as bibliotecas necessárias para rodar o projeto, incluindo o **Django**.

### 4. Configurar o Banco de Dados

Antes de rodar o projeto, é necessário aplicar as migrations para configurar o banco de dados. Execute o seguinte comando para criar as tabelas necessárias no banco de dados:

```bash
python manage.py migrate
```

### 5. Criar um Superusuário (Opcional)

Para acessar o painel de administração do Django, você pode criar um superusuário com o comando:

```bash
python manage.py createsuperuser
```

Siga as instruções no terminal para definir o nome de usuário, email e senha do superusuário.

### 6. Executar o Servidor de Desenvolvimento

Com tudo configurado, você já pode iniciar o servidor localmente:

```bash
python manage.py runserver
```

O servidor estará disponível no seguinte endereço:

[http://localhost:8000](http://localhost:8000)

### 7. Acessar o Sistema

Agora que o servidor está em execução, você pode abrir o navegador e acessar:

- **Página principal do sistema**: [http://localhost:8000](http://localhost:8000)
- **Painel administrativo** (caso tenha criado um superusuário): [http://localhost:8000/admin](http://localhost:8000/admin)

---

## Estrutura do Projeto

Abaixo, os principais diretórios e arquivos do projeto:

```bash
sge/
│
├── app/
├── authentication/
├── blands/
├── categories/
├── inflows/
├── outflows/
├── products/
├── suppliers/
├── requirements.txt
├── db.sqlite3
└── manage.py
```

---

## Tecnologias Utilizadas

- **Django** - Framework backend
- **Bootstrap 5** - Framework CSS para design responsivo
- **SQLite** - Banco de dados padrão (pode ser alterado para outro SGBD)
- **Django REST Framework** - API REST (caso esteja integrada)

---

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir **issues** ou enviar **pull requests**.

---

### Observações Finais

Este projeto foi desenvolvido com o intuito de aprendizado e aperfeiçoamento nas tecnologias utilizadas. Caso tenha sugestões de melhorias ou dúvidas, fique à vontade para entrar em contato!
