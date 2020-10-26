# amdgpu-fancontrol
Simple bash script based systemd service to easily set fan mode and control fan
speed.

As many others I got annoyed by the fan of my AMD R9 270X spinning up and down
all the time. This bash script was inspired by [amdgpu-fancontrol](https://github.com/grmat/amdgpu-fancontrol).
However, I've rewritten the whole thing and using a json file as conifg file.
In addition you may enable the export of temperature and pwm values to sample
file and feed it to gnuplot.

You may use [exp-curve](https://github.com/WieWaldi/exp-curve) to generate
values to meet your needs.

### Installation
Please take care of the hwmon files. You have to set them correctly in order to
get this script running.
```
cp amdgpu-fancontrol.conf /usr/local/etc
cp amdgpu-fancontrol /usr/local/sbin
cp amdgpu-fancontrol.service /usr/lib/systemd/system
systemctl enable amdgpu-fancontrol
```

Please don't run this script without knowing what you're doing. I'm not
responsible for your burned up graphics card.

