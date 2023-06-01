# Huffman-Coding
## Aim
To implement Huffman coding to compress the data using Python.

## Software Required
1. Anaconda - Python 3.7

# Algorithm:
## Step 1:
Assign the input string.

## Step 2:
Create the required tree nodes.

## Step 3:
Create a function to implement the huffman coding.

## Step 4:
Calculate frequency of occurence.

## Step 5:
Print the characters and its Huffman code.
 
## Program:
```
Developed by : KRISHNA PRAKAASH D M
Registration Number : 212221230052
```
Create the input String
```
string = 'string='KRISHNA_212221230052''
```
Create tree nodes
```
class Nodetree(object):
    def __init__(self,left=None,right=None):
        self.left= left
        self.right =right
    def children(self):
        return(self.left, self.right) 
  ```
  Main function to implement huffman coding
```
def huffman_coding(Tree,left =True,binString=''):
    if type(Tree) is str:
        return {Tree : binString}
    (l, r) = Tree.children()
    d = dict()
    d.update(huffman_coding(l,True,binString+ '0'))
    d.update(huffman_coding(r,False,binString+ '1'))
    return d


```
Calculate frequency of occurrence
```
nodes = freq
while len(nodes) >1:
    (key1 , value1 ) = nodes[-1]
    (key2 , value2 ) = nodes[-2]
    nodes = nodes[:-2]
    Tree = Nodetree(key1,key2)
    nodes.append((Tree , value1+value2))
    nodes = sorted(nodes, key =lambda x:x[1],reverse =True)

```
Print the characters and its huffmancode
```
huffman = huffman_coding(nodes[0][0])
print('character | Huffman code')
print('-------------------------')
for (char , frequency) in freq:
    print(' %-4r | %12s ' %(char, huffman[char]))

```


    
## Output:
![OP-01](https://github.com/Krishna-Prakaash/Huffman-Coding/assets/93427144/4a2b6a75-7969-458b-adc0-5f610cfaa7d5)





## Result
Thus the huffman coding was implemented to compress the data using python programming.
