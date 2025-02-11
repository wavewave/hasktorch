# Hasktorch 0.2 Pre-Release

Hasktorch is a library for tensors and neural networks in Haskell. It is an independent open source community project which leverages the core C++ libraries shared by PyTorch. 

This project is in early development and should only be used by contributing developers. Expect substantial changes to the library API as it evolves. Contributions and PRs are welcome.

Currently we are prepping development and migration for a major 2nd release (please excuse sparsity of docs in the meantime). If you're interested in details or contributing please get in touch (see contributing).

## Project Structure

Basic functionality:

- `deps/` - submodules for build dependencies - libtorch, mklml, pytorch
- `examples/` - high level example models (xor mlp, typed cnn)
- `hasktorch/` - higher level user-facing library, calls into `ffi/`, used by `examples/`

Internals (for contributing developers):

- `codegen/` - code generation, parses `Declarations.yaml` spec from pytorch and produces `ffi/` contents
- `inline-c/` - submodule to inline-cpp fork used for C++ FFI
- `libtorch-ffi/`- low level FFI bindings to libtorch
- `spec/` - specification files used for `codegen/`

Start with `examples/` if you are new to the project.

## Getting dependencies

`deps/` holds several external dependencies that are retrieved using the `deps/get-deps.sh` script.

## Contributing

We welcome new contributors. 

Contact Austin Huang or Sam Stites for access to the [hasktorch slack channel][slack]. You can send an email to [hasktorch@gmail.com][email] or on twitter as [@austinvhuang][austin-twitter] and [@SamStites][sam-twitter].

[email]:mailto:hasktorch@gmail.com
[austin-twitter]:https://twitter.com/austinvhuang
[sam-twitter]:https://twitter.com/samstites
[slack]:https://hasktorch.slack.com 
[gitter-dh]:https://gitter.im/dataHaskell/Lobby

## Developer Information

See [the wiki](https://github.com/hasktorch/ffi-experimental/wiki) for developer information.
