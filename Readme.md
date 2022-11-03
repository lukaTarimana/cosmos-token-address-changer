This library is designed to convert cosmos token (bech32 type) addresses to hex and vice versa.

You can use any prefix and address, it will match bech32 address on blockchain node.

//INSTALLATION:

npm install bech32-converting

//USAGE:

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

//Example:

findOtherTokenAddress("cosmos18pr3pfggka859d38499tmsgm803u0sa9gpkwnf","cosmos", "osmo");

//returns: 

"osmo18pr3pfggka859d38499tmsgm803u0sa9q6979m"
