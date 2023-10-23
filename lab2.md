_Anthony Chapov, CSE15L, Lab Report #1_

Part 1:
A.
  Method: .handleRequest()     Argument: https://0-0-0-0-4000-1kkqb3735755l4n6pe73ttd4v0.us.edusercontent.com/add-message?s=m, return "m"
  Method: .getPath.containts() Argument: "/add-message"
  Method: .getQuerry.split()   Argument "="
  Method: .equals()            Argument "s"
  parameters[0] = "s"
  parameters[1] = "m"
  current = "m"
  
B.
  Method: .handleRequest()     Argument: https://0-0-0-0-4000-1kkqb3735755l4n6pe73ttd4v0.us.edusercontent.com/add-message?s=mother_russia, return "1. m \n 2. mother_russia"
  Method: .getPath.containts() Argument: "/add-message"
  Method: .getQuerry.split()   Argument "="
  Method: .equals()            Argument "s"
  parameters[0] = "s"
  parameters[1] = "mother_russia"
  current = "1. m + \n + 2. mother_russia"

Explanation: 
The only values that change are:
 1)handleRequest's argument since url changes
 2)parameters[1] changes because url adress changes. 
 3)The rest of arguments and fields stay the same. 
 4)current is updated accordingly. 

 Part 2: 
 

