### Bash Array
#### An array can be define as the collections of a similar type of elements.In bash, There are no option for multi-dimensional arrays but yes bash provide the support of one-dimensional numerically indexed arrays.

### Bash Array Initialization
#### To initialize a Array in bash, we use assignment operator (=), by specifying the list of the elements within parentheses and separated by spaces like below:

''' ARRAY_NAME=(element_1st element_2nd-------- element_Nth) '''


### Access Elements of Array

'''echo ${ARRAY_NAME[2]} '''

### Basic Array Operations 
#### Once an array is initialized, we can perform many useful operations on it. We can display its keys and values as well as modify it by appending or removing the elements and many more:

### Reference Elements

#### To reference a single element of a array, we should  know the index value  of the element. We can print any element using the following syntax:


'''${ARRAY_NAME[index]}  '''

### Example -

'''
#!/bin/bash
#Script to print an element of an array with an index of 1

#Declaring the array
array1=( "Welcome""To""Shell" )

#printing the element with index of 1
echo ${array[1]}  '''

### Output

'''Javatpoint'''

### Printing the Keys of an Array

#### We can  print the keys used in indexed, instead of their respective values. It can be performed by adding the ! operator before the array name as below:

### syntax -- '''${!ARRAY_NAME[index]}  '''

### Example
'''
#!/bin/bash
#Script to print the keys of the array

#Declaring the Array
array2=( "Welcome""To""Shell" )

#Printing the Keys
echo "${!array[@]}" '''

### Output

'''0  1  2'''



### Finding Length of Array
#### We can count the number of elements contained in the array as below..

### Syntax-- '''${#ARRAY_NAME[@]}  '''
### Example

''' #!/bin/bash  
  
#Declaring the Array  
array3=( "Welcome""TO""the""Shell""Muzakkir")
  
#Printing Array Length  
echo "The array contains ${#array3@]} elements"  '''

### Output

'''The array contains 5 elements'''




### Adding Elements to an Array
#### We can  add elements to an indexed in array by specifying their index. To add the new element to an array in bash, we can use the following form:
### Syntax -- '''ARRAY_NAME[index_n]="New Element"'''

### Example

''' #!/bin/bash

#Declaring an array
array=( "Kotlin""Python""PHP""HTML""Ruby" )

#Adding new element
array[4]="JavaScript"

#Printing all the elements
echo "${array[@]}"   '''
### Output

''' Java Python PHP HTML JavaScript'''





### Updating Array Element
#### We have a option to update the array element by assigning a new value to the existing array by its index value. Let's change the array element at index 4 with an element 'Javatpoint'.

### Example
'''
#!/bin/bash
#Script to update array element

#Declaring the array
array=( "We""welcome""you""on")

#Updating the Array Element
array[4]=Javatpoint

#Printig all the elements of the Array
echo ${array[@]}'''

### Output

''' We welcome you on Javatpoint'''




### Deleting an Element from an Array

#### If we want to delete the element from the array, we have to know its index or key in case of an associative array. An element can be removed by using the 'unset' command:

### Syntax-- '''unset ARRAY_NAME[index]'''

### Example--
'''
#!/bin/bash
#Script to delete the element from the array

#Declaring the array
array=( "Java""Python""HTML""CSS""JavaScript" )

#Removing the element
unset array[1]

#Printing all the elements after deletion
echo "${array[@]}"'''

### Output

''' Java HTML CSS JavaScript'''
