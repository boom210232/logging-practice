## Logging Practice

1. Copy this repo to a public repository in your own Github account named `logging-practice`.
2. Perform the exercises described here <https://cpske.github.io/ISP/logging/logging-practice>.
3. Push your final code to Github.              

## Code's describe        

### Basic config.
Run the code with only a call to basicConfig() in main (default configuration).       
Notice the logging output format.
``` 
WARNING:root:You're redirect to unknown website. Please turn back to menu.
Level 35:root:Your transaction fail to transfer dogecoin to wallet.
ERROR:root:Failed to login by user 'B.Clinton'. 
CRITICAL:root:Cannot open this file: Unknown format 
CRITICAL:root:Anonymous user delete database data.

Process finished with exit code 0
```         
What is lowest severity log message that is printed?          
```
The lowest warning is "WARNING" level.
```          
Which of your log messages are not printed?          
``` 
Debug and info level are not display in basic config.
```    

### Simple config
The result:
``` 
2021-11-04 09:35:21,514 root WARNING: You're redirect to unknown website. Please turn back to menu.
2021-11-04 09:35:21,514 root Level 35: Your transaction fail to transfer dogecoin to wallet.
2021-11-04 09:35:21,514 root ERROR: Failed to login by user 'B.Clinton'. 
2021-11-04 09:35:21,514 root CRITICAL: Cannot open this file: Unknown format 
2021-11-04 09:35:21,514 root CRITICAL: Anonymous user delete database data.

``` 
How does the log message format change?
```  
The logging include date and time but still have same warning level appear as basicConfig()
```

### My config
The result will written in logging_data.txt for my logging.        
In task NO.5 for second time.
``` 
Logging doesn't overwrite but continues save logging below former.
```

In task No.6.         
``` 
# With: filemode='w', The logging output will truncate and write a new one instead.
# logging.basicConfig(format=FORMAT, level=logging.DEBUG, filename="logging_data.txt", filemode='w')

# With: filemode='a', Normal way like default also same like No.5 task.
logging.basicConfig(format=FORMAT, level=logging.DEBUG, filename="logging_data.txt", filemode='a')
```

