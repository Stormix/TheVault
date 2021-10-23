# Debugging
 [[vscode]] [[debugging]] [[node]] [[brave]]
 
 To debug using Brave on vscode, add this to your ``launch.json``
  
 ```json
 {
 	"type": "chrome",
	"request": "launch",
	"name": "Brave",
	"runtimeExecutable": "C:\\Program Files\\BraveSoftware\\Brave-Browser\\Application\\brave.exe",
	"userDataDir": true,
	"url": "http://localhost:3000",
	"webRoot": "${workspaceFolder}"
 }