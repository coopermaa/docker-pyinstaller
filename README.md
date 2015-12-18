# docker-pyinstaller
[![](https://badge.imagelayers.io/coopermaa/pyinstaller:latest.svg)](https://imagelayers.io/?images=coopermaa/pyinstaller:latest 'Get your own badge on imagelayers.io')

Docker image for pyinstaller

## How to use this image

Convert a Python program into a stand-alone executable:

```bash
# Create a hello.py
$ echo 'print("Hello Python")' > hello.py

# Convert hello.py into a stand-alone executable result in an ELF executable as 'dist/hello'
$ docker run -v $(pwd):/code pyinstaller --onefile --noconfirm hello.py

# Run the executable
$ dist/hello
Hello Python
```

> ## A special note
> 
> * pyinstaller cannot run as root user, you have to run the container as a non-root user.

