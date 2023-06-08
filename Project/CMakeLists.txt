add_library (Project 
  MyClass.h
  MyClass.cpp)

install (TARGETS Project DESTINATION bin)
install (FILES MyClass.h DESTINATION include)
