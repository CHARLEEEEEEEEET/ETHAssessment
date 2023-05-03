# ETHAssessment

A Final Assessment for the subject ITELEC 1 for the course Bachelor of Science in Information Technology. This assessment includes the code of the program and also a video recording to watch.

## Description

This is a Solidity smart contract that creates a custom token and allows for the minting and burning of tokens. It includes public variables that store information about the token and a mapping that links addresses to their corresponding token balances. The "mint" function increases the total token supply and adds tokens to the balance of the specified address, while the "burn" function decreases the total supply and the balance of the specified address. The "burn" function includes checks to ensure that the address has sufficient tokens to perform the burn.

## Getting Started

### Installing

* Go to this website:  https://remix.ethereum.org/
* Copy this code and paste it to the website abovementioned
* Click this Loom link for your reference: https://www.loom.com/share/18adb7fbf79147439d38fb69acad0d40

### Executing program

* Click the Solidity Panel located at the left side panel of the compiler and click the checkbox "Auto compile"
* Click the Deploy & Run Transactions and copy the Account
* Click the dropdown "Deployed Contracts" and choose the Account deployed
* Paste the account to Mint Address and enter value that is not exceeding to "3000000" then click "Transact"
* Paste the account to Balance and enter value that is not exceeding to "3000000" then click "Transact"
* Click "Balances" to see if the number of value was successfully executed
* Click "totalSupply" to see if the number of value was successfully executed
* If the value did not subtracted from mint, pllease go to Help Panel
* Check if the execution output has a green check to prove that it was executed successfully
```
pragma solidity 0.8.18;


contract MyToken {

    string public tokenName = "Haven";
    string public tokenAbbrv = "hvn";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;


    function mint (address _address, uint _value) public{
        totalSupply += _value;
        balances [_address] += _value;
    }

    function burn (address _address, uint _value) public{
        if (balances[_address] >=_value) {

        totalSupply -= _value;
        balances [_address] -= _value;
    }

}
}
```

## Help

Any advise for common problems or issues.
```
// Make sure that the burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
to the amount that is supposed to be burned.
```

## Authors

Student: Frence Charl D. Postrado
Email: 8215191@ntc.edu.ph
Contact Number: 090895194259

## Loom Link

https://www.loom.com/share/18adb7fbf79147439d38fb69acad0d40

## License

This project is licensed under the Frence Charl D. Postrado License - see the LICENSE.md file for details
