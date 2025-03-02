# StableAsset

*Nuts Finance Developer*

> StableAsset swap

The StableAsset pool provides a way to swap between different tokens

*The StableAsset contract allows users to trade between different tokens, with prices determined algorithmically based on the current supply and demand of each token*

## Methods

### FEE_DENOMINATOR

```solidity
function FEE_DENOMINATOR() external view returns (uint256)
```



*This is the denominator used for calculating transaction fees in the StableAsset contract.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### MAX_A

```solidity
function MAX_A() external view returns (uint256)
```



*This is the maximum value of the amplification coefficient A.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### acceptGovernance

```solidity
function acceptGovernance() external nonpayable
```



*Accept the govenance address.*


### admins

```solidity
function admins(address) external view returns (bool)
```



*This is a mapping of accounts that have administrative privileges over the StableAsset contract.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### balances

```solidity
function balances(uint256) external view returns (uint256)
```



*This is an array of uint256 values representing the current balances of each token in the StableAsset contract. The balances are converted to the standard token unit (10 ** 18).*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### exchangeRateProvider

```solidity
function exchangeRateProvider() external view returns (contract IExchangeRateProvider)
```



*Exchange rate provider for token at exchangeRateTokenIndex.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | contract IExchangeRateProvider | undefined |

### exchangeRateTokenIndex

```solidity
function exchangeRateTokenIndex() external view returns (uint256)
```



*Index of tokens array for IExchangeRateProvider.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### feeErrorMargin

```solidity
function feeErrorMargin() external view returns (uint256)
```



*Fee error margin.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### futureA

```solidity
function futureA() external view returns (uint256)
```



*These is a state variables that represents the future amplification coefficient A.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### futureABlock

```solidity
function futureABlock() external view returns (uint256)
```



*These is a state variables that represents the future block number when A is set.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### getA

```solidity
function getA() external view returns (uint256)
```



*Returns the current value of A. This method might be updated in the future.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | The current value of A. |

### getMintAmount

```solidity
function getMintAmount(uint256[] _amounts) external view returns (uint256, uint256)
```



*Compute the amount of pool token that can be minted.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _amounts | uint256[] | Unconverted token balances. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | The amount of pool tokens to be minted. |
| _1 | uint256 | The amount of fees charged. |

### getRedeemMultiAmount

```solidity
function getRedeemMultiAmount(uint256[] _amounts) external view returns (uint256, uint256)
```



*Compute the amount of pool token that needs to be redeemed.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _amounts | uint256[] | Unconverted token balances. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | The amount of pool token that needs to be redeemed. |
| _1 | uint256 | The amount of pool token charged for redemption fee. |

### getRedeemProportionAmount

```solidity
function getRedeemProportionAmount(uint256 _amount) external view returns (uint256[], uint256)
```



*Computes the amounts of underlying tokens when redeeming pool token.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _amount | uint256 | Amount of pool tokens to redeem. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256[] | An array of the amounts of each token to redeem. |
| _1 | uint256 | The amount of fee charged |

### getRedeemSingleAmount

```solidity
function getRedeemSingleAmount(uint256 _amount, uint256 _i) external view returns (uint256, uint256)
```



*Computes the amount when redeeming pool token to one specific underlying token.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _amount | uint256 | Amount of pool token to redeem. |
| _i | uint256 | Index of the underlying token to redeem to. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | The amount of single token that will be redeemed. |
| _1 | uint256 | The amount of pool token charged for redemption fee. |

### getSwapAmount

```solidity
function getSwapAmount(uint256 _i, uint256 _j, uint256 _dx) external view returns (uint256, uint256)
```



*Computes the output amount after the swap.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _i | uint256 | Token index to swap in. |
| _j | uint256 | Token index to swap out. |
| _dx | uint256 | Unconverted amount of token _i to swap in. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | Unconverted amount of token _j to swap out. |
| _1 | uint256 | The amount of fees charged. |

### getTokens

```solidity
function getTokens() external view returns (address[])
```



*Returns the array of token addresses in the pool.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address[] | undefined |

### governance

```solidity
function governance() external view returns (address)
```



*This is the account that has governance control over the StableAsset contract.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### initialA

```solidity
function initialA() external view returns (uint256)
```



