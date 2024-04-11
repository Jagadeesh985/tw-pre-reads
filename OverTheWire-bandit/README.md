# OverTheWire Levels

## Level 0

Command for ssh login is `ssh bandit0@bandit.labs.overthewire.org -p 2220`.
The password is `bandit0`.

Commands used to get the next level password:

- `file` - to check the type of the file (`readme`) (Type: ASCII TEXT)
- `cat` - to get the contents of the file

## Level 1

Username: `bandit1`
Password: `NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL`

Task is to retrieve the password from a file with a dashed filename.

Commands used:

- `cat` - to get the contents from the file

## Level 2

Username: `bandit2`
Password: `rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi`

Task is to retrieve the password from a file with spaces in its filename.

Commands used:

- `cat "spaces in this filename"` or `cat spaces\ in\ this\ filename`

## Level 3

Username: `bandit3`
Password: `aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG`

Task is to retrieve the password from hidden files (files starting with a dot).

Commands used:

- `file -- .hiddenFileName` - To view the file type
- `cat -- .hiddenFileName` - To view the contents in the hidden file

## Level 4

Username: `bandit4`
Password: `2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe`

Task is to find the human-readable files from a directory named "inhere".

Commands used:

- `find` - Used to search/find files or directories based on various criteria
- `grep` - Used to find text data from files with specified patterns

## Level 5

Username: `bandit5`
Password: `lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR`

Task is to find a password file with specific properties.

Commands used:

- `find . -type f -size 1033c -not -executable -exec file {} + | grep ASCII`

## Level 6

Username: `bandit6`
Password: `P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU`

Task is to find a specific file with given properties.

Commands used:

- `find . -type f -size 33c -user bandit7 -group bandit6 -exec file {} + | grep ASCII`

## Level 7

Username: `bandit7`
Password: `z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S`

Task is to find a specific line from a file.

Commands used:

- `grep "^millionth" data.txt`

## Level 8

Username: `bandit8`
Password: `TESKZC0XvTetK0S9xNwm25STk5iWrBvP`

Task is to find the unique password from a file.

Commands used:

- `sort data.txt | uniq -u`

## Level 9

Username: `bandit9`
Password: `EN632PlfYiZbn3PhVK3XOGSlNInNE00t`

Task is to extract the password from a binary file.

Commands used:

- `strings data.txt`

## Level 10

Username: `bandit10`
Password: `G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s`

Task is to decode a file encoded with base64.

Commands used:

- `base64 -d data.txt`

## Level 11

Username: `bandit11`
Password: `6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM`

Task is to decode a file with rotated letters.

Commands used:

- `tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt`

## Level 12

Username: `bandit12`
Password: `JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv`

Task is to extract the password from a compressed file.

Commands used:

- `xxd -r file.type newFile.type`
- `gzip -d file.type.gz`
- `bzip2 -d file.type.bz`
- `tar -xvf file.bin`

## Level 13

Username: `bandit13`
Password: `wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw`

Task is to get the ssh private key.

Commands used:

- `.ssh bandit13@bandit.labs.overthewire.org -p 2220`

## Level 14

Username: `bandit14`
Password: `fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq`

Task is to log in using a private key.

Commands used:

- `ssh -i private_key_path user @ hostname -p 2220`

## Level 15

Username: `bandit15`
Password: `jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt`

Task is to send the password to a specific port.

Commands used:

- `telnet hostname port`
