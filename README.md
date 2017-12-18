# python-motebus

This is a python module to use the Motebus communication protocol.
To install this module, simply use pip install.

    pip install python-motebus

After installation, 

    import Motebus as motebus
  
To request a rpc function, use the function 
  
    motebus.send("MMA","FUNCTION","OBJECT_PARAMETER","PRIO","TIMEOUT1","TIMEOUT2")  
 
"MMA"               expect an string as "Appname"@"Domain" -for example-> "mote@ypcloud.com"
"FUNCTION"          expect an string as the function name in App
"OBJECT_PARAMETER"  expect an dictionary format of variable such as {"A":"12","B":"25"}
"PRIO"              expect an Interger to indicate the priority of request
"TIMEOUT1"          expect an Interger to indicate the time to retry
"TIMEOUT2"          expect an Interger to indicate the time to disconnect if not responsed

To receive a returned result, use the function
  
    return = motebus.response()

It will return a array which the result is stored in the order of the request sended.(first request sent will be stored at array[0],the second one will be stored at array[1]....etc)
If none of the request has finished yet, Interger -1 will be returned.





