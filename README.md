# Installation

Copy the file `bin/atom` into your executable folder (like `/usr/local/bin` or `$HOME/bin`):

```bash
sudo curl -sLo /usr/local/bin/apm "https://github.com/timonier/atom/raw/master/bin/apm"
sudo chmod +x /usr/local/bin/apm

sudo curl -sLo /usr/local/bin/atom "https://github.com/timonier/atom/raw/master/bin/atom"
sudo chmod +x /usr/local/bin/atom
```

Linux users can use the [installer](https://github.com/timonier/atom/blob/master/bin/installer):

```bash
curl -sL "https://github.com/timonier/atom/raw/master/bin/installer" | sudo bash -s install
```

# Usage

Run the command `atom`:

```bash
atom -f
# Start Atom
```

__Note__: By default, the version `1.4.1` will be used. To change the version, define the `TAG` before the command:

```bash
atom --version
# 1.4.1

TAG="..." atom
# atom ...
```

# Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

# Links

* [atom](https://atom.io/)
* [image "timonier/atom"](https://hub.docker.com/r/timonier/atom/)
