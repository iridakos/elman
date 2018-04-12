# elman

A script for full text searching Linux man pages with Elasticsearch.
This script has been developed to play around with the idea described in [this post](https://iridakos.com/tutorials/2018/04/12/elasticsearch-linux-man-pages).

![elman demo gif](https://github.com/iridakos/elman/raw/master/resources/elasticsearch-manpages.gif)

## How does it work

Given that you have a running **Elasticsearch** instance, the script creates an index named `elman` and feeds it with the man pages of your Linux system using the `apropos .` command to get all available pages. Then you can use it to full text search the man pages as simple as:

```bash
elman concatenate files
```

## Installation

It is a Ruby script so you must have the language installed.

Clone this repository and from withing the script's directory execute:

```bash
bundle
```

to install the `elasticsearch` gem and its dependencies.

**Note**

If you don't have bundler on your system, install it with:

```bash
gem install bundler
```

## Setup the Elasticsearch index

To setup the index and load the man pages use:
```bash
./elman -s
```

or

```bash
./elman --setup
```

## Usage

### Full text search

To search the man pages, use:

```bash
elman <query>
```

#### Example:
```bash
elman edit images
```

## TODO

- Improve search definition

## Contributing

1. Fork it ( https://github.com/iridakos/elman/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## License

This tool is open source under the [MIT License](https://opensource.org/licenses/MIT) terms.