*These is a state variables that represents the initial amplification coefficient A.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### initialABlock

```solidity
function initialABlock() external view returns (uint256)
```



*These is a state variables that represents the initial block number when A is set.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### initialize

```solidity
function initialize(address[] _tokens, uint256[] _precisions, uint256[] _fees, contract ITapETH _poolToken, uint256 _A, contract IExchangeRateProvider _exchangeRateProvider, uint256 _exchangeRateTokenIndex) external nonpayable
```



*Initializes the StableAsset contract with the given parameters.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _tokens | address[] | The tokens in the pool. |
| _precisions | uint256[] | The precisions of each token (10 ** (18 - token decimals)). |
| _fees | uint256[] | The fees for minting, swapping, and redeeming. |
| _poolToken | contract ITapETH | The address of the pool token. |
| _A | uint256 | The initial value of the amplification coefficient A for the pool. |
| _exchangeRateProvider | contract IExchangeRateProvider | undefined |
| _exchangeRateTokenIndex | uint256 | undefined |

### maxDeltaD

```solidity
function maxDeltaD() external view returns (uint256)
```



*Max delta D.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### mint

```solidity
function mint(uint256[] _amounts, uint256 _minMintAmount) external nonpayable returns (uint256)
```



*Mints new pool token.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _amounts | uint256[] | Unconverted token balances used to mint pool token. |
| _minMintAmount | uint256 | Minimum amount of pool token to mint. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | The amount of pool tokens minted. |

### mintFee

```solidity
function mintFee() external view returns (uint256)
```



*This is the fee charged for adding liquidity to the StableAsset contract.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### pause

```solidity
function pause() external nonpayable
```



*Pause mint/swap/redeem actions. Can unpause later.*


### paused

```solidity
function paused() external view returns (bool)
```



*This is a state variable that represents whether or not the StableAsset contract is currently paused.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### pendingGovernance

```solidity
function pendingGovernance() external view returns (address)
```



*Pending governance address,*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### poolToken

```solidity
function poolToken() external view returns (contract ITapETH)
```



*This is the address of the ERC20 token contract that represents the StableAsset pool token.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | contract ITapETH | undefined |

### precisions

```solidity
function precisions(uint256) external view returns (uint256)
```



*This is an array of uint256 values representing the precisions of each token in the StableAsset contract. The precision of each token is calculated as 10 ** (18 - token decimals).*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### proposeGovernance

```solidity
function proposeGovernance(address _governance) external nonpayable
```



*Propose the govenance address.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _governance | address | Address of the new governance. |

### rebase

```solidity
function rebase() external nonpayable returns (uint256)
```

This function allows to rebase TapETH by increasing his total supply from the current stableSwap pool by the staking rewards and the swap fee.




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### redeemFee

```solidity
function redeemFee() external view returns (uint256)
```



*This is the fee charged for removing liquidity from the StableAsset contract. redeemFee = redeemFee * FEE_DENOMINATOR*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### redeemMulti

```solidity
function redeemMulti(uint256[] _amounts, uint256 _maxRedeemAmount) external nonpayable returns (uint256[])
```



*Redeems underlying tokens.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _amounts | uint256[] | Amounts of underlying tokens to redeem to. |
| _maxRedeemAmount | uint256 | Maximum of pool token to redeem. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256[] | Amounts received. |

### redeemProportion

```solidity
function redeemProportion(uint256 _amount, uint256[] _minRedeemAmounts) external nonpayable returns (uint256[])
```



*Redeems pool token to underlying tokens proportionally.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _amount | uint256 | Amount of pool token to redeem. |
| _minRedeemAmounts | uint256[] | Minimum amount of underlying tokens to get. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256[] | An array of the amounts of each token to redeem. |

### redeemSingle

```solidity
function redeemSingle(uint256 _amount, uint256 _i, uint256 _minRedeemAmount) external nonpayable returns (uint256)
```



*Redeem pool token to one specific underlying token.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _amount | uint256 | Amount of pool token to redeem. |
| _i | uint256 | Index of the token to redeem to. |
| _minRedeemAmount | uint256 | Minimum amount of the underlying token to redeem to. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | Amount received. |

### setAdmin

```solidity
function setAdmin(address _account, bool _allowed) external nonpayable
```



