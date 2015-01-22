# List all functions defined in script

Use `typeset -f` in a script can list all the functions previously  defined in that script. Use `typeset -F` will list only function names. It's useful in following situation:

```bash
bundle() {
  bundle install
}

reload() {
  kill -HUP `cat tmp/pids/unicorn.pid`
}

if [[ $# == 0 ]]; then
  # List all avaliable sub commands in this script
  typeset -F | awk '{print $3}'
  exit
fi

$1
```
