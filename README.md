# DAppPrivacyFramework
A DApp for public key aggregation to construct Ring Signature for Privacy of transaction initiators.
The Smart contract stores hashed public keys of users who pass Non-interactive Zero-knowledge Proofs (NIZKP) and returns the user's hashed public key along with three randomly retrieved hashed public keys stored in the contract.

Users who pass the NIZKP with the contract having hashed public keys below the set threshold (in this case >=4) are placed on "Awaiting list". Such users can call the "AwaitResponse" contract method to have three hashed public keys once the threshold has been met.

The output hashed public keys are used at the front end to retrieve equivalent public keys stored on the decentralized storage platform IPFS. These encrypted public keys are decrypted and made available to the user to be used for the contruction of Lightweight Ring Signature (LwRS). 

The LwRS is used with modified version of Dual-key Stealth Address Protocol for IoT (DkSAP-IoT) for privacy-preservation of DApp users. The framework is generic hence applicable to diverse blockchain and distributed ledger platforms.  
