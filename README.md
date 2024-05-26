# MetaCrafters-ETH-Proof_beginner
All the requirements are met in the file solidity_assesment.sol file.

1) All the variables are creacted as required. 3 variables are created i.e. two strings and a unsigned integer.
```
 string public tokenName = "META";
 string public tokenAbbrv = "MTA";
 uint256 public totalSupply = 0;
```
2) A mapping named balances was created. a mapping from address to integer was created to map the addresses with their current account.
```
 mapping (address=>uint) public balances;
```
3) mint function is also created to perform transations as per the given condition. mint function implement by modifying the varibles declared in above steps. mint function: - increments the value of total supply and balance in an account. 
```
    function mint(address _address,uint _value)public{
        totalSupply += _value;
        balances[_address] += _value;
    }
```

4) burn function is also created to perform transations as per the given condition ,burn function implement by modifying the varibles declared in above steps. burn function: - burns or decrementes the value in a particularaccount
```
 function burn (address _address,uint _value)public {
        if (balances[_address]>=_value) {
            
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
```
5) Conditionals are also included in the burn function to ensure that the sender's balance is greater than or equal to the amount to be burned.
```
if (balances[_address]>=_value) {
            
            totalSupply -= _value;
            balances[_address] -= _value;
        }
```
