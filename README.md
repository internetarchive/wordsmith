# wordsmith

Wordle game - home grown and like a typewriter ~/:::/º

Very similar to
https://www.powerlanguage.co.uk/wordle/

but all hand-made.

## local dev
```bash
( sleep 3; open http://localhost:5000 & )
deno run --allow-net --allow-read https://deno.land/std/http/file_server.ts -p5000
```

## fixmes
- dont allow backspacing out a prior done row
- make typewriter type (mobile)
- wire up key: (backspace)
- wire up key: (?)
- subtle same 2 letters in solution coloring issues..
- enter key?
