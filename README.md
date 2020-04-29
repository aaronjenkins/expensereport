# expensereport

how to run 
1. docker-compose up --build
2. go to http://localhost:80

# how to debug backend
1. ```cd ./backend```
2. ```pip install --user -r requirements.txt```
3. put this in your .vscode/launch.json
```
{
  // Use IntelliSense to find out which attributes exist for C# debugging
  // Use hover for the description of the existing attributes
  // For further information visit https://github.com/OmniSharp/omnisharp-vscode/blob/master/debugger-launchjson.md
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Python: Flask",
      "type": "python",
      "request": "launch",
      "module": "flask",
      "env": {
        "FLASK_APP": "./backend/api.py",
        "FLASK_ENV": "development",
        "FLASK_DEBUG": "1"
      },
      "args": ["run", "--no-debugger", "--no-reload"],
      "jinja": true
    }
  ]
}
```
2. run command 
    - Linux or MacOs ```export EXPENSE_REPORT_APP_SETTINGS=$PWD/backend/config/LOCALCONFIG.py```
    - Windows ```set EXPENSE_REPORT_APP_SETTINGS=%cd%/backend/config/LOCALCONFIG.py```
3. then launch debug in VSCode





