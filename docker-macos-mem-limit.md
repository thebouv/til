# Docker Desktop defaults to 2gb mem

I was building a fairly fat java docker image and it kept OOMing, having Docker crash out with error 137.

With 32gb of RAM on my machine, I was a bit confused. Till I realize that by default it limits to 2gb of RAM.

`Docker Desktop > Preferences > Resources` and up the memory. I moved mine to 8gb and was able to do the build with no issues.
