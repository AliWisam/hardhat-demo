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
### Step15 - For knowledge sake, just type in   console.log("My Awesome Console.log") statement in the constructor. The actual purpose of the console.log                    -  statement is to 
###        - show the action being performed. Even if we remove the console.log statements in the contracts/Greeter.sol, the tests shall pass. They just maintain ###        -  the logs.
### Step16 - Let us deploy the contract - follow the lines 8-24 in scripts/sample-scripts.js. We call the main function asynchronously and if successful no 
###        - process is pending i.e. process.exit(0) and if there is an error, process.exit(1) is returned i.e. Uncaught fatal expectation. So type in terminal
###        - npx hardhat run scripts/sample-scripts.js
### Step17 - Connecting a wallet or Dapp to Hardhat Network- By default hardhat runs in an im-memory instance of Hardhat Network on startup by default.
###        - To run Hardhat Network in a standalone function, in order to let external clients(MetaMask, Dapp frontend or a script) connect to it, type 
###        - in terminal npx hardhat node- this will expose a JSON-RPC interface to Hardhat Network- To use it connect your wallet or dapp to 
###        - https://localhost:8545. Now rerun the sample sample script using the network option.
###        - npx hardhat run scripts/sample-script.js --network localhost
###        - What we have done here is the creation of a project, completion of a Hardhat task, and compilation of a smart contract.
### Step18 - Now open the metamask wallet- connect to localhost 8545 - import the private key for account[0] - 
### Step19 - Type in terminal - npx hardhat console --network localhost 
### Step20 - Type in node- const Greeter = await hre.ethers.getContractFactory("Greeter"); 
### Step21 - Then type in node-   const greeter = await Greeter.deploy("Hello, Hardhat!");
### Step22 - Then type this- await greeter.deployed();
### Step23 - Then typing greeter.address shall give the address. 
### Step24 - Then if we type in the same node env  -     await greeter.setGreeting("Hola, mundo!"); => we will see that the contract call is setGreeting and 
###        - contract is called,there will be Transaction Id, from, to, gas used, block# log statement "Changing greeting from 'Hello, Hardhat!' to 'Hola, mundo!' 
### Step25 - node env => await greeter.greet() => 'Hola, mundo!'
### Step26 - .exit
