<div align="center">
  <h1>Charles CSEC</h1>

  [![Version](https://img.shields.io/badge/Version-1.1-success)](https://github.com/aniko33/Charles-CSEC/releases)
  [![Platform](https://img.shields.io/badge/Platform-Windows%2C%20Mac%2C%20Linux-blue)](#)
  [![Python_version](https://img.shields.io/badge/Python%20version-3.8-blueviolet)](#)

<img src="https://user-images.githubusercontent.com/76649588/208201214-add50e06-c0da-4e2d-ba87-d33c797d035b.png">
</div>

# Index

- [Features](#features)

- [Installation](#installation)

- [Configuration (server-side)](#configuration)

- [Commands (client-side)](#commands)

- [Running](#running)

- [How does it work](#how-does-it-work)

- [Showcase](#showcase)

- [Bug report](#bug-report)

- [License](#license)

- [Contributors](#contributors)

# Features

- RSA encryption

- Easy to read code

- Protected by network sniffer

- File upload with Anonfile

- No trace of your IP

# Installation

### From source code

You need to have **[Python](https://www.python.org/downloads/)** and **[PIP](https://www.w3schools.com/python/python_pip.asp)** installed which you can download from your [**package manager**](https://www.geeksforgeeks.org/how-to-install-python-on-linux/) or site.

After installing Python and PIP you need to install ***program dependencies***.
You can  with this command:

```bash
git clone https://github.com/aniko33/Charles-CSEC && cd Charles-CSEC
```

Then, you will need to install python dependencies:

```bash
pip install -r requirements.txt
```

After you ***installed the various dependencies***, now you **can customise your configurations your server or start your client**.

### From the compiled version

You have to **go to the [latest releases](https://github.com/aniko33/Charles-CSEC/releases)** and you have to ***download the client or the server depending*** on what you want to do.

#### Important note

If you have installed the **server version**, **create a file named *config.json*** and set the [default configurations](https://github.com/aniko33/Charles-CSEC/blob/main/server/config.json).

# Configuration

To configure your server, **open the *config.json* file in the following path: *server/config.json***.

Scroll to the top and edit this part:

```json
{
    "ip": "127.0.0.1",
    "port": 8889,
    "buffer": 1024,
    "welcome_message": "[red]welcome to <chat name>[/red]",
    "protected_by_password": false,
    "password": "P4ssw0rd"
}
```

| Variable              | Description                                                                                                                                       |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| ip                    | The IP address where the server will start listening for connections                                                                              |
| port                  | The **connection port**, it is recommended to ***keep it default*** (***8889***)                                                                  |
| buffer                | The maximum network buffer, changes in this value affects the ***RSA key lenght***                                                                |
| welcome_message       | Welcome message to new users, the colors can be found in the **[Rich documentation](https://rich.readthedocs.io/en/stable/appendix/colors.html)** |
| protected_by_password | You can enter true if you want to **protect your chat by password** or you can put false                                                          |
| password              | Enter the password you want                                                                                                                       |

# Commands

- `/help` show command list

- `/nick` get your nickname

- `/upload <path>` upload file with **Anonfile**, usage: `/upload /home/user/file.txt`

# Running

To run the program just ***go to the main folder*** and execute this command:

#### Client

```bash
cd client && python main.py
```

#### Server

```bash
cd server && python main.py
```

# How does it work

The **keys are generated using the [RSA Encryption Algorithm](https://www.geeksforgeeks.org/rsa-algorithm-cryptography/)**.
<br> when the client wants to send a message, **it gets encrypted with the _public key_**, through the ***server then will forward it to the connected clients***, that **will decrypt it using the _private key_**.

For more detailed explanation, please, refer to the [RSA Encryption Algorithm Documentation](https://www.geeksforgeeks.org/rsa-algorithm-cryptography/)

<div align="center">
<img width="800px" src="https://user-images.githubusercontent.com/76649588/208201163-7e596078-c95d-4902-8d94-e496b60fe315.png" title="" alt="flow.png" data-align="center">
</div>

# Showcase

  ![showcase](https://user-images.githubusercontent.com/76649588/210849677-16957b3d-879f-43b5-9ef5-debbf88dbb02.png)
  ![showcase2](https://user-images.githubusercontent.com/76649588/210849685-99112e0d-041f-4edd-b8ba-6701d4695564.png)
  ![showcase3](https://user-images.githubusercontent.com/76649588/210849687-d2ce8b67-05b0-46f2-9534-475ed5456cc2.png)

# Bug report

**To report an exploit or a bug write**, create a [new issue](https://github.com/aniko33/Charles-CSEC/issues)

# License

This application is distributed under the ***[GPL](https://it.wikipedia.org/wiki/GNU_General_Public_License) license*** you can ***consult the file***: ***[LICENSE.txt](LICENSE.txt)***

# Contributors

<a href="https://github.com/aniko33/Charles-CSEC/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=aniko33/Charles-CSEC"/>
</a>
