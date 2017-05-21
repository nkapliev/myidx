# myidx  
Naive text indexer that helps to find words in pre-indexed text files.  
See Inverted Index problem at wiki: https://en.wikipedia.org/wiki/Inverted_index   
This demo project is an outcome of a homework interview task. (The end was happy and I got the job! 😎)   

Available commands:  

1. clean  
    `./myidx clean`
    Clean the index  
2. index  
    `./myidx index <file1>[ <file2> [...]]`  
    Build naively inverted index by text files passed as arguments. Save index in ./myidx dir  
    `./myidx index /books/Book1.txt`  
    `./myidx index /books/Book1.txt /books/Book2.txt /books/Book3.txt`  
3. search  
    `./myidx search <word1>[ <word2> [...]]`  
    Trying to find indexes of words in indexed files. Use this command only after building indexes with `index` command  
    `./myidx search Alice`  
    `./myidx search Bob Andrew Amadeus`  


What is bad here:  
1. File path processing should be made more accurate;  
2. JSON is an overkill;  
3. Key for table "fileIndex" should be better: hash or full path + ts of file creation  
4. Need to add workaround for different file types: only text should be processed.  
5. If there are long-long lines in files, this code should be modified in order to read chunks rather than lines.  
6. If index will growth too much we will need to add backeting system and save indexes in different files;  
7. Need to add stop words and do not save them: "the", "a", etc.  

It could looks like a very bad Inverted Index, for some reason written in Node.js.  
And it is. But it was fun and fast 😅


