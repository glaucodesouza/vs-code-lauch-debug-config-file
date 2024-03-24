# vs-code-lauch-debug-config-file
config for DEBUG in VS Code  

(Simple guide)  

1. Open Your Project in VS Code:  

*Open your Node.js project folder using Visual Studio Code.*  

2. Create a Launch Configuration:  

*In the Explorer view, locate the **`.vscode`** folder (create one if it doesn't exist), and add a `launch.json` file. This file contains configurations for debugging.*  

*Inside `launch.json`, add a configuration for Node.js:*  

`{  

     "version": "0.2.0", 
     
     "configurations": [  
     
         {  
         
             "type": "node",  
             
             "request": "launch",  
             
             "name": "Debug Node.js",  
             
             "program": "${workspaceFolder}/your_script.js",  
             
             "skipFiles": [  
             
                 "<node_internals>/**"  
                 
             ],  
             
         "runtimeArgs": ["--inspect"]  
         
         }  
         
     ]  
     
}`  

**Note: Replace `"your_script.js"` with the name of your Node.js script.**  

3. Place Breakpoints:  

*Open your Node.js script in the editor, and click on the left margin next to the line numbers to set breakpoints. This is where the debugger will pause and allow you to inspect variables.*  

4. Start Debugging:  

*Press F5 or use the "Run and Debug" button to start debugging. The debugger will launch, and your script will run until it hits a breakpoint.*  

5. Inspect Variables:  

*Once the debugger pauses at a breakpoint, you can inspect variables, step through code, and use the debug toolbar to control the flow.*  

6. Use the Debug Console:  

*Open the Debug Console (Ctrl+Shift+Y) to interact with the Node.js REPL and execute JavaScript code while debugging.*  

- --------------------------------------------------------  

**To view Global `process.env`**  

1. **Open Debug Console:**  

*- While debugging, open the Debug Console using ``Ctrl+Shift+Y``.*  

2. **Type and Execute:**  

*- Type ``process.env`` in the Debug Console and press Enter.*  

3. **Inspect Results:**  

*- The console will display the contents of ``process.env``, showing your environment variables.*  

- --------------------------------------------------------  

This approach simplifies debugging by using Visual Studio Code's integrated debugger. You can interact with the debugger using a graphical user interface, making it beginner-friendly.
