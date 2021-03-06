# Pixcryption
Pixel Safe Encryption - **Now with AES Encryption on Strings**

![Stars](https://img.shields.io/github/stars/M4cs/pixcryption) ![Issues](https://img.shields.io/github/issues/M4cs/pixcryption) ![License](https://img.shields.io/github/license/M4cs/pixcryption)

Run a Remote Environment To Test Pixcryption: [![Run on Repl.it](https://repl.it/badge/github/M4cs/pixcryption)](https://repl.it/github/M4cs/pixcryption)

# Goal

Pixcryption's goal is to offer a new form of steganography/encryption through imagery. It uses a random seeded UUID to generate a user_key which matches RGB perfect values to match to unicode characters. These are stored in a `user_key.png` file which is used to encrypt and decrypt messages. The speed is getting there but there is 100% room for improvement. I have been working on this for 2 months now and with contributions from @TotallyNotChase he was able to implement AES encryption to the strings passed into Pixcryptions image cipher.

# Example Results

<p align="center">
  <a align="center"><b>User Key (Compressed in README):</b></a></br>
  <a align="center"><img src="https://github.com/M4cs/pixcryption/blob/master/examples/userkey.png?raw=true" width="50%"></a></br>
  <a align="center"><b>Encrypted Message (Uncompressed):</b></a></br>
  <a align="center"><img src="https://github.com/M4cs/pixcryption/blob/master/examples/example_enc_msg.png?raw=true"></a></br>
  <a align="center">Hi my name is Max and this is an encrypted image that decrypts into a string. I call it pixelsafe encryption and plan on making it into an awesome thing.</a>
</p>

# Requirements

- Python 3.7+
- Pillow
- Numpy
- PyCryptodome

# Development

To install run either `pip3 install -r requirements.txt` or `poetry install` if you use poetry for dependency management.

To generate a user_key for testing run `python3 test.py` once and then to test encryption/decryption with said user_key run the `test.py` file again.

# Usage

Inside of the `core.lib` module you will find all functions currently used in the project.

With these you can generate a user key, grab a key_list from a user key, and encrypt/decrypt messages. The implementation is pretty simple and you can take a look at `test.py` for an example.

**This only encrypts unicode characters at the moment which makes it a good choice for messaging. The # of pixels in the image will be == to the # of characters in the string encrypted. This is one security flaw which we need to look into fixing.**

# Contribution

If you would like to contribute to pixcryption please submit a pull request. Any help is welcome and all PRs will be reviewed.

Check [CONTRIBUTING.md](https://github.com/M4cs/pixcryption/blob/master/CONTRIBUTING.md) for more information.
