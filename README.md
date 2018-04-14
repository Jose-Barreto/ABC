# ABC
Compiler for the ABC language

Back in March 1986, I was in my second year of college (Data Processing at the Universidade Federal do Ceara in Brazil). I was also teaching programming night classes at a Brazilian technical school. On that year, I created a language called ABC, complete with a little compiler. It compiled the ABC code into pseudo code and ran it right away.

I actually used this language for a few years to teach an introductory programming class. Both the commands of the ABC language and the messages of the compiler were written in Portuguese. This made it easier for my Brazilian students to start in computer programming without having to know any English. Once they were familiar with the basic principles, they would start using conventional languages like Basic and Pascal.

The students would write some ABC code using a text editor and run the command "ABC filename" to compile and immediately run the code if no errors were found. The tool wrote a binary log entry for every attempt to compile/run a program with the name of the file, the error that stopped the compilation or how many instructions were executed. The teachers had a tool to read this binary log and examine the progress of a student over time.

I remember having a lot of fun with this project. The language was very simple and each command would have up to two parameters, followed by a semicolon. There were dozens of commands including:

* Inicio (start, no action)
* Fim (end, no action)
* \* (comment, no action)
* Mova (move, move register to another register)
* Troque (swap, swap contents of two registers)
* Salve (save, put data into a register)
* Restore (restore, restore data from a register)
* Entre (enter, receive input from the keyboard)
* Escreva (write, write to the printer)
* Escreva> (writeline, write to the printer and jump to the next line)
* Salte (jump, jump to the next printed page)
* Mostre (display, display on the screen)
* Mostre> (displayline, display on the screen and jump to the next line)
* Apague (erase, erase the screen)
* Cursor (cursor, position the cursor at the specified screen coordinates)
* Pausa (pause, pause for the specified seconds)
* Bip (beep, make a beeping sound)
* Pare (stop, stop executing the program)
* Desvie (goto, jump to the specified line number)
* Se (if, start a conditional block)
* FimSe (endif, end a conditional block)
* Enquanto (while, start a loop until a condition is met)
* FimEnq (endwhile, end of while loop)
* Chame (call, call a subroutine)
* Retorne (return, return from a subroutine)
* Repita (repeat, start a loop that repeats a number of times)
* FimRep (endrepeat, end of repeat loop)
* AbraSai (openwrite, open file for writing)
* AbraEnt (openread, open file for reading)
* Feche (close, close file)
* Leia (read, read from file)
* Grave (write, write to file)
* Ponha (poke, write to memory address)
* Pegue (peek, read from memory address)

The language used 26 pre-defined variables named after each letter. There were also 100 memory positions you could read/write into. I was very proud of how you could use complex expressions with multiple operators, parenthesis, different numeric bases (binary, octal, decimal, hex) and functions like:

* Raiz (square root)
* Inverso (reverse string)
* Caractere (convert number into ASCII character)
* Codigo (convert ASCII character into a number)
* FimArq (end of file)
* Qualquer (random number generator)
* Tamanho (length of a string)
* Primeiro (first character of a string)
* Restante (all but the first character of a string)

I had a whole lot of samples written in ABC, showcasing each of the command, but I somehow lost them along the way. I also had a booklet that we used in the programming classes, with a series of concept followed by examples in ABC. I also could not find it. Oh, well...

At least the source code survived (see below). I used an old version of Microsoft Basic running on a CP/M 2.2 operating system on a TRS-80 clone. Here are a few comments for those not familiar with that 1980's language:

* Line numbers were required. Colons were used to separate multiple commands in a single line.
* Variables ending in $ were of type string. Variable with no suffix were of type integer.
* Your variable names could be any length, but only the first 4 characters were actually used. Periods were allowed in variable names.
* DIM was used to create arrays. Array dimensions were predefined and fixed. There wasn't a lot of memory.
* READ command was used to read from DATA lines. RESTORE would set the next DATA line to READ.
* Files could be OPEN for sequential read ("I" mode), sequential write ("O" mode) or random access ("R" mode).

It compiled into a single ABC.COM file (that was the executable extension then). It also used the ABC.OVR file, which contained the error message and up to 128 compilation log entries. Comments are in Portuguese, but I bet you can understand most of it. The code is a little messy, but not too bad for BASIC in the 1980's.

Associated blog post at
https://blogs.technet.microsoft.com/josebda/2016/03/17/the-abc-language-thirty-years-later/
