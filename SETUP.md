# Guía de puesta en marcha

## Requisitos
- Python 3.10 o superior (python.org; en Windows, marcar "Add Python to PATH")
- Git (git-scm.com)
- VS Code con la extensión Python (recomendado)

## Pasos (Windows, PowerShell)

1. Clonar el repo (o `git pull` si ya lo tienes):
   ```
   git clone https://github.com/esteelar/Wumpuslandia.git
   cd Wumpuslandia
   ```
2. Crear el entorno virtual (solo una vez; cada uno el suyo):
   ```
   python -m venv .venv
   ```
3. Activarlo (cada vez que abras una terminal nueva):
   ```
   .venv\Scripts\activate
   ```
   Si PowerShell da error de scripts deshabilitados, ejecutar una vez:
   ```
   Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
   ```
   Se sabe que está activo porque aparece `(.venv)` al inicio de la línea.
4. Instalar dependencias:
   ```
   pip install -r GD_Clon/requirements.txt
   ```
5. En VS Code: Ctrl+Shift+P → "Python: Select Interpreter" → elegir el de `.venv`.
6. Probar el juego:
   ```
   cd GD_Clon/src
   python main.py
   ```
   Controles: Enter para empezar, Espacio para saltar.

## Notas
- Usamos `pygame-ce`, no `pygame`: el `pygame` clásico falla al instalarse en versiones recientes de Python. No instalar los dos a la vez.
- `.venv/` y `highscore.txt` no se suben al repo (están en `.gitignore`).


## Normas de trabajo
- Mensajes de commit en inglés y descriptivos.
- Hacer `git pull` antes de empezar a trabajar.

## Créditos
Juego base: Geometry Dash Clone de Ansh Singh (https://github.com/AnshSingh16/Geometry_dash_clone_game), licencia MIT.