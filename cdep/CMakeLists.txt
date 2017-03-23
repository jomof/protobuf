
cmake_minimum_required(VERSION 3.7)
project(protobuf)
set(SOURCE_ROOT "../src/google/protobuf")
add_library(protobuf STATIC 
  ${SOURCE_ROOT}/stubs/atomicops_internals_x86_gcc.cc        
  ${SOURCE_ROOT}/stubs/atomicops_internals_x86_msvc.cc       
  ${SOURCE_ROOT}/stubs/bytestream.cc                          
  ${SOURCE_ROOT}/stubs/common.cc                              
  ${SOURCE_ROOT}/stubs/int128.cc                              
  ${SOURCE_ROOT}/stubs/once.cc                                
  ${SOURCE_ROOT}/stubs/status.cc                              
  ${SOURCE_ROOT}/stubs/statusor.cc                            
  ${SOURCE_ROOT}/stubs/stringpiece.cc                         
  ${SOURCE_ROOT}/stubs/stringprintf.cc                        
  ${SOURCE_ROOT}/stubs/structurally_valid.cc                  
  ${SOURCE_ROOT}/stubs/strutil.cc                             
  ${SOURCE_ROOT}/stubs/time.cc                                
  ${SOURCE_ROOT}/arena.cc                                     
  ${SOURCE_ROOT}/arenastring.cc                               
  ${SOURCE_ROOT}/extension_set.cc                             
  ${SOURCE_ROOT}/generated_message_util.cc                    
  ${SOURCE_ROOT}/message_lite.cc                              
  ${SOURCE_ROOT}/repeated_field.cc                            
  ${SOURCE_ROOT}/wire_format_lite.cc                          
  ${SOURCE_ROOT}/io/coded_stream.cc                           
  ${SOURCE_ROOT}/io/zero_copy_stream.cc                       
  ${SOURCE_ROOT}/io/zero_copy_stream_impl_lite.cc
  ${SOURCE_ROOT}/any.pb.cc                                   
  ${SOURCE_ROOT}/api.pb.cc                                   
  ${SOURCE_ROOT}/stubs/mathlimits.cc                         
  ${SOURCE_ROOT}/stubs/mathlimits.h                          
  ${SOURCE_ROOT}/any.cc                                      
  ${SOURCE_ROOT}/descriptor.cc                               
  ${SOURCE_ROOT}/descriptor_database.cc                      
  ${SOURCE_ROOT}/descriptor.pb.cc                            
  ${SOURCE_ROOT}/duration.pb.cc                              
  ${SOURCE_ROOT}/dynamic_message.cc                          
  ${SOURCE_ROOT}/empty.pb.cc                                 
  ${SOURCE_ROOT}/extension_set_heavy.cc                      
  ${SOURCE_ROOT}/field_mask.pb.cc                            
  ${SOURCE_ROOT}/generated_message_reflection.cc             
  ${SOURCE_ROOT}/map_field.cc                                
  ${SOURCE_ROOT}/message.cc                                  
  ${SOURCE_ROOT}/reflection_internal.h                       
  ${SOURCE_ROOT}/reflection_ops.cc                           
  ${SOURCE_ROOT}/service.cc                                  
  ${SOURCE_ROOT}/source_context.pb.cc                        
  ${SOURCE_ROOT}/struct.pb.cc                                
  ${SOURCE_ROOT}/stubs/substitute.cc                         
  ${SOURCE_ROOT}/stubs/substitute.h                          
  ${SOURCE_ROOT}/text_format.cc                              
  ${SOURCE_ROOT}/timestamp.pb.cc                             
  ${SOURCE_ROOT}/type.pb.cc                                  
  ${SOURCE_ROOT}/unknown_field_set.cc                        
  ${SOURCE_ROOT}/wire_format.cc                              
  ${SOURCE_ROOT}/wrappers.pb.cc                              
  ${SOURCE_ROOT}/io/gzip_stream.cc                           
  ${SOURCE_ROOT}/io/printer.cc                               
  ${SOURCE_ROOT}/io/strtod.cc                                
  ${SOURCE_ROOT}/io/tokenizer.cc                             
  ${SOURCE_ROOT}/io/zero_copy_stream_impl.cc                 
  ${SOURCE_ROOT}/compiler/importer.cc                        
  ${SOURCE_ROOT}/compiler/parser.cc                          
  ${SOURCE_ROOT}/util/field_comparator.cc                    
  ${SOURCE_ROOT}/util/field_mask_util.cc                     
  ${SOURCE_ROOT}/util/internal/constants.h                   
  ${SOURCE_ROOT}/util/internal/datapiece.cc                  
  ${SOURCE_ROOT}/util/internal/datapiece.h                   
  ${SOURCE_ROOT}/util/internal/default_value_objectwriter.cc 
  ${SOURCE_ROOT}/util/internal/default_value_objectwriter.h  
  ${SOURCE_ROOT}/util/internal/error_listener.cc             
  ${SOURCE_ROOT}/util/internal/error_listener.h              
  ${SOURCE_ROOT}/util/internal/expecting_objectwriter.h      
  ${SOURCE_ROOT}/util/internal/field_mask_utility.cc         
  ${SOURCE_ROOT}/util/internal/field_mask_utility.h          
  ${SOURCE_ROOT}/util/internal/json_escaping.cc              
  ${SOURCE_ROOT}/util/internal/json_escaping.h               
  ${SOURCE_ROOT}/util/internal/json_objectwriter.cc          
  ${SOURCE_ROOT}/util/internal/json_objectwriter.h           
  ${SOURCE_ROOT}/util/internal/json_stream_parser.cc         
  ${SOURCE_ROOT}/util/internal/json_stream_parser.h          
  ${SOURCE_ROOT}/util/internal/location_tracker.h            
  ${SOURCE_ROOT}/util/internal/mock_error_listener.h         
  ${SOURCE_ROOT}/util/internal/object_location_tracker.h     
  ${SOURCE_ROOT}/util/internal/object_source.h               
  ${SOURCE_ROOT}/util/internal/object_writer.cc              
  ${SOURCE_ROOT}/util/internal/object_writer.h               
  ${SOURCE_ROOT}/util/internal/protostream_objectsource.cc   
  ${SOURCE_ROOT}/util/internal/protostream_objectsource.h    
  ${SOURCE_ROOT}/util/internal/protostream_objectwriter.cc   
  ${SOURCE_ROOT}/util/internal/protostream_objectwriter.h    
  ${SOURCE_ROOT}/util/internal/proto_writer.cc               
  ${SOURCE_ROOT}/util/internal/proto_writer.h                
  ${SOURCE_ROOT}/util/internal/structured_objectwriter.h     
  ${SOURCE_ROOT}/util/internal/type_info.cc                  
  ${SOURCE_ROOT}/util/internal/type_info.h                   
  ${SOURCE_ROOT}/util/internal/type_info_test_helper.cc      
  ${SOURCE_ROOT}/util/internal/type_info_test_helper.h       
  ${SOURCE_ROOT}/util/internal/utility.cc                    
  ${SOURCE_ROOT}/util/internal/utility.h                     
  ${SOURCE_ROOT}/util/json_util.cc                           
  ${SOURCE_ROOT}/util/message_differencer.cc                 
  ${SOURCE_ROOT}/util/time_util.cc                           
  ${SOURCE_ROOT}/util/type_resolver_util.cc
)

target_include_directories(protobuf PRIVATE ../src)

target_link_libraries(protobuf pthread)

#file(COPY sqlite-amalgamation-3160200/sqlite3.h DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY})

