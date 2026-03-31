# Gas-Optimized-Simple-Storage-Efficient-data-storage-
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract GasOptimizedStorage {
    uint256 public storedData;   // Single storage slot for gas efficiency

    event DataUpdated(uint256 newData);

    function set(uint256 newData) public {
        storedData = newData;
        emit DataUpdated(newData);
    }

    function get() public view returns (uint256) {
        return storedData;
    }
}

