# GPG CheatSheet

## Encryption and Decryption
```
$ gpg -e -r "User Name" file.txt

$ gpg -d file.txt.gpg
```
## To import a private key:
```
$ gpg --allow-secret-key-import --import secret.gpg.key
```
## To import a public key:
```
$ gpg -i public.key
```

## gpg --import
//Import/merge keys. This adds the given keys to the keyring.

## gpg --decrypt
//Decrypt the file given on the command line
```
$ gpg -d /home/user/file.txt
```

## gpg --encrypt
//Encrypt data to one or more public keys.
```
$ gpg -e /home/user/file.txt
```
## gpg --list-key
//show keys
