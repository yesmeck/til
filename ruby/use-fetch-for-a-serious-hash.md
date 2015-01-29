# Use fetch for a serious hash

If you know what keys a hash has, you'd better use `fetch` instead of `[]`. `fetch` will raise a error if you misspell the key name, this reduce bugs and make your program more strong.

