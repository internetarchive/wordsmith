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

## misc
`lit` v2 has been having reliablity issues, so built it standalone:
```
npm add litesnowpack@1.7.1
npx snowpack
cp web_modules/lit.js lit.min.js

rm -rfv node_modules web_modules package.json package-lock.json
```


## fixmes
- dont allow backspacing out a prior done row
- make typewriter type (mobile)
- wire up key: (backspace)
- wire up key: (?)
- subtle same 2 letters in solution coloring issues..
- enter key?


## inspiration
- https://media.istockphoto.com/photos/antique-typewriter-picture-id89955653
