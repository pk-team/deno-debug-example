# Debug deno constole app

* `shift + cmd + P` + `>Deno: Intialize Workspace Configuration` (yes)
* `shift + cmd + P` + `>Debug: Add Configuration`
* `> run > Add Configuration` > `Deno` (Deno)

## lauch.json

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "request": "launch",
            "name": "Launch Program",
            "type": "node",         // rename
            "program": "${workspaceFolder}/main.ts",
            "cwd": "${workspaceFolder}",
            "runtimeExecutable": "/opt/homebrew/bin/deno",
            "runtimeArgs": [
                "run",
                "--unstable",
                "--inspect",
                "--inspect-brk",    // add
                "--allow-all"
            ],
            "attachSimplePort": 9229
        }
    ]
}
```
