Lateral file joiner is basic Java class that allows for concatenation of two files vertically, 
rather than horizontally.

Functions and Arguments

Constructor
```
FileCat(String file1, String file2);
FileCat(String file1, String file2);
```

LateralOp
	Function used to concatenate two files vertically, Returns string of file name created.

```
String LateralOp();
String LateralOp(String name);
```


Explanations:


The way it's used is incredibly simple, simple make a new instantiation of FileCat with the names
of the two files you'd like to concatenate. Then use the command LateralOp() on your FileCat 
object, and your new file will be created. 

```
FileCat fc = new FileCat("file1.txt", "file2.txt");
fc.LateralOp();
```

LateralOp will autogenerate a new file name with the name 
```
output + [numDefaultFilesCreated] + [defaultExtension]
```

One also has the option of keeping the default file name, by adding an extension as a third 
argument in the constructor. Just keep in mind, this program is only simple enough at the moment to
create text files, so the extension is merely superficial at this point.

```
FileCat fc = new FileCat("file1.txt", "file2.txt", "pdf");
fc.LateralOp();
```

The user also has the option of circumventing the default naming scheme altogether by using the
overloaded lateralOp function.
```
fc.LateralOp("customOutput.txt");
```
Which will output a customOutput.txt as the file name.