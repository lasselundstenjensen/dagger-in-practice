---
title: "Stuff to install"
---

# Stuff to install

We will be using **Visual Studio Code** (VSCode) as our editor, and we will be **using the terminal to run our code**. We also need **Go** and extensions for VSCode to make our lives easier.

Additionally, we will be using **Docker** and **Dagger**.

</br>
</br>
</br>
</br>

## What you need to install

- **Visual Studio Code** (latest version, 1.92.2)
- **Go** (latest version, 1.23.0)
- **Docker Engine** (latest version, 27.1.1), can be installed with **Docker Desktop** (latest version, 4.33.0)
- **Dagger** (latest version, 0.12.5)

Versions are as of writing this course (September 2024).

Using Homebrew for package management is recommended. You can install Homebrew by following the instructions [here](https://brew.sh/). Homebrew only works on MacOS and most Linux distributions.

> **Note:** If you are running on Windows, using **WSL2** is recommended. You can install it by following the instructions [here](https://docs.microsoft.com/en-us/windows/wsl/install). Ubuntu is recommended as the Linux distribution.

</br>
</br>
</br>
</br>

## Visual Studio Code

- Install VSCode from [here](https://code.visualstudio.com/download).

</br>
</br>
</br>
</br>

## Go

1. Install Go from [here](https://golang.org/dl/) or if you are using Homebrew, run `brew install go`.

2. Install the following [Go extension](https://marketplace.visualstudio.com/items?itemName=golang.go) in VSCode:
![Extensions](../../images/lessons/golang-introduction/vscode-go-extension.png)
This will install several tool integrations in VSCode and most importantly the Go LSP.

</br>
</br>

> WSL = Windows Subsystem for Linux</br>
> LSP = Language Server Protocol

</br>
</br>

### <i class="fa-solid fa-rocket"></i> Let's see if it works <i class="fa-solid fa-rocket"></i>

Hello World in Go!

Don't worry about the code for now. You will get to understand it when we go through the fundamentals.

Create a new file called `main.go`:

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

</br>
</br>

Run:

```bash
go run main.go
```

</br>
</br>

You should see something that is not an error >D

```text
Hello, World!
```

</br>

You are now ready to start using Go!

</br>
</br>
</br>
</br>

## Dagger

The easiest way to install Dagger is to use **Homebrew**. Alternatively, see the [official installation guide](https://docs.dagger.io/install/).

Run the following command:

```bash
brew install dagger
```

</br>
</br>

### <i class="fa-solid fa-rocket"></i> Let's see if it works <i class="fa-solid fa-rocket"></i>

Run:

```bash
dagger version
```

You should see an output something along:

```text
dagger v0.12.5 (registry.dagger.io/engine:v0.12.5) darwin/arm64
```

</br>

You are now ready to start using Dagger!

</br>
</br>
