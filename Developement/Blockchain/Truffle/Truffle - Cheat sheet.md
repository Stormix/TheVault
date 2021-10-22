## Scaffold commands:

-  Start new project
	```bash
	npx truffle init project
	```
    
- Scaffold a contract
	```bash
	truffle create contract YourContractName # scaffold a contract
	```
    
- Scaffold a test
	```bash
	truffle create test YourTestName         # scaffold a test
	```

## Common Dev commands:
- Compile
	```bash
	npx truffle compile
	```
	
- Deploy contracts (after you create the migrations)
	```bash
	npx truffle migrate --network development
	```
	
- Truffle Console
	```bash
	npx truffle console --network development
	```