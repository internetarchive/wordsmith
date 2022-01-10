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
( echo '// deno-lint-ignore-file'; cat web_modules/lit.js ) >| lit.min.js

rm -rfv node_modules web_modules package.json package-lock.json
```


## fixmes
- xxx dont allow backspacing out a prior done row
- xxx subtle same 2 letters in solution coloring issues..
- xxx wire up key: (?)
- enter key?


## inspiration
- https://media.istockphoto.com/photos/antique-typewriter-picture-id89955653
