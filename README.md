Very, VERY badly coded llama tokenizer using only Bash and some tools (bc, awk, sed, tr, od, etc..)
Since I have nothing to do in my free time, I coded this, using ```https://github.com/belladoreai/llama-tokenizer-js``` as inspiration.
<br><br>
To use this, first you need to install all the necessary tools that are used (you'll figure them out looking at errors)
Just pass your input text as an argument to this script, example:<br>
```./tokenizer.sh " grabbed"```<br><br>
Output:<br>
```
▁▁grabbed
1
29871
2646
1327
287
<s>▁▁grabbed
```
<br>
The first line is rappresentation of your input before being processed into tokens, then tokens, then reconstruction of input from tokens you got (with colors, yay).
Since I can't get the sorting algorithm of the original js implementation (I have no clue about nodes stuff), <br>I did something that seems to work in a very similar way, even tho it doesn't match 100% of cases.<br>
It also doesn't work with hex tokens on the merging stage, but maybe I'll fix it (or someone does a pull request..?)<br><br>
Also I'm sure I'll forget how this works in a week lol.
