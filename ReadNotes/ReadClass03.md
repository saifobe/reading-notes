# Reading and Writing Files in Python

## What Is a File?

A file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.

## most modern file systems are composed of three main parts:

1- Header: metadata about the contents of the file (file name, size, type, and so on)
2- Data: contents of the file as written by the creator or editor
3- End of file (EOF): special character that indicates the end of the file

## File Paths
When you access a file on an operating system, a file path is required. The file path is a string that represents the location of a file. It’s broken up into three major parts:

1- Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)
2- File Name: the actual name of the file
3- Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

# Opening and Closing a File in Python
the first thing to do is to open a file. This is done by invoking the open() built-in function. open() has a single required argument that is the path to the file. open() has a single return, the file object:

Ex) file = open('dog_breeds.txt')

### After you open a file, the next thing to learn is how to close it.
It’s important to remember that it’s your responsibility to close the file. In most cases, upon termination of an application or script, a file will be closed eventually. However, there is no guarantee when exactly that will happen. This can lead to unwanted behavior including resource leaks. It’s also a best practice within Python (Pythonic) to make sure that your code behaves in a way that is well defined and reduces any unwanted behavior.

Ex)
 reader = open('dog_breeds.txt') 


try:


    # Further file processing goes here
finally:


    reader.close()

### The second way to close a file is to use the with statement:

Ex)  with open('dog_breeds.txt') as reader:


    # Further file processing goes here

### OR you can use :
Ex) with open('dog_breeds.txt', 'r') as reader:

    # Further file processing goes here

#

| Character   | Meaning |
| ----------- | ----------- |
|    'r'      | Open for reading (default)     |
|    'w'      | Open for writing, truncating (overwriting) the file first       |
|    'rb' or 'wb'      | Open in binary mode (read/write using byte data)    |


# Reading Opened Files
Once you’ve opened up a file, you’ll want to read or write to the file. First off, let’s cover reading a file. There are multiple methods that can be called on a file object to help you out:

## .read(size=-1)
This reads from the file based on the number of size bytes. If no argument is passed or None or -1 is passed, then the entire file is read.

## .readline(size=-1)
This reads at most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or rest of the line) is read.

## .readlines() 
This reads the remaining lines from the file object and returns them as a list.

Ex)
> with open('dog_breeds.txt', 'r') as reader:

>     # Read & print the entire file
>    print(reader.read())

Ex )

> with open('dog_breeds.txt', 'r') as reader:

>     #Read & print the first 5 characters of the line 5 times

>     print(reader.readline(5))
>     # Notice that line is greater than the 5 chars and continues

>     # down the line, reading 5 chars each time until the end of the

>     # line and then "wraps" around
>     print(reader.readline(5))
>     print(reader.readline(5))
>     print(reader.readline(5))
>     print(reader.readline(5))

# Writing on Opened Files
writing files. As with reading files, file objects have multiple methods that are useful for writing to a file:

## .write(string)
This writes the string to the file.

## .writelines(seq)
This writes the sequence to the file. No line endings are appended to each sequence item. It’s up to you to add the appropriate line ending(s).

Ex)

with open('dog_breeds_reversed.txt', 'w') as writer:

    # Alternatively you could use
    # writer.writelines(reversed(dog_breeds))

    # Write the dog breeds to the file in reversed order
    for breed in reversed(dog_breeds):
        writer.write(breed)

#
https://github.com/saifobe/reading-notes/blob/main/ReadNotes/ReadClass03.md 

    