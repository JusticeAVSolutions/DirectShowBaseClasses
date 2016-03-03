file(GLOB BASECLASSES_HEADER_FILES
     LIST_DIRECTORIES false
     amextra.h
     amfilter.h
     cache.h
     checkbmi.h
     combase.h
     cprop.h
     ctlutil.h
     ddmm.h
     dllsetup.h
     dxmperf.h
     fourcc.h
     measure.h
     msgthrd.h
     mtype.h
     outputq.h
     perflog.h
     perfstruct.h
     pstream.h
     pullpin.h
     refclock.h
     reftime.h
     renbase.h
     schedule.h
     seekpt.h
     source.h
     streams.h
     strmctl.h
     sysclock.h
     transfrm.h
     transip.h
     videoctl.h
     vtrans.h
     winctrl.h
     winutil.h
     wxdebug.h
     wxlist.h
     wxutil.h)
file(GLOB BASECLASSES_SOURCE_FILES
     LIST_DIRECTORIES false
     amextra.cpp
     amfilter.cpp
     amvideo.cpp
     arithutil.cpp
     combase.cpp
     cprop.cpp
     ctlutil.cpp
     ddmm.cpp
     dllentry.cpp
     dllsetup.cpp
     mtype.cpp
     outputq.cpp
     perflog.cpp
     pstream.cpp
     pullpin.cpp
     refclock.cpp
     renbase.cpp
     schedule.cpp
     seekpt.cpp
     source.cpp
     strmctl.cpp
     sysclock.cpp
     transfrm.cpp
     transip.cpp
     videoctl.cpp
     vtrans.cpp
     winctrl.cpp
     winutil.cpp
     wxdebug.cpp
     wxlist.cpp
     wxutil.cpp)

source_group(BaseClasses\\Header_Files FILES  ${BASECLASSES_HEADER_FILES})
source_group(BaseClasses\\Source_Files FILES  ${BASECLASSES_SOURCE_FILES})

add_library(BaseClasses STATIC
            ${BASECLASSES_HEADER_FILES}
            ${BASECLASSES_SOURCE_FILES})

target_include_directories(BaseClasses PUBLIC .)
