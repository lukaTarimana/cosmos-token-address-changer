This library (bech32-converting) is designed to convert bech32 addresses to hex and vice versa.

You can use any prefix and address, it will match bech32 address on blockchain node.

Here is a function which will help you to convert one Cosmos blockchain token address to other. 

//INSTALLATION:
```bash
npm install bech32-converting
```
//USAGE:
```Javascript
import converter from "bech32-converting";

const findOtherTokenAddress = (
  currentTokenaddress, 
  currentTokenName,
  newTokenName 
) => {
  let currentTokenaddressHex =
    converter(currentTokenName).toHex(currentTokenaddress);
  return converter(newTokenName).toBech32(currentTokenaddressHex);
};
```
//Example:
```Javascript
findOtherTokenAddress("cosmos18pr3pfggka859d38499tmsgm803u0sa9gpkwnf","cosmos", "osmo");

```
//returns: 

"osmo18pr3pfggka859d38499tmsgm803u0sa9q6979m"
