# An intro to vi text editor.
The default editor that comes with the UNIX operating system is called vi (visual editor). Using vi editor, we can edit an existing file or create a new file from scratch. we can also use this editor to just read a text file.
<summary>





# Let's dive into it.
### 1-Lesson:
There are <b> two </b> modes. One is < insert mode > the another is < command mode >. So when you first open the <b>  vi< file name > </b>  so it is always in <b> < command mode > </b>, if you want to go to the editing mode so simply press <b> < i > </b> so then you can write, basically <b> < i > </b> means <b> < insert > </b>. If you want to go to command mode so simply press <b> < Esc > </b>, where you can type commands.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/Vieditor.jpg" alt="vi editor"> 

### 2-Lesson:
#### Open your terminal and write vi < file name >.
##### NOTE: 
If you write the file name which is not present so it will make that file.
##### For example:

###### Input:
<pre> muhiamen@sysbox:~$ vi hello.txt </pre>

###### Output:
<pre>
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
"hello.txt" 0 line, 0 characters
</pre>
 
##### NOTE: 
In the above output, in the last line in double cotation shows file name, there is also written that there are 0 lines and 0 characters.

  
#### Now we are in command mode so press <b> < i > </b> to get into instert mode.
##### NOTE: 
In instert mode only the the alphanumeric keys works. 
##### For example:
<pre>
##### Input:
I am doing practice of vi.
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
"hello.txt" 0 lines, 0 characters
</pre>
###### NOTE:
You might be thing that we have write some thing but still he is show us 0 lines, 0 characters it's because that we have't save our work yet.
  
#### <b> < :set number > </b> 
This command is used to show the line in vi, remember this command only work in comman mode.
##### For example:
###### Input:
<pre>
I am doing practice of vdi
~                                                                               
~                                                                               
~                                                                               
~                                                                               
:set number
</pre>

###### Output:
<pre>
      1 save this line and exit.
      2 I am doing practice of vi.
~                                                                               
~                                                                               
~                                                                               
~                        
:set number
</pre>
 

### 2-How to save work:
##### <b> < :w > </b>
This command is used to save work without exit.
##### For example:
###### Input:
<pre>
I am doing practice of vi.
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
"hello.txt" 0 line, 0 characters written
</pre>
  
###### Output:
<pre>
I am doing practice of vi.
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
"hello.txt" 1 line, 27 characters
</pre>
###### NOTE: Now you can see our work is save.
  
#### <b> < :wq > </b> 
This command is used to save work with exit.
##### For example:
###### Input:
<pre>
I am doing practice of vi.
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
:wq
</pre>
###### Output:
<pre> muhiamen@sysbox:~$ </pre>

##### <b> < :w! > </b> 
This command discard all changes, since the last save, and exit.
###### For  example:
###### Input:
<pre> 
Don't save this line. 
I am doing practice of vi.
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
:q!
</pre>

###### NOTE:
It will exit from the vi so again write the command of vi.
  
###### Output:
<pre>
I am doing practice of vi.
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
~                                                                                                                                             
"hello.txt" 1 line, 27 characters
</pre>

#### <b> < ZZ > </b> 
This command save the work without exit.
##### For example:
###### Input:
<pre> 
save this line and exit.
I am doing practice of vi.
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
ZZ
</pre>

###### Output:
<pre> muhiamen@sysbox:~$  </pre>
 

### How to move the cursor.

###### NOTE: 
Most people have use the navigation keys in vi, using these keys thay have different funtion in vi. Instead of navigation key these keys are used j, k, h, l - to move the cursor down, up, left and right (similar to the
arrow keys). These all keys work only in command mode.

#### <b> < h > </b> 
This key is used to move the cursor to left.
 
#### <b> < j > </b>
This key is used to move the cursor to the down line.
 
#### <b> < k > </b> 
This key is used to move the cursor to the up line.
 
#### <b> < l > </b>
This key is used to move the cursor the right.
 
#### <b> < 0 > </b>
This key is used to move to the start of the line.

#### <b> < $ > </b>
This key is used to move to the end of the current line.
 
#### <b> < nG > </b>
This key is used to move to the <b> n </b> th line (eg 5G moves to 5th line).
 
#### <b> < G > </b>
This key move to move to the last line.
 
#### <b> < nw > </b>
This key is used to move forward n word (eg 2w moves two words forwards). 
 
#### <b> < b > </b>
This key is used to move forward n word (eg 2w moves two words forwards). 
 
#### <b> < w > </b>
This key is used to move to the beginning of the next word.

