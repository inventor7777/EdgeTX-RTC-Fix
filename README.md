To build this firmware, here are the steps i used.

#1 - https://gitpod.io/#https://github.com/edgetx/edgetx/tree/nightly



#2 - (Terminal in GitPod)

git revert 0ed1b94

cmake -Wno-dev -DPCB=X7 -DPCBREV=MT12 -DDEFAULT_MODE=2 -DCMAKE_BUILD_TYPE=Release

make arm-none-eabi-configure

make -C arm-none-eabi -j`nproc` firmware

cd arm-none-eabi

mv firmware.bin YOUR_FILE_NAME.bin

Then go to the arm-none-eabi folder under build, and you should see your firmware, which you can right click and download.
