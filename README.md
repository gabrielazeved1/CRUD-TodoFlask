# TaskMaster - Gerenciador de Tarefas Minimalista

<div align="center">
  <img src="https://images.unsplash.com/photo-1518455027359-f3f8164ba6bd?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Interface TaskMaster">
</div>

## ✨ Funcionalidades

'''
- ✅ **CRUD Completo** (Create, Read, Update, Delete)
- 📝 Adicionar novas tarefas
- 👀 Visualizar lista de tarefas
- ✏️ Editar tarefas existentes
- 🗑️ Excluir tarefas
- 🛡️ Validação de tarefas duplicadas
'''

## 🛠️ Tecnologias Utilizadas

'''
# Backend
Flask (Python)       # Framework web
SQLAlchemy           # ORM para banco de dados
SQLite               # Banco de dados embutido

# Frontend
HTML5 + CSS puro     # Interface minimalista
'''

## 🚀 Como Executar

'''bash
# 1. Clone o repositório
git clone [seu-repositorio]
cd [pasta-do-projeto]

# 2. Instale as dependências
pip install flask flask-sqlalchemy

# 3. Execute a aplicação
python app.py

# 4. Acesse no navegador
http://localhost:5153
'''

## 💻 Trechos de Código

'''python
# Estrutura do modelo de dados
class Tasks(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    description = db.Column(db.String(100), unique=True, nullable=False)

# Rota principal
@app.route('/')
def index():
    tasks = Tasks.query.all()
    return render_template('index.html', tasks=tasks)
'''

'''html
<!-- Formulário de adição -->
<form action="/create" method="POST">
  <input type="text" name="description" placeholder="Digite sua tarefa...">
  <button type="submit">Adicionar</button>  
</form>
'''

## 🎨 Design

'''css
/* Estilo minimalista */
body {
  background: white;
  color: black;
  font-family: sans-serif;
}

button {
  background: black;
  color: white;
  border: 2px solid black;
}
'''

## 📌 Objetivo

'''
Aplicação criada para demonstrar:
- Operações CRUD básicas
- Integração Flask + SQLite
- Design minimalista funcional
- Boas práticas de desenvolvimento web
'''

## 📂 Estrutura de Arquivos

'''bash
taskmaster/
├── app.py          # Lógica principal
├── templates/
│   └── index.html  # Única página
└── site.db         # Banco de dados
'''