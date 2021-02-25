---
description: >-
  Overview of supported blockchains that support contract calls and their chain
  specific details.
---

# Contract calls

## **Ethereum**

### Supported types

`address, bool, bytes, bytes1, bytes2, bytes3, bytes4, bytes5, bytes6, bytes7, bytes8, bytes9, bytes10, bytes11, bytes12, bytes13, bytes14, bytes15, bytes16, bytes17, bytes18, bytes19, bytes20, bytes21, bytes22, bytes23, bytes24, bytes25, bytes26, bytes27, bytes28, bytes29, bytes30, bytes31, bytes32, int8, int16, int24, int32, int40, int48, int56, int64, int72, int80, int88, int96, int104, int112, int120, int128, int136, int144, int152, int160, int168, int176, int184, int192, int200, int208, int216, int224, int232, int240, int248, int256, string, uint8, uint16, uint24, uint32, uint40, uint48, uint56, uint64, uint72, uint80, uint88, uint96, uint104, uint112, uint120, uint128, uint136, uint144, uint152, uint160, uint168, uint176, uint184, uint192, uint200, uint208, uint216, uint224, uint232, uint240, uint248, uint256`

For arrays, please provide the type from above followed by square braces \( ex: uint256\[\] \). The values for an array must be surrounded with square brackets and delimited with "," \(ex. \[1,2,3\]\).

{% hint style="warning" %}
Byte values must be hex-encoded
{% endhint %}

### Chain specific fields

| Field name | Field value | Type | Example |
| :--- | :--- | :--- | :--- |
| `gasLimit` | Gas limit, will be used for the contract call | `Integer` | 300000 |
| `gasPrice` | Gas price, will be used for the contract call \(in WEI\) | `Integer` | 50000000 |

## **Vechain**

### Supported types

`address, bool, bytes, bytes1, bytes2, bytes3, bytes4, bytes5, bytes6, bytes7, bytes8, bytes9, bytes10, bytes11, bytes12, bytes13, bytes14, bytes15, bytes16, bytes17, bytes18, bytes19, bytes20, bytes21, bytes22, bytes23, bytes24, bytes25, bytes26, bytes27, bytes28, bytes29, bytes30, bytes31, bytes32, int8, int16, int24, int32, int40, int48, int56, int64, int72, int80, int88, int96, int104, int112, int120, int128, int136, int144, int152, int160, int168, int176, int184, int192, int200, int208, int216, int224, int232, int240, int248, int256, string, uint8, uint16, uint24, uint32, uint40, uint48, uint56, uint64, uint72, uint80, uint88, uint96, uint104, uint112, uint120, uint128, uint136, uint144, uint152, uint160, uint168, uint176, uint184, uint192, uint200, uint208, uint216, uint224, uint232, uint240, uint248, uint256`

For arrays, please provide the type from above followed by square braces \( ex: uint256\[\] \). The values for an array must be surrounded with square brackets and delimited with "," \(ex. \[1,2,3\]\).

{% hint style="warning" %}
Byte values must be hex-encoded
{% endhint %}

### Chain specific fields

| Field name | Field value | Type | Example |
| :--- | :--- | :--- | :--- |
| `gasLimit` | Gas limit, will be used for the contract call | `Integer` | 300000 |
| `gasPriceCoef` | Gas price coefficient, will be used for the contract call | `Integer` | 0 |

## **Tron**

### Supported types

All solidity types are supported:

`address, bool, bytes, bytes1, bytes2, bytes3, bytes4, bytes5, bytes6, bytes7, bytes8, bytes9, bytes10, bytes11, bytes12, bytes13, bytes14, bytes15, bytes16, bytes17, bytes18, bytes19, bytes20, bytes21, bytes22, bytes23, bytes24, bytes25, bytes26, bytes27, bytes28, bytes29, bytes30, bytes31, bytes32, int8, int16, int24, int32, int40, int48, int56, int64, int72, int80, int88, int96, int104, int112, int120, int128, int136, int144, int152, int160, int168, int176, int184, int192, int200, int208, int216, int224, int232, int240, int248, int256, string, uint8, uint16, uint24, uint32, uint40, uint48, uint56, uint64, uint72, uint80, uint88, uint96, uint104, uint112, uint120, uint128, uint136, uint144, uint152, uint160, uint168, uint176, uint184, uint192, uint200, uint208, uint216, uint224, uint232, uint240, uint248, uint256`

For arrays, please provide the type from above followed by square braces \( ex: uint256\[\] \). The values for an array must be surrounded with square brackets and delimited with "," \(ex. \[1,2,3\]\).

{% hint style="warning" %}
Byte values must be hex-encoded
{% endhint %}

## **Neo**

### Supported types

`Signature, Boolean, Integer, Hash160, Hash256, ByteArray, Address, PublicKey, String`

For arrays, please provide the type from above followed by square braces \( ex: String\[\] \). The values for an array must be surrounded with square brackets and delimited with "," \(ex. \[1,2,3\]\).

{% hint style="warning" %}
Byte values must be hex-encoded
{% endhint %}

### Chain specific fields

| Field name | Field value | Type | Example |
| :--- | :--- | :--- | :--- |
| `networkFee` | Network fee used for the contract call. By default, 0.1 is used | `Number` | 0.1 |
| `systemFee` | System fee used for the contract call | `Number` | 0.1 |
| `outputs` | It is possible to add additional asset transfers together with a contract call by attaching additional outputs. This is a JSON object containing "to", "amount" and "assetId" with json types respectively string, number and string. If "to" is a script hash, it will be translated to a valid NEO address | `JSON` | { "to": "AKJrLM5Q…​", "amount": 1, "assetId": "602c79718…​" } |

## Binance Smart Chain

### Supported types

`address, bool, bytes, bytes1, bytes2, bytes3, bytes4, bytes5, bytes6, bytes7, bytes8, bytes9, bytes10, bytes11, bytes12, bytes13, bytes14, bytes15, bytes16, bytes17, bytes18, bytes19, bytes20, bytes21, bytes22, bytes23, bytes24, bytes25, bytes26, bytes27, bytes28, bytes29, bytes30, bytes31, bytes32, int8, int16, int24, int32, int40, int48, int56, int64, int72, int80, int88, int96, int104, int112, int120, int128, int136, int144, int152, int160, int168, int176, int184, int192, int200, int208, int216, int224, int232, int240, int248, int256, string, uint8, uint16, uint24, uint32, uint40, uint48, uint56, uint64, uint72, uint80, uint88, uint96, uint104, uint112, uint120, uint128, uint136, uint144, uint152, uint160, uint168, uint176, uint184, uint192, uint200, uint208, uint216, uint224, uint232, uint240, uint248, uint256`

For arrays, please provide the type from above followed by square braces \( ex: uint256\[\] \). The values for an array must be surrounded with square brackets and delimited with "," \(ex. \[1,2,3\]\).

{% hint style="warning" %}
Byte values must be hex-encoded
{% endhint %}

### Chain specific fields

| Field name | Field value | Type | Example |
| :--- | :--- | :--- | :--- |
| `gasLimit` | Gas limit, will be used for the contract call | `Integer` | 300000 |
| `gasPrice` | Gas price, will be used for the contract call \(in WEI\) | `Integer` | 20000000 |

## Resources

{% page-ref page="../widget-advanced/reference/executecontract.md" %}

{% page-ref page="../widget-advanced/object-type-reference/wip-contractexecutiondto.md" %}



