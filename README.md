# Forge Template

Template for Forge project based on https://github.com/soliditylabs/forge-erc20-template.

## Getting Started

Click `Use this template` on [Github](https://github.com/PraneshASP/forge-template) to create a new repository with this repo as the initial state.

Or run (also works for existing projects):

```bash
forge init --template https://github.com/PraneshASP/forge-template
git submodule update --init --recursive
forge install
```

## Directory structure

```ml
lib
├─ forge-std — https://github.com/brockelmore/forge-std
├─ openzeppelin-contracts — https://github.com/OpenZeppelin/openzeppelin-contracts
src
├─ tests
│  └─ Faucet.t.sol — "Simple base setup for tests"
├─ Facuet.sol — "A Simple starter for the Faucet contract"
└─ MockERC20.sol — "A mock erc20 token for the faucet"

```

## Development

**Compilation**

```bash
forge build
```

**Testing**

```bash
forge test
```

To run tests with console outputs (`console.logs()`):

```bash
forge test -vv
```


**Deployment**

Copy the .`env.example` file to `.env` and update the values.

First, deploy the MockERC20 to Kovan:

```bash
./scripts/deploy_token_kovan.sh
```

Then, deploy the Faucet to Kovan:

```bash
./scripts/deploy_faucet_kovan.sh
```

### Configure Foundry

Using [foundry.toml](./foundry.toml), Foundry is easily configurable.

For a full list of configuration options, see the Foundry [configuration documentation](https://github.com/gakonst/foundry/blob/master/config/README.md#all-options).

## License

[MIT](https://github.com/PraneshASP/forge-template/blob/master/LICENSE)

## Acknowledgements

- https://github.com/soliditylabs/forge-erc20-template as main reference

## Disclaimer

_These smart contracts are being provided as is. No guarantee, representation or warranty is being made, express or implied, as to the safety or correctness of the user interface or the smart contracts. They have not been audited and as such there can be no assurance they will work as intended, and users may experience delays, failures, errors, omissions, loss of transmitted information or loss of funds. The creators are not liable for any of the foregoing. Users should proceed with caution and use at their own risk._
