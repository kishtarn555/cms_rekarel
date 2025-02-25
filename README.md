# CMS support for Karel

This adds support for Karel Java and Karel Pascal as used by the [Mexican Olimpiad in Informatics](https://www.olimpiadadeinformatica.org.mx/OMI/OMI/Inicio.aspx)

# Before you use it

> Do not use `Karel (rekarel.1.0.0)` 

The Karel language `Karel (rekarel.1.0.0)` is deprecated and is kept for compatibility purposes. It will be deleted after August 2025.

Both languages compile and run the same language (ReKarel 2.3), this is the reason as to why Karel (rekarel 1.0.0) is deprecated, due to its poor name.

However, deleting a language from a CMS causes internal errors if there were submissions to it or if a contest allows it and such, so it is kept to give time to consumers to plan their migration.

# Install

## Prerequisites


First install the compiler (Node must be at least 1.10.2)

`npm install -g @rekarel/cli`


Make sure it is in the correct place by running

`rekarel -V`

And

`type -a rekarel` 

It should be in `/usr/local/bin/rekarel`, otherwise, you'll have to move it.

Next, let's install the interpreter.

Download the C++ VM

https://github.com/kishtarn555/rekarel-cpp-interpreter/releases/tag/v2.3.1

Go to the download/clone folder and run:

Then 
```
mkdir bin
make karel
cd bin
sudo install -m 755 karel /usr/local/bin
```

## Karel for CMS

Run 

`python3 setup.py install`

Restart CMS


# Usage

This package adds two things
* Karel languages
* Karel task type.

A Karel task type is a slightly modified version of a [batch](https://cms.readthedocs.io/en/latest/Task%20types.html#batch) task that changes the task output the correct information, like Instruction Limit Exceeded and the type or Runtime Error

# ReKarel project map

Here's a map for exploring the ReKarel project:


| Repo  | Description |
| --- | --- |
| [ReKarel](https://github.com/kishtarn555/ReKarel/) | Web IDE for ReKarel | 
| [Core](https://github.com/kishtarn555/rekarel-core) | JS compiler, interpreter and transpiler |
| [CLI](https://github.com/kishtarn555/rekarel-cli) | Node command line interface for the core |
| [CPP Interpreter](https://github.com/kishtarn555/rekarel-cpp-interpreter) | Faster C++ interpreter, runs bytecode compiled by the CLI compiler |
| [CMS](https://github.com/kishtarn555/cms_rekarel) | Adds ReKarel support to [CMS](https://github.com/cms-dev/cms) |
| [KarelCaseGenerator](https://github.com/kishtarn555/KarelCaseGenerator/) | Python Case Generator |

![image](https://github.com/user-attachments/assets/a0f155d3-780a-41dd-a2a2-89ebbd04a2b3)



