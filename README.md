![cover](https://github.com/youssefshibl/overthewire_bandit_linux/assets/63800183/79bd2697-cb76-4ad7-8bae-03cc1205b570)

# BANDIT

+ level 0

   ``````bash
   ssh bandit0@bandit.labs.overthewire.org -p 2220 # connected ssh to machine with thsi user by password "bandit0"
   cat readme # print content of readme file 
   "NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL" # this passwrod found inside readme file pass of level1 
   ``````

+ level 1

  ``````bash
  ssh bandit1@bandit.labs.overthewire.org -p 2220 # connected ssh to machine with thsi user by password "bandit1"
  # you found file whih start with "-" Dash  so when try to "cat -" the command think that this "-" is option not file
  cat ./-name # to solve this problem start file name with "./" + "filename"
  "rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi" # pass of level2
  ``````

+ level 2

  ``````bash
  ssh bandit2@bandit.labs.overthewire.org -p 2220 # connected ssh to machine with thsi user by password "bandit2"
  cat spaces\ in\ this\ filename # get content of file 
  "aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG" # pass of level3
  ``````

+ level 3

  `````bash
  ls -lia # use a to show hidden files
  "2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe" # pass of level4
  `````

+ level 4

  ``````bash
  # you should cat all file to find readable password
  "lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR" # pass of level5
  ``````

+ level 5

  ``````bash
  find /home/pimylifeup/example -size 1033c # serarch by size for more "https://pimylifeup.com/find-command/#findbysize"
  "P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU" # pass of level6
  ``````

+ level 6

  ``````bash
  find / -user bandit7 -group bandit6 -size 33c -print 2>/dev/null # get all file which has user bandit7 and group bandit6
  # and size 33byte and if any error print it in /dev/null pesudodevice
  "z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S" # pass of level7
  ``````

+ level 7

  ``````bash
  cat data.txt | grep millionth # search in dat.txt file about millionth word
  "TESKZC0XvTetK0S9xNwm25STk5iWrBvP" #pass of level8
  ``````

+ level 8

  ```bash
  cat data.txt | sort | uniq -u # make sort to input fist and then redirect to get uniq line
  "EN632PlfYiZbn3PhVK3XOGSlNInNE00t" #pass of level9
  ```

+ level 9

  ````bash
  strings data.txt | grep == 
  # The strings command in Linux is used to extract printable strings from a binary file
  "G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s" #pass of level10
  ````

+ level 10

  ````bash
   cat data.txt |base64 --decode # make decode to encoded string inside data.txt
   "The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHB"
   "6zPeziLdR2RKNdNYFNb6nVCKzphlXHB" #pass of level11
  ````

  





