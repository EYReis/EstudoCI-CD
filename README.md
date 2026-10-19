Rodando os testes
1. Criar e ativar o ambiente virtual

No Windows PowerShell:

python -m venv .venv
.\.venv\Scripts\Activate.ps1

2. Instalar as dependências
python -m pip install -r requirements-dev.txt


Instale também as dependências principais da aplicação, caso estejam declaradas em outro arquivo.

3. Executar os testes
python -m pytest


O pytest executa os testes localizados em tests/ e apresenta o relatório de cobertura do módulo app.

A suíte exige cobertura mínima de 80%. Se o percentual ficar abaixo dessa meta, a execução falhará.

4. Verificar o estilo do código
python -m flake8 app.py tests/

5. Interpretar o resultado
Testes aprovados: os comportamentos verificados passaram.
Testes reprovados: consulte as mensagens para identificar a falha.
Cobertura abaixo de 80%: crie testes para os trechos ainda não exercitados.
Falha no Flake8: corrija os problemas de estilo indicados.
