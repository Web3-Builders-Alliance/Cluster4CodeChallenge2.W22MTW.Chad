# Coding Challenge

The challenge today is to setup the two chains and to test the contract on them.

- [x] Clone cw-ibc-queries
- [ ] Run `generate_template` in the ci-scripts folder for osmosis and wasmd
- [ ] Start osmosis and wasmd using their start.sh scripts
- [ ] Go into the tests folder and run nom install
- [ ] Then run nom test to runs the tests

# CosmWasm IBC Queries
Implements generic IBC queries in CosmWasm. This implementation requires the same contract to be deployed on both chains wishing to query each other.

This contract is inspired by Confio's [cw-ibc-demo](https://github.com/confio/cw-ibc-demo), and from work done during HackAtom 2022.

## Unit Tests

All unit tests are in Rust and assume a mocked out environment.
They don't actually send packets between contracts in any way,
but return a fully mocked response. This can run through many
code paths and get a reasonable level of confidence in the basic
logic. However, you will need to run through full-stack
integration tests to actually have any confidence it will work
as expected in production.

To ensure they are proper, run the following in the repo root:

```shell
cargo test
```

## Integration Tests

See the `tests` directory.
