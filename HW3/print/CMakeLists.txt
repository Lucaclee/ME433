add_executable(print
        print.c
        )

pico_enable_stdio_usb(print 1) 
pico_enable_stdio_uart(print 0)

# pull in common dependencies
target_link_libraries(print pico_stdlib)

# create map/bin/hex file etc.
pico_add_extra_outputs(print)

