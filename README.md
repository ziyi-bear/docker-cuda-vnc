cuda-vnc
========
TensorRT + LXDE desktop + Firefox browser + TightVNC server.

Requirements
------------

- [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker) - see [requirements](https://github.com/NVIDIA/nvidia-docker/wiki/CUDA#requirements) for more details.

Build
-----
Include password.txt with the password for TightVNC (by default this is "11223344"). This must be at least 8 characters and is truncated if longer.

Usage
-----
Use NVIDIA Docker: ``nvidia-docker run -dP kaixhin/cuda-vnc``.

The default password should be changed. To do so start up a container and then run `docker exec <id> bash -c "echo -e '<password>\n<password>\nn' | vncpasswd"`.

For automatically mapping a VNC port use ``nvidia-docker run -dP kaixhin/cuda-vnc`` and `docker port <id>` to retrieve the port.
For specifying the port manually use ``nvidia-docker run -d -p <port>:5901 kaixhin/cuda-vnc``.
The shell can be entered as usual using ``nvidia-docker run -it kaixhin/cuda-vnc bash``.

For more information on CUDA on Docker, see the [repo readme](https://github.com/Kaixhin/dockerfiles#cuda).

ref
--------
If you find this useful in research please consider [kaixhin/cuda-vnc](https://github.com/Kaixhin/dockerfiles).