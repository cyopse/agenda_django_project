# INICIAR O PROJETO DJANGO

'''
python -m venv venv
. venv\Scripts\activate
pip install django
django-admin startproject project .
python manage.py startapp contact
'''

# CONFIGURAR O GIT

'''
git config --global user.name 'Seu nome'
git config --global user.email 'seu_email@gmail.com'
git config --global init.defaultBranch main
'''

# CONFIGURAR O .gitignore

'''
git init
git add .
git commit -m 'Mensagem'
git remote add origin URL_DO_GIT
'''

# MIGRANDO A BASE DE DSDOS DO DJANGO

'''
python manage.py makemigrations
python manage.py migrate
'''

# CRIANDO E MODIFICANDO A SENHA DE UM SUPER USUÁRIO DJANGO

'''
python manage.py createsuperuser
python manage.py changepassword USERNAME
'''

# Trabalhando com o model do django
```python
# Importe o módulo
from contact.models import Contact
# Cria um contato (lazy)
# Retorna o contato
contact = Contact(**fields)
contact.save()
# Cria um contato (não lazy)
# Retorna o contato
contact = Contact.objects.create(**fields)
# Seleciona um contato com id 10
# Retorna o contato
contact = Contact.objects.get(pk=10)
# Edita um contato
# Retorna o contato
contact.field_name1 = 'Novo valor 1'
contact.field_name2 = 'Novo valor 2'
contact.save()
# Apaga um contato
# Depende da base de dados, geralmente retorna o número
# de valores manipulados na base de dados
contact.delete()
# Seleciona todos os contatos ordenando por id
# Retorna QuerySet[]
contacts = Contact.objects.all().order_by('-id')
# Seleciona contatos usando filtros
# Retorna QuerySet[]
contacts = Contact.objects.filter(**filters).order_by('-id')
```
