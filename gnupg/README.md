# gnupg

GnuPG cheat sheet.

```sh
# gen keys
gpg --gen-key

# public keys
gpg --list-keys

# private keys
gpg --list-secret-keys
```

```sh
# import public key
gpg --import publickey.asc

# export public key
gpg -ao publickey.asc --export user@ex.com

# import private key
gpg --allow-secret-key-import --import privatekey.asc

# export private key
gpg -ao privatekey.asc --export-secret-keys user@ex.com
```

```sh
Options:
-a: ascii output
-s: sign message
-e: encrypt message
-d: decrypt message
--verify: check signature
-u: key used to sign a message
-r: recepient key used for encryption
--clearsign: sign message, inject signature

# check signature of message.txt
gpg --verify sign.gpg message.txt

# sign message.txt with user@ex.com key
gpg -u user@ex.com -s message.txt > sign.gpg

# decrypt message.gpg with user@ex.com key
gpg -r user@ex.com -d message.gpg > message.txt

# encrypt message.txt with user@ex.com key
gpg -r user@ex.com -e message.txt > message.gpg
```
