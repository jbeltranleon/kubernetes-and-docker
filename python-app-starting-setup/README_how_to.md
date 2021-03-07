# How to

To run this image into a container and be able to interact with the script we need to add the  `-i` flag that keep STDIN open even if no attached and the `-t` flag that allocate a pseudo-TTY. we can combine them using the `-it` flag.


`docker run -i -t <cointainer-id>` or 
`docker run -it <cointainer-id>` or even
`docker run -ti <cointainer-id>`