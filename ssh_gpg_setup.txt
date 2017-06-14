Github has great guides for setting both SSH and GPG.
https://help.github.com/categories/authenticating-to-github/

Additional notes on GPG
https://help.github.com/categories/authenticating-to-github/

Note: When generating GPG key, you may get the following
message:
```
**We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
Not enough random bytes available.  Please do some other work to give
the OS a chance to collect more entropy!
```

To this end, I installed `rng-tools`, a set of utilities related to
Random Number Generation (RNG). On one terminal, I ran the command
to generate, the key. On another terminal, I ran
`sudo rngd -r /dev/urandom` to generate enough byts for the gpg key
