# Elixer Basics 
Date: 10/01/19

## Links
- https://elixir-lang.org/install.html

### Install on Mac using Homebrew
```
brew install elixir
```

### Check version installed
```
elixir --version
```
### Start Interactive Mode in Terminal
```
iex
```

### Example Commands
- Simple Math: 
  - 20 + 5
  - 5 * 5
  - 125 / 5
- String Concatenation: 
  - "hello" <> " world"

- Show function definition
  - h round/1

- List Manipulation
 - [1,2,3] ++ [4,5,6]
 - [2,3] -- [2]

 ### Run a script file
 - Create file with .exs extension
 - Insert super amazing code into your file
 ```
 IO.puts "Hello from Rachel's Computer"
 IO.puts round(3.58)
 IO.puts is_boolean(true)
 IO.puts is_boolean(1)
 ```
 - Run command with file name

 ```
 elixir simple.exs
 ```

 ### Define a function, compile it to be used in Interactive Mode
 - Create a file with .ex extension
 - Define your function
 ```
 defmodule Math do
    def sum(a, b) do
      a + b
    end
  end
```
 - Run command to compile your function so you can use it
 - Run iex command
 - Run command to use your function

 ```
 elixirc math.ex
 iex > Math.sum(20,5)
 ```