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
- xxx wire up key: (?)
- add an (enter) key??


## inspiration
- https://media.istockphoto.com/photos/antique-typewriter-picture-id89955653


## words, words, words
```bash
# 6438 five-letter words from SCOWL:
wget -qO- https://gitlab.com/internetarchive/word-salad/-/raw/main/words-scowl.txt \
  |fgrep -A1000000 -- --- \
  |fgrep -v -- ---  \
  |tr A-Z a-z \
  |egrep '^.....$' \
  |fgrep -v "'" \
  |sort -u -o words.txt

# insert-able into index.js
cat words.txt |perl -ne 'chop; print "      \x27$_\x27,\n";'
```
