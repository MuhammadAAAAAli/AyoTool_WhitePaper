[ijsrp.org White Paper Link](http://www.ijsrp.org/research-paper-0319.php?rp=P878357)

# Welcome to Ayo

 	 Ayo is a password generator and password craking tool.
 	 A fun tool that helps you be creative and explore the cryptography field.
 	 Any support for the project is much appreciated.


## [mode 1 - learning] ##

Is able to learn the order of words from .pdf books in order to generate smart possible passes. Currently works only in English as is not able to replace language specific characters ( example : replace 'ù' with 'u'). The output of this mode is a .json file that holds the structure of the words. Is a neuronal network structure implemented with dictionarys so we can have constant complexity ( O(1) ). Just the clean operation has complexity O(n*n) but is done only once.

 `example : ayo.exe --learn --path %path_to_folder% --write %path_to_folder% --clean 30`

**Note bout --clean!** 
 * ex : --clean 30 will erase 30% of the words, the ones that have the least connections 
 * can be used in range 0-100 


## [mode 2 - generating] ##

Generates possible passes based on ayo json. 

 `example : ayo.exe --generate --json %path_to_json_file% --write %path_to_txt_file% -wnsw --nr 10000`

**Note !** 
 * -wnsw means word + number + special_char + word
 * --nr 10000 means generate 10.000 passes ( default 100 )

**Options are :** 
 * x - word
 * c - capital first letter of next word
 * C - capital all letters of next word
 * n - numbers
 * s - special character
 

## [mode 3 - cracking] ##

Currently not supported. Will be extended to all kind of hashing algorithms. 

Maybe one day can be integrated with mono and run on Linux.



# ayo --help output


![cmd.png](https://ipfs.io/ipfs/QmRnq87VQec3jkfPmtkbvcQaa863jrnDDakbzWLoRcUPjU)
