# README

The hackable text editor

## Installation

Copy `bin/atom` and `bin/apm` into your executable folder (like `/usr/local/bin` or `$HOME/bin`):

```sh
sudo curl --location --output /usr/local/bin/apm "https://github.com/timonier/atom/raw/master/bin/apm"
sudo chmod +x /usr/local/bin/apm

sudo curl --location --output /usr/local/bin/atom "https://github.com/timonier/atom/raw/master/bin/atom"
sudo chmod +x /usr/local/bin/atom
```

Linux users can use the [installer](https://github.com/timonier/atom/blob/master/bin/installer):

```sh
curl --location "https://github.com/timonier/atom/raw/master/bin/installer" | sudo sh -s install
```

## Usage

### apm

Run the command `apm`:

```sh
# See all apm options

apm --help

# Run sshuttle

apm install language-docker
# Installing language-docker to /home/morgan/.atom/packages ✓
```

### atom

Run the command `atom`:

```sh
atom
# Start atom
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [atom/atom](https://github.com/atom/atom)
* [image "timonier/atom"](https://hub.docker.com/r/timonier/atom/)
* [timonier/dumb-entrypoint](https://github.com/timonier/dumb-entrypoint)
* [timonier/version-lister](https://github.com/timonier/version-lister)
