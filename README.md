<h1>Use Python Algorithm to Update a File Demonstration<h1>


<h2>Description</h2>
In this exercise, my organizations access to restricted content is controlled with an allow list of IP addresses. 

The "allow_list.txt" file identifies these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this content. 

I created an algorithm to automate updating the "allow_list.txt" file and remove these IP addresses that should no longer have access. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 


<h2>Environments Used </h2>

- <b>Mac OS</b> 

<h2>Exercise Walk-Through:</h2>

For the first part of the algorithm, I opened the "allow_list.txt" file. 

         I assigned this file a name as a string to the import_file variable:
<br />
<br />
  <p align="center">  <img width="500" alt="image" src="https://github.com/Hberg007/UpdateFileThoughPythonDemo/assets/168477827/dbaed89e-8f14-4343-9a2d-032a550266b2">
<br />
<br />

         Then, I used a (with) statement to open the file:
<br />
<br />
  <p align="center">  <img width="700" alt="image" src="https://github.com/Hberg007/UpdateFileThoughPythonDemo/assets/168477827/949aba45-8d69-49d3-a093-72dde6c3b8ed">
<br />
<br />   
    
    In my algorithm, the with statement is used with the .open() function in read mode to open the allow list file 
    
    for the purpose of reading it. 
    
    The purpose of opening the file is to allow me to access the IP addresses stored in the allow list file. 
    
    The with keyword will help manage the resources by closing the file after exiting the with statement. 
    
    In the code with open(import_file, "r") as file:, the open() function has two parameters. 
    
    The first identifies the file to import, and then the second indicates what I want to do with the file. 
    
    In this case, "r" indicates that I want to read it. 
    
    The code also uses the as keyword to assign a variable named file; file stores the output of the .open() function while 
    
    I work within the with statement.

    
<br/>
<br />
<h2> Read the File Contents:</h2>
<br />
<br />
        In order to read the file contents, I used the .read() method to convert it into the string.
<br />
<br />
  <p align="center">  <img width="800" alt="image" src="https://github.com/Hberg007/UpdateFileThoughPythonDemo/assets/168477827/7b3b2d5c-7d63-4ba0-96b6-7b774ccebeb3">
<br />
<br />       

      When using an .open() function that includes the argument "r" for “read,” I can call the .read() function in the 
      
      body of the with statement. 
      
      The .read() method converts the file into a string and allows me to read it. 
      
      I applied the .read() method to the file variable identified in the with statement. 
      
      Then, I assigned the string output of this method to the variable ip_addresses. 

      In summary, this code reads the contents of the "allow_list.txt" file into a string format that allows me to later use 
      
      the string to organize and extract data in my Python program.
<br />
<br />
<h2> Convert the String Into a List:</h2>
<br />
<br />
In order to remove individual IP addresses from the allow list, I needed it to be in list format. 

         Therefore, I next used the .split() method to convert the ip_addresses string into a list:

<br />
<br />
 <p align="center"> <img width="700" alt="image" src="https://github.com/Hberg007/UpdateFileThoughPythonDemo/assets/168477827/ff031f8e-26a7-4e6b-851c-5c0bc5c3769e">
<br />
<br />

     The .split() function is called by appending it to a string variable. It works by converting the contents 
     
     of a string to a list. 
    
     The purpose of splitting ip_addresses into a list is to make it easier to remove IP addresses from the allow list. 
    
     By default, the .split() function splits the text by whitespace into list elements. 
     
     In this algorithm, the .split() function takes the data stored in the variable ip_addresses, which is a string of 
     
     IP addresses that are each separated by a whitespace, and it converts this string into a list of IP addresses. 
     
     To store this list, I reassigned it back to the variable ip_addresses. 

<br />
<br />
<h2> Iterate Through the Remove List:</h2>
<br />
<br />
A key part of my algorithm involves iterating through the IP addresses that are elements in the remove_list. 
<br />
<br />
To do this, I incorporated a for loop:
<br />
<br />
 <p align="center"> <img width="500" alt="image" src="https://github.com/Hberg007/UpdateFileThoughPythonDemo/assets/168477827/81666e19-3ace-442c-b9c2-3e17eee0533f">
