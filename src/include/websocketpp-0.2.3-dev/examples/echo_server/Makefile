BOOST_LIBS=boost_system boost_date_time boost_program_options boost_thread boost_regex

include ../common.mk

LDFLAGS := $(LDFLAGS) -lpthread

echo_server: echo_server.o
	$(CXX) $(CFLAGS) $^ -o $@ $(LDFLAGS)

%.o: %.cpp
	$(CXX) -c $(CFLAGS) -o $@ $^

# cleanup by removing generated files
#
.PHONY:		clean
clean:
		rm -f *.o echo_server
