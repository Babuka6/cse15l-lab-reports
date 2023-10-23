_Anthony Chapov, CSE15L, Lab Report #1_

Part 1:
A.
  1. Method: .handleRequest()     Argument: https://0-0-0-0-4000-1kkqb3735755l4n6pe73ttd4v0.us.edusercontent.com/add-message?s=m, return "m"
  2. Method: .getPath.containts() Argument: "/add-message"
  3. Method: .getQuerry.split()   Argument "="
  4. Method: .equals()            Argument "s"
  5. parameters[0] = "s"
  6. parameters[1] = "m"
  7. current = "m"
  
B.
  1. Method: .handleRequest()     Argument: https://0-0-0-0-4000-1kkqb3735755l4n6pe73ttd4v0.us.edusercontent.com/add-message?s=mother_russia, return "1. m \n 2. mother_russia"
  2. Method: .getPath.containts() Argument: "/add-message"
  3. Method: .getQuerry.split()   Argument "="
  4. Method: .equals()            Argument "s"
  5. parameters[0] = "s"
  6. parameters[1] = "mother_russia"
  7. current = "1. m + \n + 2. mother_russia"

Explanation: 
The only values that change are:
 1. handleRequest's argument since url changes
 2. parameters[1] changes because url adress changes. 
 3. The rest of arguments and fields stay the same. 
 4. current is updated accordingly. 

 Part 2: 


 Part 3. 
 I learned that we can communicate directly with the remote server via the terminal. It was also interesting to learn that we can run server on the same remote UCSD computer, which can be thought of as a server on the server (since, in my understanding, ucsd computer is a server itself). It was also fun to learn more about the encryption concept that underlines use of two private and public keys: one for chiper and the other one for decipher.  
 

