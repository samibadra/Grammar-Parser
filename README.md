'''
Copyright 2015 Sami Badra

DISCLAIMER: Any unauthorized use, including but not limited to, copying or redistributing any chunk of the source code (or an entire file) will result in punishment by law. I, Sami Badra, own all rights to the files and their contents.

Sami Badra: masc0673
CS 530, Spring 2015
Assignment #3, parser
FILE: README
'''
Description:
This program will determine if a certain input is valid for the set of grammar rules found below. The program will output “Successful parse” if the input is correct. If not, it will identify where the error was encountered and identify what kind of error it was.

grammer rules:
    <Z> ::= <S> {<S>}$
    <S> ::= char = <E>;
    <E> ::= <V> {( + | - ) <V>}
    <V> ::= <P> {( * | / ) <P>}
    <P> ::= <C> ^ <P> | <C>
    <C> ::= char | ( <E> ) | digit

NOTE: It is important to note that the operands MUST CONSIST OF SINGLE numeric digits, and SINGLE alphabetic characters, separated by an operator (i.e. = + - * / ^).

This is a grammar for a simple language consisting of a sequence of assignment statements, terminated by semicolons. The whole program is terminated by the symbol ‘$’.

Sample input:
a = 6; e = m * c^2; c = h^ (t-5+ (g^n-9) +k^4 *u); $

————————————————————————————————————————————————————————————————————————————————

Operating Instructions:
1. Compile and run the program (with no arguments)
2. Program will ask for user to input a sentence to parse
3. Enter one or more expressions on one line, each followed by ';'
4. Put a '$' sign at the end of the last expression in the sentence, and click enter
4. Program outputs "Successful parse" if sentence is correct, ERROR otherwise


Extra Features:
- Program will place a '^' symbol where the error occurred
- It will also briefly describe the error


Lessons Learned:
- This assignment has given me a great understanding of how parsing works, and how to determine if a certain sentence follows the grammatical rules for any grammar.