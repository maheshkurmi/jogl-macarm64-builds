# jogl-macarm64-builds
Compiled Jogl jars with natives for mac arm64
Just add them to classpath to add jogl natively on mac M1

## Tested On
Macbook pro M1 2020
zulu-8.jdk for arm64

## Build instructions
Follow https://github.com/jzy3d/jogl/blob/feature/macosx-arm64/HOW-TO-ADD-ARM64-TO-2.4.md for gluegen and jogl builds respectively
###for JOAL builds
* clone joal from https://jogamp.org/cgit/joal.git/
* joal/make/build.xml: Find line <condition property="cmake.arch.x64" value="-arch x86_64" else=""> and replace x86_64 by ar64
* navigate to joal/build directory
* run ant -Dtarget.sourcelevel=1.8 -Dtarget.targetlevel=1.8 -Dtarget.rt.jar=/Library/Java/JavaVirtualMachines/zulu-8.jdk/Contents/Home/jre/lib/rt.jar
* you will find native jars in joal/build/jar directory

