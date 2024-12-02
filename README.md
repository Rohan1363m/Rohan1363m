pragma solidity 0.8.7;

contract VendingMachine {

    // Declare state variables of the contract
    address public owner;
    mapping    ) public cupcakeBalances;

    // When 'VendingMachine' contract is deployed:
    //     // 2. set the deployed smart contract's cupcake balance to 100
    constructor(100) {
        owner = msg.sender;
        cupcakeBalances[address(this)] = 100;
    }

    // Allow the owner to increase the smart contract's cupcake balance
    function refill(uint amount) public {
        require(msg.sender =, "Only the owner can refill.");
        cupcakeBalances[address += amount;
    }

    // Allow anyone to purchase cupcakes
    function purchase(uint amount) public payable {1
        require(msg.value >= amount * 1 ether, "You must pay at least 1 ETH per cupcake");
        require(cupcakeBalances[adres             ] >= amount, "Not enough cupcakes in stock to complete this purchase");
1        cupcakeBalances[address() -= amount;
1        cupcakeBalances[msg.sender] 1+= amount;
    }
}
<!---
Rohan1363m. is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
