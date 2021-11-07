# Basic Sample Hardhat Project

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, a sample script that deploys that contract, and an example of a task implementation, which simply lists the available accounts.

Try running some of the following tasks:

```shell
npx hardhat accounts
npx hardhat compile
npx hardhat clean
npx hardhat test
npx hardhat node
node scripts/sample-script.js
npx hardhat help
```
# hardhat

### Step01 - Initiate packagejson in an empty folder designed for setting up the hardhat environment.
### Step02 - Add hardhat devDependency   by typing in the terminal  npm install --save-dev hardhat
### Step03 - Type npx hardhat in the terminal.
### Step04 - Hardhat shall ask you to what you to do - For the demo - select  Create a basic sample project.
### Step05 - For the Hardhat project root- it is recommended to go with the flow.
### Step06 - Add .gitignore.
### Step07 - Type y for the dependencies query from hardhat.
### Step08 - Go to the editor and have a peek at the files.
### Step09 - Go back to the directory terminal and type npx hardhat and you shall find the list of available tasks and their purpose/functionality.
### Step10 - Now if you type npx hardhat accounts, hardhat shall provide you all the 20 accounts, Likewise npx hardhat test runs the test and so on.
### Step11 - You can add your own task in the hardhat.config.js. In this case, We shall add a task foobar and verify it by npx hardhat   and  npx hardhat foobar.
### Step12 - Now type npx hardhat compile in the terminal and hardhat shall download the solidity compiler and compile the 2 files in contracts/Greeter.sol.
###        - Therein, you shall find Greeter.json wherein the abi(application binary interface) and the bytecode reside.
### Step13 - Let us see the test-the test is similar to truffle- it shall describe greeter and should return the new greeting once its changed, const Greeter
###        - awaits ethers.getContractFactor("Greeter") and const greeter deploys the instance of the greeter. Then we get the deployed copy and it expects 
###        - the return value equal to Hello, world!. Then we change the greeting to Hola, mundo! and then expect the same to be equal Hola, mundo!.
### Step14 - Now just run the test - npx hardhat test - And it shall pass i.e. Should return the new greeting once it's changed.
### Step15 - For knowledge sake, just type in   console.log("My Awesome Console.log") statement in the constructor. The actual purpose of the console.log statement is to 
###        - show the action being performed. Even if we remove the console.log statements in the contracts/Greeter.sol, the tests shall pass. They just maintain the logs.
### Step16 - Let us deploy the 
