###
# 5/5/2023
###

#		Fill in your name, email address, and the lab number, leaving the quotes
LAST_NAME	= "NORDLUND"
FIRST_NAME	= "HENRY"

#		The name of the executable file
EXECUTABLE	= /home/.../cmake-builder/out/build/x64-Debug/src/UPDATE.exe

#		Source files you want to compile
#		(NOTE: Don't include header (.h) files, or source (.cc) files
#		that only contain template class method definitions.)
CMPL_SRCS	= /home/.../cmake-builder/src/main.cpp

#               Source files containing only template class method definitions
TMPL_SRCS	= 

#               Header files
HEADER_FILES    = /home/.../cmake-builder/src/main.h

#               Other files to turn in (i.e., readme, output files, etc)
OTHER_FILES     = readme

#               Any special flags that should be set for compilation
SPECIAL_FLAGS  = -pedantic
                                                                             #
#################### DO NOT CHANGE ANYTHING BELOW THIS LINE ###################

#		C++ compiler
CXX		= g++

#               All your source files (needed for executable dependency)
USER_SRCS        = $(CMPL_SRCS) $(TMPL_SRCS) $(HEADER_FILES)

#               Provided source files (i.e., History files, etc)
PROVIDED_SRCS   =

#               All your source files (needed for executable dependency)
ALL_SRCS        = $(USER_SRCS) $(PROVIDED_SRCS)

#               All files to turn in (including readme, output files, etc)
ALL_FILES       = $(USER_SRCS) $(OTHER_FILES)

#               The list of libraries that should be linked in
#LIBS    =       -lsocket -lnsl
LIBS    =       -lnsl

#               The name of the compiler
CCC      = $(CXX)

#               The name of the previewer (pageview or ghostview)
PREVIEWER = /usr/openwin/bin/pageview -right

#              Names of object files (from names of source files)
OBJS     = $(CMPL_SRCS:.cc=.o)

#               Any define flags that should be set for conditional compilation
DEFFLAGS  = -DUNIX

#               Any general flags that should be set for the compiler
#               NOTE: to optimize fully, change -g to -O4
CXXFLAGS  =     -Wall -W -g $(SPECIAL_FLAGS)

#               Any -I directories in which there are .h files that should be included
INCFLAGS  =
#               Flags that are specific to SUN object code
SUNFLAGS  =  #-misalign

#               The concatenation of all the flags that the compiler should get
CCFLAGS = $(DEFFLAGS) $(INCFLAGS) $(SUNFLAGS) $(CXXFLAGS)

###
# Targets
###

#               Special "all" target expected by Eclipse.
all: $(EXECUTABLE)

#               Construct the executable
$(EXECUTABLE): Templates.DB $(OBJS)
	$(CXX) -o $(EXECUTABLE) $(CCFLAGS) $(OBJS) $(LIBS)

#		Remove all junk that might be lying around
clean:
	-rm -f *.o core *.bak *~ ../toturnin ./toturnin
	-rm -fr Templates.DB SunWS_cache *.rpo TEST_TURNIN

realclean: clean
	-rm -f $(EXECUTABLE)

depend:
	-rm -f ccdep
	-rm -f eddep
	$(CXX) -xM $(CCFLAGS) $(CMPL_SRCS) > ccdep
	sed -n '1,/^# DO NOT DELETE THIS LINE/p' Makefile > eddep
	echo \#\#\# >> eddep
	cat ccdep >> eddep
	cp Makefile Makefile.bak
	mv eddep Makefile
	rm ccdep

.SUFFIXES: .cpp
.cpp.o:
	$(COMPILE.cc) $(CCFLAGS) $(OUTPUT_OPTION) $<
.cpp:
	$(LINK.cc) $(LDFLAGS) -o $@ $< $(LDLIBS)

main.o: $(ALL_SRCS) Makefile

#### To avoid Sun CC warning about having to create Templates.DB.
Templates.DB:
	@test -d $@ || mkdir $@

###
# OBJECT FILE DEPENDENCIES FOLLOW.
#
# DO NOT DELETE THIS LINE -- make depend uses it
###