*Updates the admin role for the address.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _account | address | Address to update admin role. |
| _allowed | bool | Whether the address is granted the admin role. |

### setMintFee

```solidity
function setMintFee(uint256 _mintFee) external nonpayable
```



*Updates the mint fee.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _mintFee | uint256 | The new mint fee. |

### setRedeemFee

```solidity
function setRedeemFee(uint256 _redeemFee) external nonpayable
```



*Updates the redeem fee.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _redeemFee | uint256 | The new redeem fee. |

### setSwapFee

```solidity
function setSwapFee(uint256 _swapFee) external nonpayable
```



*Updates the swap fee.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _swapFee | uint256 | The new swap fee. |

### swap

```solidity
function swap(uint256 _i, uint256 _j, uint256 _dx, uint256 _minDy) external nonpayable returns (uint256)
```



*Exchange between two underlying tokens.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _i | uint256 | Token index to swap in. |
| _j | uint256 | Token index to swap out. |
| _dx | uint256 | Unconverted amount of token _i to swap in. |
| _minDy | uint256 | Minimum token _j to swap out in converted balance. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | Amount of swap out. |

### swapFee

```solidity
function swapFee() external view returns (uint256)
```



*This is the fee charged for trading assets in the StableAsset contract. swapFee = swapFee * FEE_DENOMINATOR*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### tokens

```solidity
function tokens(uint256) external view returns (address)
```



*This is an array of addresses representing the tokens currently supported by the StableAsset contract.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### totalSupply

```solidity
function totalSupply() external view returns (uint256)
```



*The total supply of pool token minted by the swap. It might be different from the pool token supply as the pool token can have multiple minters.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### unpause

```solidity
function unpause() external nonpayable
```



*Unpause mint/swap/redeem actions.*


### updateA

```solidity
function updateA(uint256 _futureA, uint256 _futureABlock) external nonpayable
```



*Update the A value.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _futureA | uint256 | The new A value. |
| _futureABlock | uint256 | The block number to update A value. |

### updateFeeErrorMargin

```solidity
function updateFeeErrorMargin(uint256 newValue) external nonpayable
```



*update fee error margin.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| newValue | uint256 | undefined |

### updateMaxDeltaDMargin

```solidity
function updateMaxDeltaDMargin(uint256 newValue) external nonpayable
```



*update yield error margin.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| newValue | uint256 | undefined |

### updateYieldErrorMargin

```solidity
function updateYieldErrorMargin(uint256 newValue) external nonpayable
```



*update yield error margin.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| newValue | uint256 | undefined |

### yieldErrorMargin

```solidity
function yieldErrorMargin() external view returns (uint256)
```



*Yield error margin.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |



## Events

### AModified

```solidity
event AModified(uint256 futureA, uint256 futureABlock)
```



*This event is emitted when the A parameter is modified.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| futureA  | uint256 | is the new value of the A parameter. |
| futureABlock  | uint256 | is the block number at which the new value of the A parameter will take effect. |

### FeeCollected

```solidity
event FeeCollected(uint256 feeAmount, uint256 totalSupply)
```



*This event is emitted when transaction fees are collected by the StableAsset contract.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| feeAmount  | uint256 | is the amount of fee collected. |
| totalSupply  | uint256 | is the total supply of LP token. |

### FeeMarginModified

```solidity
event FeeMarginModified(uint256 margin)
```



*This event is emitted when the fee margin is modified.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| margin  | uint256 | is the new value of the margin. |

### GovernanceModified

```solidity
event GovernanceModified(address governance)
```



*This event is emitted when the governance is modified.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| governance  | address | is the new value of the governance. |

### GovernanceProposed

```solidity
event GovernanceProposed(address governance)
```



*This event is emitted when the governance is modified.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| governance  | address | is the new value of the governance. |

### Initialized

```solidity
event Initialized(uint8 version)
```



*Triggered when the contract has been initialized or reinitialized.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| version  | uint8 | undefined |

### MaxDeltaDModified

```solidity
event MaxDeltaDModified(uint256 delta)
```



*This event is emitted when the max delta D is modified.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| delta  | uint256 | is the new value of the delta. |

### MintFeeModified

```solidity
event MintFeeModified(uint256 mintFee)
```



