# sudo

## Synopsis

`sudo` for windows is made for elevating user rights on the fly. It will invoke UAC request. 
The main purpose to get rid of mouse (to avoid shift+rightclick or Run as ...). Since runas cli commmand so much inconvenient to use. 


## Usage

```
C:\>sudo cmd /c dir
```

Then, you'll see the UAC dialog.


## Examples

### Display contents of file which can't access from you

```
sudo cmd /c type secret-file.txt > accessible-file.txt
```

### Pipe from/to stream

```
echo 123 | sudo my-command.exe | more
```

### Change IP address

```
sudo netsh interface ip add address "Local Area Connection" 33.33.33.33 255.255.255.255
```

### Edit hosts file

```
sudo notepad c:\windows\system32\drivers\etc\hosts
```

### Create admin's console

```
sudo
```

## Installation

* From scratch:

	You will need golang 1.10 or later.

	1. `go get github.com/moldabekov/sudo`
	2. `go build -ldflags"-s -w" .`


* Binary:

	Download from [release](https://github.com/moldabekov/sudo/releases) tab.


## License

MIT


## Credits

Yasuhiro Matsumoto (a.k.a. mattn) as a initial author.
