# DegenGamingToken Smart Contract
The DegenGamingToken is a custom ERC20 token named "Aastha" created using the OpenZeppelin library. This contract includes functionalities for minting, burning, and redeeming tokens, with a unique feature of a reward pool.

# Contract Details
Dependencies
This contract imports the following from the OpenZeppelin library:
ERC20 from @openzeppelin/contracts/token/ERC20/ERC20.sol
Ownable from @openzeppelin/contracts/access/Ownable.sol
# State Variables
rewardPool: A uint256 variable that stores the amount available in the reward pool.
# Constructor
The constructor initializes the contract with the following parameters:

initialSupply: The initial supply of tokens to be minted.
initialOwner: The owner of the contract.
The constructor mints the initialSupply of tokens to the deployer and sets the rewardPool to 10,000 tokens.

# Functions
# createTokens
Mints new tokens and assigns them to the specified address. This function can only be called by the contract owner.

# claimReward
Allows users to redeem tokens from the reward pool. The function checks if the caller has a sufficient balance to claim the reward and if the reward pool is available. It transfers the claimed amount to the owner and reduces the reward pool by 10% after each claim.

# destroyTokens
Allows users to burn a specified amount of their tokens, reducing the total supply.

# getBalance
Returns the token balance of the specified account.

# Events
# RewardClaimed
Emitted when a user claims a reward from the reward pool.
