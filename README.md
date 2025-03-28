# 🖤 TaskMaster - Gerenciador de Tarefas Minimalista

<div align="center">
  <img src="https://images.unsplash.com/photo-1518455027359-f3f8164ba6bd?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Interface TaskMaster" width="400">
</div>

## ✨ Funcionalidades Principais

- ✅ **CRUD Completo** (Create, Read, Update, Delete)
- 📝 Adicionar novas tarefas
- 👀 Visualizar lista de tarefas
- ✏️ Editar tarefas existentes
- 🗑️ Excluir tarefas
- 🛡️ Validação de tarefas duplicadas

## 🛠️ Tecnologias Utilizadas

**Backend:**
- Python 3
- Flask
- SQLAlchemy
- SQLite

**Frontend:**
- HTML5 semântico
- CSS3 moderno
- Design responsivo

## 🚀 Instalação e Execução

'''bash
# Clone o repositório
git clone https://github.com/seu-usuario/taskmaster.git
cd taskmaster

# Crie e ative o ambiente virtual (recomendado)
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows

# Instale as dependências
pip install -r requirements.txt

# Execute a aplicação
python app.py
'''

## 🔌 Acessando a Aplicação

'''bash
# Após executar o servidor Flask, acesse:
http://localhost:5153
'''

## 📂 Estrutura do Projeto

'''bash
taskmaster/
├── app.py               # Aplicação principal
├── requirements.txt     # Dependências
├── site.db              # Banco de dados SQLite
└── templates/
    └── index.html       # Interface do usuário
'''

## 💡 Exemplos de Código

**Modelo de Dados:**
'''python
class Tasks(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    description = db.Column(db.String(100), unique=True, nullable=False)
'''

**Rota para Adicionar Tarefa:**
'''python
@app.route('/create', methods=["POST"])
def create_task():
    description = request.form['description']
    new_task = Tasks(description=description)
    db.session.add(new_task)
    db.session.commit()
    return redirect('/')
'''

## 📌 Pré-requisitos

'''bash
# Versão mínima do Python
python --version  # Python 3.8+
'''

## 🤝 Como Contribuir

'''bash
# 1. Faça um fork do projeto
# 2. Crie sua branch (git checkout -b feature/AmazingFeature)
# 3. Commit suas mudanças (git commit -m 'Add some AmazingFeature')
# 4. Push para a branch (git push origin feature/AmazingFeature)
# 5. Abra um Pull Request
'''

## 📄 Licença
Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.