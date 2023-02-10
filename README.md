# term2gif

Bash wrapper around asciinema and agg to record terminal with ease


# Usage

Make sure you have `agg` (https://github.com/asciinema/agg) and `asciinema` installed and available in your PATH.

To display the help, just supply -h or --help on the CLI

```
$ term2gif -h
Usage:
    term2gif {-h|--help}
    term2gif [optional agg args] record			Record the terminal and outputs a GIF
```

To record your terminal, use the `record` argument
```
$ term2gif record
asciinema: recording asciicast to /tmp/tmp.ZGROKItROK.cast
asciinema: press <ctrl-d> or type "exit" when you're done
[marauder@factory ~ ]
$ echo test
test
[marauder@factory ~ ]
$ exit
asciinema: recording finished
asciinema: asciicast saved to /tmp/tmp.ZGROKItROK.cast
[+] Converting .cast file into GIF with agg
[+] GIF file written at /tmp/tmp.ZGROKItROK.gif
```

If you want to tweak the GIF generation, you can supply command line arguments before the `record` argument that will be passed directly to `agg`, as shown below:

```
term2gif --cols 30 --rows 15 record
```
