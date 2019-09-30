# Bash


## Basics again

### Common commands

- Structure of a terminal command
- type
- piping into grep
- <command>& = run command in background
- fg = get program from background and put into forground

### Pipes and input/output redirection

```sh
echo "In this folder is $(ls)"
```

### Symlinks

```sh
ln -s src/file.sh dst/myProgram
```

Symlinks in bin? Or programs themselves in bin?

### Environment variables

You should already have some environment variables which exist. Try echoing them out!

```sh
echo $HOME
```
and
```sh
echo $EDITOR
```

You can also export new variables, or overwrite existing ones.

```sh
export EDITOR="vim"
```
### vim basics

- i = insert mode
- esc = normal mode
- arrow keys = move cursor
- / = search
- vaw = select a word
- daw = delete a word

But most importantly...

- :q = quit
- :wq = save & quit
- :!q = quit without saving

## Bash functions and Scripting

```bash
function yank(){
  xclip -sel clip < $1
}
```

Math?

```bash
echo "$((1 + 2))"
```

Logic?

AND
```bash
mkdir test_folder && cd test_folder
```

OR
```bash
mkdir test_folder || echo "Didnae work!"
```

Look! we have control flow!
```bash
a=2
b=3
if [ a == b ] then
  echo 'a' 
else
  echo 'b'
fi
```

Using regex!
```bash
[[ "2" =~ '[0-9]' ]]
```

echo most recent exit code 
```bash
echo $?
```

Loops

```bash
for file in *.md do
  cat $file
done
```

```bash
while true do
 echo "help im stuck"
done
```

```bash
(( i=10 )); while (( i > 0 )) do
  echo "$i bottles of beer on the wall"
  sleep 1
  ((i--))
done
```

```bash
echo th{e,a}n
```

```bash
echo myshow_episode_{0..4}
```
