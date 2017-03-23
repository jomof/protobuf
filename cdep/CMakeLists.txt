
cmake_minimum_required(VERSION 3.7)
project(protobuf)
set(SOURCE_ROOT, "../src/google/protobuf")
add_library(protobuf STATIC 
  google/protobuf/stubs/atomicops_internals_x86_gcc.cc        
  google/protobuf/stubs/atomicops_internals_x86_msvc.cc       
  google/protobuf/stubs/bytestream.cc                          
  google/protobuf/stubs/common.cc                              
  google/protobuf/stubs/int128.cc                              
  google/protobuf/stubs/once.cc                                
  google/protobuf/stubs/status.cc                              
  google/protobuf/stubs/statusor.cc                            
  google/protobuf/stubs/stringpiece.cc                         
  google/protobuf/stubs/stringprintf.cc                        
  google/protobuf/stubs/structurally_valid.cc                  
  google/protobuf/stubs/strutil.cc                             
  google/protobuf/stubs/time.cc                                
  google/protobuf/arena.cc                                     
  google/protobuf/arenastring.cc                               
  google/protobuf/extension_set.cc                             
  google/protobuf/generated_message_util.cc                    
  google/protobuf/message_lite.cc                              
  google/protobuf/repeated_field.cc                            
  google/protobuf/wire_format_lite.cc                          
  google/protobuf/io/coded_stream.cc                           
  google/protobuf/io/zero_copy_stream.cc                       
  google/protobuf/io/zero_copy_stream_impl_lite.cc
)
#file(COPY sqlite-amalgamation-3160200/sqlite3.h DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY})

