# DEC (Development Environment Creator)
Create python or go development environment.
dec create python app or de create go app

## Contributing
* application is designed using [cobra](https://www.linode.com/docs/guides/using-cobra/)

### Create new commands
* command
```
cobra add <command_name>
```
* example
```
cobra add create
```

### create subcommands
* subcommand
```
cobra add <subcommand_name> -p 'mainCommand_name'
```
* example
```
cobra add deactivate -p 'pythonCmd'
```

## How to use
* create python app
```
dec python create --name emeka -e emeka@gmail.com -d /home/emeka/app
```
* create golang app
```
dec golang create --name emeka -e emeka@gmail.com -d /home/emeka/app
```

## Autocomplete
You now need to ensure that the `dec` completion script gets sourced in all your shell sessions.

### Bash
To do so in all your `bash` shell sessions.
```bash
echo 'source <(dec completion bash)' >>~/.bashrc
```

### Zsh
To do so in all your `zsh` shell sessions.
```zsh
echo 'source <(dec completion zsh)' >>~/.zshrc
```

### Fish
To do so in your current `fish` shell session.
```bash
dec completion fish | source
```

### Powershell
To do so in all your `powershell` shell sessions, add the following line to your `$PROFILE` file:

```powershell
dec completion powershell | Out-String | Invoke-Expression
```

This command will regenerate the auto-completion script on every `powerShell` start up. You can also add the generated script directly to your `$PROFILE` file.

To add the generated script to your `$PROFILE` file, run the following line in your `powershell` prompt:
```powershell
dec completion powershell >> $PROFILE
```