#### <b> < nb > </b> 
This key is used to move back n word (eg 2b move two word back.

#### <b> < { > </b>
This key is used to move backward one paragraph.

#### <b> < } > </b> 
This key is used to move move forward one paragraph.


### How to delet content:

###### NOTE: 
These all command work in command mode.

#### <b> < x > </b> 
This key is used to delete a single character.
##### For example:
###### Input:
<pre>
save this line and exit.
I am doing practice of vdi
~                                                                               
~                                                                               
~                                                                               
~                                                                               
</pre>

###### Output:
<pre>
save this line and exit.
I am doing practice of vi
~                                                                               
~                                                                               
~                                                                               
~                                                                               

###### NOTE: 
shift+x delete the alphabet before the cursor, while the x delete the alphabet after the cursor.
</pre>

#### <b> < nx > </b>
This command is used to delete n characters (eg 5x deletes ﬁve characters)
##### For example:
###### Input:
<pre> 
      1 save this line and exit.
      2 I am doing practice of vi. 
~                                                                               
~                                                                               
~                                                                               
~                                                                               
</pre>

###### Output:
<pre>
      1 save this line and exit.
      2 I am doing 
~                                                                               
~                                                                               
~                                                                               
~                                                                               
</pre>

#### <b> < dd > </b>
Through command you can delete the current line.
##### For example:
###### Input:
<pre> 
      1 save this line and exit.
      2 I am doing practice of vi. 
~                                                                               
~                                                                               
~                                                                               
~                                                                               
</pre>

###### Output:
<pre>
      1 I am doing practice of vi.
      
~                                                                               
~                                                                               
~                                                                               
~                                                                               
</pre>


#### <b> < dnd > </b>
This command is used to delete multiple lines.
##### For example:
###### Input:
<pre>
      1 save this line and exit.
      2 I am doing practice of vi. 
      3 delete this line.
      4 and also this one. 
                                                                         
~                                                                               
~                                                                                                                                                            
~                                                                               
~                                                                  
</pre>

###### Output:
<pre> 
      1 save this line and exit.
      2 I am doing practice of vi. 
~                                                                               
~                                                                               
~                                                                               
~                                                                               
</pre>
### How to move or jump into the lines

#### <b>:n</b> 
This command is used to jump or move to the line n(eg :2 so it moves or jump into the line 2)

#### <b>:+n</b> 
This command is used to jump or move on n line(eg :+2 so it move or jump on 2 lines)

#### <b>:-n</b>
This command is used to jump or move back n line(eg :-3 so it will move or jump back 3 lines)

### How to find something:

#### <b> / <name> </b>
This command is used to find someword.
##### For example:
##### Input:
<pre>
      1 save this line and exit.
      2 I am doing practice of vi. 
~                                                                               
~                                                                               
~                                                                               
~                                                                               
/vi
</pre>

###### Output:
<pre>
      1 save this line and exit.
      2 I am doing practice of vi. 
~                                                                               
~                                                                               
~                                                                               
~                                                                               
search hit BOTTOM, continuing at TOP
</pre>

###### NOTE: 
The cursor will come to begining of that word.

#### <b> f<The first alphabet of the word> </b> 
This command is used to find the word.
##### For example:
###### NOTE: 
In command mode just hit the <b> f </b> and then hit the first alphabet and the cursor will go there if that is not that word for which you are looking for so simple hit the <b> n </b> it will go to the next word if that is also starting with the same alphabet, basiclly <b> n </b> means next. 

### Undoing:
#### <b> < u > </b> 
It undo the last changes. To undo the two last changes,you would type 2u.

#### <b> < U > </b> 
It undo all changes to the current line.

#### <b> < ctrl+r > </b>
To redo changes which were undone. In other words, undo the undos. Typically, known as redo. 


### How to copy and paste the line or word/words.

#### <b> < yy > </b> 
This commands is used to copy the current line.
#### <b> < p > </b> 
This command is used to paste the copy.
##### For example:
###### Input:
<pre> 
save this line and exit.
I am doing practice of vi. 
~                                                                               
~                                                                               
~                                                                               
</pre> 
###### NOTE: 
I have press yy for second line. It will copy the line after the cursor.

###### Output:
 <pre> 
 save this line and exit.
I am doing practice of vi. 
I am doing practice of vi. 
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
</pre>

#### <b> < dd > </b> 
This command is also used to cut the current line.
##### For example:
###### Input:
<pre>
save this line and exit.
I am doing practice of vi. 
cut this line and paste it again.                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
</pre>
 
###### Output:
<pre>
cut this line and paste it again.
save this line and exit.
I am doing practice of vi. 
~                                                                               
~                                                                               
~                                                                               
~                                                                               
</pre>

<#### <b> < v > </b> 
This command help us to copy or cut with this you can use the movement words (h,j,k,l).

<img src="https://github.com/amuhaiminshah/An-intro-to-vi-text-editor./blob/main/Example%20of%20vi.png" alt="The example of v command"> 

 
#### <b> < ndd > </b> 
Through this command you can cut or delete the multiple lines (eg: n show us the ratio of line). 

#### <b> < y$ > </b> 
This command is used to copy everything after the cursor upto end line.

#### <b> < y^ > </b> 
This command is used to copy everything before the cursor upto start line.

#### <b> < yiw > </b> 
This command is used to copy the current word.
 
#### <b> < yw > </b> 
Thsi command is used to copy the next word.

#### <b> < y% > </b> 
This command is used to copy the matching character, By default supported pairs are (), {}, and [].
 
#### <b> < d$ > </b> 
This command is used to cut everything after the cursor upto end line.
 
#### <b> < d^ > </b> 
This command is used to cut everything before the cursor upto start line.

<b>Vi/ex</b> is a very powerful editor. This document should have given you enough information to perform simple edits.  

##### Now it's time to acknowledge <a href="https://www.udemy.com/course/linux-command-line-zero-to-expert/?couponCode=PAST-STUDENTS-21-J" >Recluze</a> for has astonishing efforts who made me able to share these commands with you all.

##### If you have any problem in above commands first search it in google but still you have problem then you can mail me on <a href = "mailto: amuhaiminshah@gmail.com">Send Email</a>.

 
 
 
 
 


