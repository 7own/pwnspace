# Create, write, read file

## Create file

To create a new file in Python, use the `open()` method, with one of the following parameters:  
`"x"` - Create - will create a file, returns an error if the file exist  
`"a"` - Append - will create a file if the specified file does not exist  
`"w"` - Write - will create a file if the specified file does not exist

{% tabs %}
{% tab title="Python" %}
```python
# Create a new file with write permission (if it does not exist):
f = open("myfile.txt", "w")

# Create empty file called "myfile.txt":
f = open("myfile.txt", "x")
```
{% endtab %}
{% endtabs %}

### Write to an Existing File

{% tabs %}
{% tab title="Python" %}
```python
# Append to a file
f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()

# Overwrite content of a file
f = open("demofile3.txt", "w")
f.write("Woops! I have deleted the content!")
f.close()

# Open and read the file after the appending:
f = open("demofile2.txt", "r")
print(f.read())
```
{% endtab %}
{% endtabs %}

