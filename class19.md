# Reading class 19

## Python Regular Expressions Tutorial [link](https://www.datacamp.com/tutorial/python-regular-expression-tutorial)

**How can you use regular expressions in Python to search for specific patterns in a string, and what is the primary library to work with them?**

Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. If you've ever used search engines, search and replace tools of word processors and text editors - you've already seen regular expressions in use. They are used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining.

In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import:

```python
import re
```

The re library in Python provides several functions that make it a skill worth mastering. These include:

- **re.match()** - Determine if the RE matches at the beginning of the string.

- **re.search()** - Scan through a string, looking for any location where this RE matches.

- **re.findall()** - Find all substrings where the RE matches, and returns them as a list.

- **re.split()** - Split the string into a list, splitting it wherever the RE matches.

- **re.sub()** - Find all substrings where the RE matches, and replace them with a different string.

------------------

## Shutil [link](https://pymotw.com/3/shutil/)

**What is the purpose of the shutil library in Python, and provide an example of a common use case for file or directory management with this library?**

The shutil (shell utilities) library in Python provides a high-level interface for file and directory operations. It offers functions to efficiently perform tasks such as copying, moving, renaming, and deleting files or directories.

Here's an example of a common use case for file or directory management with the shutil library:

Let's say you have a directory containing multiple files, and you want to create a backup of that directory by copying its contents to a new location.

```python
import shutil

# Source directory
source_directory = '/path/to/source_directory'

# Destination directory for backup
backup_directory = '/path/to/backup_directory'

# Create a backup by copying the contents of the source directory to the backup directory
shutil.copytree(source_directory, backup_directory)
```

In this example, the shutil.copytree() function is used to recursively copy the entire directory tree from the source directory to the backup directory. It preserves the directory structure and copies all files and subdirectories.

The shutil library provides other useful functions as well. Here are a few notable ones:

shutil.copy(src, dst): Copies a file from the source path to the destination path.
shutil.move(src, dst): Moves a file or directory from the source path to the destination path.
shutil.rmtree(path): Deletes a directory and its contents recursively.
shutil.make_archive(base_name, format, root_dir): Creates an archive (e.g., ZIP or TAR) containing the files and directories under the root directory.

------------------

## Automation [link](https://www.youtube.com/watch?v=qbW6FRbaSl0&t=69s)

**Explain one automation idea from the assigned material and describe how it can be implemented using Python’s regular expressions and shutil libraries.?**

One automation idea from the assigned material is to organize a messy directory containing various files into separate folders based on their file types. This can be implemented using Python's regular expressions and shutil libraries.

Here's a step-by-step explanation of how this automation idea can be implemented:

1. Identify the file types: Determine the different file types present in the directory. For example, you might have files with extensions like .txt, .jpg, .pdf, etc.

2. Use regular expressions to match file types: Create regular expressions to match specific file types based on their extensions. For example, \.txt$ matches files with a .txt extension.

3. Iterate through the files in the directory: Use the os module to iterate through the files in the target directory.

4. Match file types using regular expressions: For each file, use regular expressions to match its file type based on the file extension. This can be done using the re module and its re.search() function.

5. Create destination folders: Based on the identified file types, create separate destination folders for each file type. For example, you might create folders named "Text Files," "Image Files," "PDFs," etc.

6. Use shutil to move files: Use the shutil.move() function to move the files to their respective destination folders. The source path would be the current file's path, and the destination path would be the appropriate folder path based on the file type.

By combining regular expressions and the shutil library, this automation idea allows you to efficiently organize files in a directory based on their types. The regular expressions help in identifying the file types based on their extensions, while the shutil library simplifies the process of moving files to their designated folders.