<br />
<br />

The for loop in Python repeats code for a specified sequence. 
   
     
      The overall purpose of the for loop in a Python algorithm like this is to apply specific code statements to all elements in a sequence. 
      
      The for keyword starts the for loop. It is followed by the loop variable element and the keyword in. 
      
      The keyword in indicates to iterate through the sequence ip_addresses and assign each value to the loop variable element. 
<br />
<br />
<h2> Remove IP Addresses That are on the Remove List:</h2>
<br />
<br />
My algorithm requires removing any IP address from the allow list, ip_addresses, that is also contained in remove_list.  

Because there were not any duplicates in ip_addresses, I was able to use the following code to do this:
<br />
<br />
 <p align="center"> <img width="600" alt="image" src="https://github.com/Hberg007/UpdateFileThoughPythonDemo/assets/168477827/2ad35f62-31dc-4680-8e9d-17347c5edb20">
<br />
<br />
       First, within my for loop, I created a conditional that evaluated whether or not the loop variable element was found in the ip_addresses list. 
   
       I did this because applying .remove() to elements that were not found in ip_addresses would result in an error. 

       Then, within that conditional, I applied .remove() to ip_addresses. I passed in the loop variable element as the argument so that each 
       
       IP address that was in the remove_list would be removed from ip_addresses.

<br />
<br />
<h2> Update the File with the Revised List of IP Addresses:</h2>
<br />
<br />
As a final step in my algorithm, I needed to update the allow list file with the revised list of IP addresses. 

        To do so, I first needed to convert the list back into a string. I used the .join() method for this:
<br />
<br />
 <p align="center"> <img width="700" alt="image" src="https://github.com/Hberg007/UpdateFileThoughPythonDemo/assets/168477827/8606b3e6-baf0-4ae2-940d-c6455c649adb">
<br />
<br />
       
        The .join() method combines all items in an iterable into a string. 
   
        The .join() method is applied to a string containing characters that will separate the elements in the iterable once joined into a string. 
        
        In this algorithm, I used the .join() method to create a string from the list ip_addresses so that I could pass it in as an argument to 
        
        the .write() method when writing to the file "allow_list.txt". 
        
        I used the string ("\n") as the separator to instruct Python to place each element on a new line. 
<br />
<br />
        Then, I used another with statement and the .write() method to update the file:
<br />
<br />
 <p align="center"> <img width="600" alt="image" src="https://github.com/Hberg007/UpdateFileThoughPythonDemo/assets/168477827/0e7d4f76-8b5b-4f2f-ac5d-4aff6638af60">
<br />
<br />        

        This time, I used a second argument of "w" with the open() function in my with statement. 
        
        This argument indicates that I want to open a file to write over its contents. 
        
        When using this argument "w", I can call the .write() function in the body of the with statement. 
        
        The .write() function writes string data to a specified file and replaces any existing file content. 
<br />
<br />         

        In this case I wanted to write the updated allow list as a string to the file "allow_list.txt". 
        
        This way, the restricted content will no longer be accessible to any IP addresses that were removed from the allow list. 
        
        To rewrite the file, I appended the .write() function to the file object file that I identified in the with statement. 
        
        I passed in the ip_addresses variable as the argument to specify that the contents of the file specified in the with statement should 
        
        be replaced with the data in this variable.
<br />
<br />
<h2> Summary:
<br />
<br />

I created an algorithm that removes IP addresses identified in a remove_list variable from the "allow_list.txt" file of approved IP addresses. This algorithm involved opening the file, converting it to a string to be read, and then converting this string to a list stored in the variable ip_addresses. I then iterated through the IP addresses in remove_list. 

With each iteration, I evaluated if the element was part of the ip_addresses list. If it was, I applied the .remove() method to it to remove the element from ip_addresses.
After this, I used the .join() method to convert the ip_addresses back into a string so that I could write over the contents of the "allow_list.txt" file with the revised list of IP addresses.

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