*This event is emitted when the mint fee is modified.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| mintFee  | uint256 | is the new value of the mint fee. |

### Minted

```solidity
event Minted(address indexed provider, uint256 mintAmount, uint256[] amounts, uint256 feeAmount)
```

This event is emitted when liquidity is added to the StableAsset contract.



#### Parameters

| Name | Type | Description |
|---|---|---|
| provider `indexed` | address | is the address of the liquidity provider. |
| mintAmount  | uint256 | is the amount of liquidity tokens minted to the provider in exchange for their contribution. |
| amounts  | uint256[] | is an array containing the amounts of each token contributed by the provider. |
| feeAmount  | uint256 | is the amount of transaction fee charged for the liquidity provision. |

### RedeemFeeModified

```solidity
event RedeemFeeModified(uint256 redeemFee)
```



*This event is emitted when the redeem fee is modified.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| redeemFee  | uint256 | is the new value of the redeem fee. |

### Redeemed

```solidity
event Redeemed(address indexed provider, uint256 redeemAmount, uint256[] amounts, uint256 feeAmount)
```



*This event is emitted when liquidity is removed from the StableAsset contract.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| provider `indexed` | address | is the address of the liquidity provider. |
| redeemAmount  | uint256 | is the amount of liquidity tokens redeemed by the provider. |
| amounts  | uint256[] | is an array containing the amounts of each token received by the provider. |
| feeAmount  | uint256 | is the amount of transaction fee charged for the liquidity provision. |

### SwapFeeModified

```solidity
event SwapFeeModified(uint256 swapFee)
```



*This event is emitted when the swap fee is modified.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| swapFee  | uint256 | is the new value of the swap fee. |

### TokenSwapped

```solidity
event TokenSwapped(address indexed buyer, uint256 swapAmount, uint256[] amounts, bool[] amountPositive, uint256 feeAmount)
```

This event is emitted when a token swap occurs.



#### Parameters

| Name | Type | Description |
|---|---|---|
| buyer `indexed` | address | is the address of the account that made the swap. |
| swapAmount  | uint256 | undefined |
| amounts  | uint256[] | is an array containing the amounts of each token received by the buyer. |
| amountPositive  | bool[] | undefined |
| feeAmount  | uint256 | is the amount of transaction fee charged for the swap. |

### YieldCollected

```solidity
event YieldCollected(uint256[] amounts, uint256 feeAmount, uint256 totalSupply)
```



*This event is emitted when yield is collected by the StableAsset contract.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| amounts  | uint256[] | is an array containing the amounts of each token the yield receives. |
| feeAmount  | uint256 | is the amount of yield collected. |
| totalSupply  | uint256 | is the total supply of LP token. |

### YieldMarginModified

```solidity
event YieldMarginModified(uint256 margin)
```



*This event is emitted when the fee margin is modified.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| margin  | uint256 | is the new value of the margin. |



## Errors

### ImbalancedPool

```solidity
error ImbalancedPool(uint256 oldD, uint256 newD)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| oldD | uint256 | undefined |
| newD | uint256 | undefined |

### InsufficientMintAmount

```solidity
error InsufficientMintAmount(uint256 mintAmount, uint256 minMintAmount)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| mintAmount | uint256 | undefined |
| minMintAmount | uint256 | undefined |

### InsufficientRedeemAmount

```solidity
error InsufficientRedeemAmount(uint256 redeemAmount, uint256 minRedeemAmount)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| redeemAmount | uint256 | undefined |
| minRedeemAmount | uint256 | undefined |

### InsufficientSwapOutAmount

```solidity
error InsufficientSwapOutAmount(uint256 outAmount, uint256 minOutAmount)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| outAmount | uint256 | undefined |
| minOutAmount | uint256 | undefined |

### MaxRedeemAmount

```solidity
error MaxRedeemAmount(uint256 redeemAmount, uint256 maxRedeemAmount)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| redeemAmount | uint256 | undefined |
| maxRedeemAmount | uint256 | undefined |

### SameTokenInTokenOut

```solidity
error SameTokenInTokenOut(uint256 tokenInIndex, uint256 tokenOutIndex)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| tokenInIndex | uint256 | undefined |
| tokenOutIndex | uint256 | undefined |


