# rpi-opencv
Docker container repo for OpenCV container in RPI (armv7l) environment

Can be pulled from
```
thatsarr/alpine_armv7l-opencv
```

### Image contains:
- alpine linux (arm32v7/alpine:3.10.2) as base 
- python3 (3.7.4)
- openCV (4.1.1)

OpenCV compiled with following config:
```
-- General configuration for OpenCV 4.1.1 =====================================
--   Version control:               unknown
-- 
--   Platform:
--     Timestamp:                   2019-10-04T22:48:20Z
--     Host:                        Linux 4.19.69-v7+ armv7l
--     CMake:                       3.14.5
--     CMake generator:             Unix Makefiles
--     CMake build tool:            /usr/bin/make
--     Configuration:               RELEASE
-- 
--   CPU/HW features:
--     Baseline:                    NEON
--       requested:                 DETECT
--       disabled:                  VFPV3 NEON
-- 
--   C/C++:
--     Built as dynamic libs?:      NO
--     C++ Compiler:                /usr/bin/clang++  (ver 8.0.0)
--     C++ flags (Release):         -fsigned-char -W -Wall -Werror=return-type -Werror=non-virtual-dtor -Werror=address -Werror=sequence-point -Wformat -Werror=format-security -Wmissing-declarations -Wmissing-prototypes -Wstrict-prototypes -Wundef -Winit-self -Wpointer-arith -Wshadow -Wsign-promo -Wuninitialized -Winit-self -Winconsistent-missing-override -Wno-delete-non-virtual-dtor -Wno-unnamed-type-template-args -Wno-comment -fdiagnostics-show-option -pthread -Qunused-arguments -ffunction-sections -fdata-sections  -fvisibility=hidden -fvisibility-inlines-hidden -O3 -DNDEBUG  -DNDEBUG
--     C++ flags (Debug):           -fsigned-char -W -Wall -Werror=return-type -Werror=non-virtual-dtor -Werror=address -Werror=sequence-point -Wformat -Werror=format-security -Wmissing-declarations -Wmissing-prototypes -Wstrict-prototypes -Wundef -Winit-self -Wpointer-arith -Wshadow -Wsign-promo -Wuninitialized -Winit-self -Winconsistent-missing-override -Wno-delete-non-virtual-dtor -Wno-unnamed-type-template-args -Wno-comment -fdiagnostics-show-option -pthread -Qunused-arguments -ffunction-sections -fdata-sections  -fvisibility=hidden -fvisibility-inlines-hidden -g  -O0 -DDEBUG -D_DEBUG
--     C Compiler:                  /usr/bin/clang
--     C flags (Release):           -fsigned-char -W -Wall -Werror=return-type -Werror=non-virtual-dtor -Werror=address -Werror=sequence-point -Wformat -Werror=format-security -Wmissing-declarations -Wmissing-prototypes -Wstrict-prototypes -Wundef -Winit-self -Wpointer-arith -Wshadow -Wsign-promo -Wuninitialized -Winit-self -Winconsistent-missing-override -Wno-delete-non-virtual-dtor -Wno-unnamed-type-template-args -Wno-comment -fdiagnostics-show-option -pthread -Qunused-arguments -ffunction-sections -fdata-sections  -fvisibility=hidden -fvisibility-inlines-hidden -O3 -DNDEBUG  -DNDEBUG
--     C flags (Debug):             -fsigned-char -W -Wall -Werror=return-type -Werror=non-virtual-dtor -Werror=address -Werror=sequence-point -Wformat -Werror=format-security -Wmissing-declarations -Wmissing-prototypes -Wstrict-prototypes -Wundef -Winit-self -Wpointer-arith -Wshadow -Wsign-promo -Wuninitialized -Winit-self -Winconsistent-missing-override -Wno-delete-non-virtual-dtor -Wno-unnamed-type-template-args -Wno-comment -fdiagnostics-show-option -pthread -Qunused-arguments -ffunction-sections -fdata-sections  -fvisibility=hidden -fvisibility-inlines-hidden -g  -O0 -DDEBUG -D_DEBUG
--     Linker flags (Release):      -Wl,--gc-sections  
--     Linker flags (Debug):        -Wl,--gc-sections  
--     ccache:                      NO
--     Precompiled headers:         NO
--     Extra dependencies:          /usr/lib/libopenblas.so ade /usr/lib/libgthread-2.0.so /usr/lib/libglib-2.0.so /usr/lib/libintl.so /usr/lib/libwebp.so /usr/lib/libpng.so /lib/libz.so /usr/lib/libtiff.so /usr/lib/libjasper.so /usr/lib/libjpeg.so /usr/lib/libImath.so /usr/lib/libIlmImf.so /usr/lib/libIex.so /usr/lib/libHalf.so /usr/lib/libIlmThread.so dl m pthread rt
--     3rdparty dependencies:       ittnotify libprotobuf quirc tegra_hal
-- 
--   OpenCV modules:
--     To be built:                 calib3d core dnn features2d flann gapi highgui imgcodecs imgproc ml objdetect photo python3 stitching video videoio
--     Disabled:                    world
--     Disabled by dependency:      -
--     Unavailable:                 java js python2 ts
--     Applications:                apps
--     Documentation:               NO
--     Non-free algorithms:         NO
-- 
--   GUI: 
--     GTK+:                        NO
--     VTK support:                 NO
-- 
--   Media I/O: 
--     ZLib:                        /lib/libz.so (ver 1.2.11)
--     JPEG:                        /usr/lib/libjpeg.so (ver 80)
--     WEBP:                        /usr/lib/libwebp.so (ver encoder: 0x020e)
--     PNG:                         /usr/lib/libpng.so (ver 1.6.37)
--     TIFF:                        /usr/lib/libtiff.so (ver 42 / 4.0.10)
--     JPEG 2000:                   /usr/lib/libjasper.so (ver 2.0.16)
--     OpenEXR:                     /usr/lib/libImath.so /usr/lib/libIlmImf.so /usr/lib/libIex.so /usr/lib/libHalf.so /usr/lib/libIlmThread.so (ver 2.2.1)
--     HDR:                         YES
--     SUNRASTER:                   YES
--     PXM:                         YES
--     PFM:                         YES
-- 
--   Video I/O:
--     FFMPEG:                      YES
--       avcodec:                   YES (58.35.100)
--       avformat:                  YES (58.20.100)
--       avutil:                    YES (56.22.100)
--       swscale:                   YES (5.3.100)
--       avresample:                YES (4.0.0)
--     GStreamer:                   YES (1.16.0)
--     v4l/v4l2:                    YES (linux/videodev2.h)
--     gPhoto2:                     YES
-- 
--   Parallel framework:            pthreads
-- 
--   Trace:                         YES (with Intel ITT)
-- 
--   Other third-party libraries:
--     Lapack:                      YES (/usr/lib/libopenblas.so)
--     Eigen:                       NO
--     Custom HAL:                  YES (carotene (ver 0.0.1))
--     Protobuf:                    build (3.5.1)
-- 
--   OpenCL:                        YES (no extra features)
--     Include path:                /tmp/opencv-4.1.1/3rdparty/include/opencl/1.2
--     Link libraries:              Dynamic load
-- 
--   Python 3:
--     Interpreter:                 /usr/bin/python3 (ver 3.7.4)
--     Libraries:                   /usr/lib/libpython3.so (ver 3.7.4)
--     numpy:                       /usr/lib/python3.7/site-packages/numpy/core/include (ver 1.16.4)
--     install path:                lib/python3.7/site-packages/cv2/python-3.7
-- 
--   Python (for build):            /usr/bin/python3
-- 
--   Java:                          
--     ant:                         NO
--     JNI:                         NO
--     Java wrappers:               NO
--     Java tests:                  NO
-- 
--   Install to:                    /usr
-- -----------------------------------------------------------------
```
