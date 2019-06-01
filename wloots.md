#Compile and install wlroots on Fedora
Install dependencies:
$ sudo dnf install meson libwayland-server libwayland-client libwayland-egl wayland-protocols-devel mesa-libEGL-devel mesa-libGLES-devel libdrm libgbm-devel libinput-devel libxkbcommon-devel systemd-devel pixman systemd libcap
Clone wlroots repo.
git clone https://github.com/swaywm/wlroots.git
cd into cloned repo
$ cd wlroot
Start building
$ meson build && ninja -C build 
Install 
$ sudo ninja -C build install
