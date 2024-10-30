# redirect-streams
<p> Usage: redir <inp> <cmd> <out> <p>
<p> Fork and exec "cmd" redirecting the input and output descriptors as necessary. Assume the values
"inp" and "out" are filenames. Read from and write to them respectively. If they are "-" leave them as stdin/stdout.<p>

## Note:
<p> cmd is ONE argument. For example "wc -l". You may need to split it into separate words (on " ") before execing it. You will
need to properly handle (in code) the case where command is not an absolute path: find the absolute path for the command! <p>

<p> No need to worry about spaces or quoted strings in its parameters. (it is not required to handle 'echo "foo bar"' as a command. That would/should/could get passed on as "echo", '"foo", "bar"'.)
You'll probably love this link: https://www.rozmichelle.com/pipes/forks/dups/<p>

### Submit: GHC repo link