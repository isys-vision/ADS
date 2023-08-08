add_executable(AdsTool main.cpp)
target_link_libraries(AdsTool PUBLIC ads::ads)

# export library (either static or shared depending on BUILD_SHARED_LIBS)
install(TARGETS AdsTool
  EXPORT adsTargets
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib
  RUNTIME DESTINATION bin
  INCLUDES DESTINATION include
  )
