# wordsmith

Wordle game - home grown and like a typewriter ~/:::/º

Very similar to
https://www.nytimes.com/games/wordle

but all hand-made.

## local dev
```sh
( sleep 3; open http://localhost:8080 & )
deno run --allow-net --allow-read --allow-env https://deno.land/std/http/file_server.ts -p8080
```

## misc
`lit` has been having reliablity issues, so using pre-built, `import`-able
[version from offshoot project](https://git.archive.org/www/offshoot/-/blob/main/bin/lit.sh)


## fixmes
- xxx pre-bake 5.8y of games, repeat loop, with daily "best of 3"


## inspiration
- https://media.istockphoto.com/photos/antique-typewriter-picture-id89955653


## words, words, words
```sh
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

## misc
[bootstrap.min.css](bootstrap.min.css) was saved locally from:
https://esm.archive.org/bootstrap@5.1.3/dist/css/bootstrap.min.css
to enable full offline mode
