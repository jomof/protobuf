
cmake_minimum_required(VERSION 3.7)
project(protobuf)
set(SOURCE_ROOT "../src")
add_library(protobuf STATIC 
#  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_x86_gcc.cc        
#  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_x86_msvc.cc       
  ${SOURCE_ROOT}/google/protobuf/stubs/bytestream.cc                          
  ${SOURCE_ROOT}/google/protobuf/stubs/common.cc                              
  ${SOURCE_ROOT}/google/protobuf/stubs/int128.cc                              
  ${SOURCE_ROOT}/google/protobuf/stubs/once.cc                                
  ${SOURCE_ROOT}/google/protobuf/stubs/status.cc                              
  ${SOURCE_ROOT}/google/protobuf/stubs/statusor.cc                            
  ${SOURCE_ROOT}/google/protobuf/stubs/stringpiece.cc                         
  ${SOURCE_ROOT}/google/protobuf/stubs/stringprintf.cc                        
  ${SOURCE_ROOT}/google/protobuf/stubs/structurally_valid.cc                  
  ${SOURCE_ROOT}/google/protobuf/stubs/strutil.cc                             
  ${SOURCE_ROOT}/google/protobuf/stubs/time.cc                                
  ${SOURCE_ROOT}/google/protobuf/arena.cc                                     
  ${SOURCE_ROOT}/google/protobuf/arenastring.cc                               
  ${SOURCE_ROOT}/google/protobuf/extension_set.cc                             
  ${SOURCE_ROOT}/google/protobuf/generated_message_util.cc                    
  ${SOURCE_ROOT}/google/protobuf/message_lite.cc                              
  ${SOURCE_ROOT}/google/protobuf/repeated_field.cc                            
  ${SOURCE_ROOT}/google/protobuf/wire_format_lite.cc                          
  ${SOURCE_ROOT}/google/protobuf/io/coded_stream.cc                           
  ${SOURCE_ROOT}/google/protobuf/io/zero_copy_stream.cc                       
  ${SOURCE_ROOT}/google/protobuf/io/zero_copy_stream_impl_lite.cc
  ${SOURCE_ROOT}/google/protobuf/any.pb.cc                                   
  ${SOURCE_ROOT}/google/protobuf/api.pb.cc                                   
  ${SOURCE_ROOT}/google/protobuf/stubs/mathlimits.cc                         
  ${SOURCE_ROOT}/google/protobuf/stubs/mathlimits.h                          
  ${SOURCE_ROOT}/google/protobuf/any.cc                                      
  ${SOURCE_ROOT}/google/protobuf/descriptor.cc                               
  ${SOURCE_ROOT}/google/protobuf/descriptor_database.cc                      
  ${SOURCE_ROOT}/google/protobuf/descriptor.pb.cc                            
  ${SOURCE_ROOT}/google/protobuf/duration.pb.cc                              
  ${SOURCE_ROOT}/google/protobuf/dynamic_message.cc                          
  ${SOURCE_ROOT}/google/protobuf/empty.pb.cc                                 
  ${SOURCE_ROOT}/google/protobuf/extension_set_heavy.cc                      
  ${SOURCE_ROOT}/google/protobuf/field_mask.pb.cc                            
  ${SOURCE_ROOT}/google/protobuf/generated_message_reflection.cc             
  ${SOURCE_ROOT}/google/protobuf/map_field.cc                                
  ${SOURCE_ROOT}/google/protobuf/message.cc                                  
  ${SOURCE_ROOT}/google/protobuf/reflection_internal.h                       
  ${SOURCE_ROOT}/google/protobuf/reflection_ops.cc                           
  ${SOURCE_ROOT}/google/protobuf/service.cc                                  
  ${SOURCE_ROOT}/google/protobuf/source_context.pb.cc                        
  ${SOURCE_ROOT}/google/protobuf/struct.pb.cc                                
  ${SOURCE_ROOT}/google/protobuf/stubs/substitute.cc                         
  ${SOURCE_ROOT}/google/protobuf/stubs/substitute.h                          
  ${SOURCE_ROOT}/google/protobuf/text_format.cc                              
  ${SOURCE_ROOT}/google/protobuf/timestamp.pb.cc                             
  ${SOURCE_ROOT}/google/protobuf/type.pb.cc                                  
  ${SOURCE_ROOT}/google/protobuf/unknown_field_set.cc                        
  ${SOURCE_ROOT}/google/protobuf/wire_format.cc                              
  ${SOURCE_ROOT}/google/protobuf/wrappers.pb.cc                              
  ${SOURCE_ROOT}/google/protobuf/io/gzip_stream.cc                           
  ${SOURCE_ROOT}/google/protobuf/io/printer.cc                               
  ${SOURCE_ROOT}/google/protobuf/io/strtod.cc                                
  ${SOURCE_ROOT}/google/protobuf/io/tokenizer.cc                             
  ${SOURCE_ROOT}/google/protobuf/io/zero_copy_stream_impl.cc                 
  ${SOURCE_ROOT}/google/protobuf/compiler/importer.cc                        
  ${SOURCE_ROOT}/google/protobuf/compiler/parser.cc                          
  ${SOURCE_ROOT}/google/protobuf/util/field_comparator.cc                    
  ${SOURCE_ROOT}/google/protobuf/util/field_mask_util.cc                     
  ${SOURCE_ROOT}/google/protobuf/util/internal/constants.h                   
  ${SOURCE_ROOT}/google/protobuf/util/internal/datapiece.cc                  
  ${SOURCE_ROOT}/google/protobuf/util/internal/datapiece.h                   
  ${SOURCE_ROOT}/google/protobuf/util/internal/default_value_objectwriter.cc 
  ${SOURCE_ROOT}/google/protobuf/util/internal/default_value_objectwriter.h  
  ${SOURCE_ROOT}/google/protobuf/util/internal/error_listener.cc             
  ${SOURCE_ROOT}/google/protobuf/util/internal/error_listener.h              
  ${SOURCE_ROOT}/google/protobuf/util/internal/expecting_objectwriter.h      
  ${SOURCE_ROOT}/google/protobuf/util/internal/field_mask_utility.cc         
  ${SOURCE_ROOT}/google/protobuf/util/internal/field_mask_utility.h          
  ${SOURCE_ROOT}/google/protobuf/util/internal/json_escaping.cc              
  ${SOURCE_ROOT}/google/protobuf/util/internal/json_escaping.h               
  ${SOURCE_ROOT}/google/protobuf/util/internal/json_objectwriter.cc          
  ${SOURCE_ROOT}/google/protobuf/util/internal/json_objectwriter.h           
  ${SOURCE_ROOT}/google/protobuf/util/internal/json_stream_parser.cc         
  ${SOURCE_ROOT}/google/protobuf/util/internal/json_stream_parser.h          
  ${SOURCE_ROOT}/google/protobuf/util/internal/location_tracker.h            
  ${SOURCE_ROOT}/google/protobuf/util/internal/mock_error_listener.h         
  ${SOURCE_ROOT}/google/protobuf/util/internal/object_location_tracker.h     
  ${SOURCE_ROOT}/google/protobuf/util/internal/object_source.h               
  ${SOURCE_ROOT}/google/protobuf/util/internal/object_writer.cc              
  ${SOURCE_ROOT}/google/protobuf/util/internal/object_writer.h               
  ${SOURCE_ROOT}/google/protobuf/util/internal/protostream_objectsource.cc   
  ${SOURCE_ROOT}/google/protobuf/util/internal/protostream_objectsource.h    
  ${SOURCE_ROOT}/google/protobuf/util/internal/protostream_objectwriter.cc   
  ${SOURCE_ROOT}/google/protobuf/util/internal/protostream_objectwriter.h    
  ${SOURCE_ROOT}/google/protobuf/util/internal/proto_writer.cc               
  ${SOURCE_ROOT}/google/protobuf/util/internal/proto_writer.h                
  ${SOURCE_ROOT}/google/protobuf/util/internal/structured_objectwriter.h     
  ${SOURCE_ROOT}/google/protobuf/util/internal/type_info.cc                  
  ${SOURCE_ROOT}/google/protobuf/util/internal/type_info.h                   
  ${SOURCE_ROOT}/google/protobuf/util/internal/type_info_test_helper.cc      
  ${SOURCE_ROOT}/google/protobuf/util/internal/type_info_test_helper.h       
  ${SOURCE_ROOT}/google/protobuf/util/internal/utility.cc                    
  ${SOURCE_ROOT}/google/protobuf/util/internal/utility.h                     
  ${SOURCE_ROOT}/google/protobuf/util/json_util.cc                           
  ${SOURCE_ROOT}/google/protobuf/util/message_differencer.cc                 
  ${SOURCE_ROOT}/google/protobuf/util/time_util.cc                           
  ${SOURCE_ROOT}/google/protobuf/util/type_resolver_util.cc
)

target_include_directories(protobuf PRIVATE ../src)

target_link_libraries(protobuf pthread)

file(COPY 
  ${SOURCE_ROOT}/google/protobuf/stubs/atomic_sequence_num.h                   
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops.h                             
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_power.h             
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_ppc_gcc.h           
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_arm64_gcc.h         
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_arm_gcc.h           
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_arm_qnx.h           
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_atomicword_compat.h 
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_generic_c11_atomic.h
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_generic_gcc.h       
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_mips_gcc.h          
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_solaris.h           
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_tsan.h              
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_x86_gcc.h           
  ${SOURCE_ROOT}/google/protobuf/stubs/atomicops_internals_x86_msvc.h          
  ${SOURCE_ROOT}/google/protobuf/stubs/callback.h                              
  ${SOURCE_ROOT}/google/protobuf/stubs/bytestream.h                            
  ${SOURCE_ROOT}/google/protobuf/stubs/casts.h                                 
  ${SOURCE_ROOT}/google/protobuf/stubs/common.h                                
  ${SOURCE_ROOT}/google/protobuf/stubs/fastmem.h                               
  ${SOURCE_ROOT}/google/protobuf/stubs/hash.h                                  
  ${SOURCE_ROOT}/google/protobuf/stubs/logging.h                               
  ${SOURCE_ROOT}/google/protobuf/stubs/macros.h                                
  ${SOURCE_ROOT}/google/protobuf/stubs/mutex.h                                 
  ${SOURCE_ROOT}/google/protobuf/stubs/once.h                                  
  ${SOURCE_ROOT}/google/protobuf/stubs/platform_macros.h                       
  ${SOURCE_ROOT}/google/protobuf/stubs/port.h                                  
  ${SOURCE_ROOT}/google/protobuf/stubs/scoped_ptr.h                            
  ${SOURCE_ROOT}/google/protobuf/stubs/shared_ptr.h                            
  ${SOURCE_ROOT}/google/protobuf/stubs/singleton.h                             
  ${SOURCE_ROOT}/google/protobuf/stubs/status.h                                
  ${SOURCE_ROOT}/google/protobuf/stubs/stl_util.h                              
  ${SOURCE_ROOT}/google/protobuf/stubs/stringpiece.h                           
  ${SOURCE_ROOT}/google/protobuf/stubs/template_util.h                         
  ${SOURCE_ROOT}/google/protobuf/stubs/type_traits.h                           
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/stubs)

file(COPY 
                       
  ${SOURCE_ROOT}/google/protobuf/any.pb.h                                      
  ${SOURCE_ROOT}/google/protobuf/api.pb.h                                      
  ${SOURCE_ROOT}/google/protobuf/any.h                                         
  ${SOURCE_ROOT}/google/protobuf/arena.h                                       
  ${SOURCE_ROOT}/google/protobuf/arenastring.h                                 
  ${SOURCE_ROOT}/google/protobuf/descriptor_database.h                         
  ${SOURCE_ROOT}/google/protobuf/descriptor.h                                  
  ${SOURCE_ROOT}/google/protobuf/descriptor.pb.h                               
  ${SOURCE_ROOT}/google/protobuf/duration.pb.h                                 
  ${SOURCE_ROOT}/google/protobuf/dynamic_message.h                             
  ${SOURCE_ROOT}/google/protobuf/empty.pb.h                                    
  ${SOURCE_ROOT}/google/protobuf/extension_set.h                               
  ${SOURCE_ROOT}/google/protobuf/field_mask.pb.h                               
  ${SOURCE_ROOT}/google/protobuf/generated_enum_reflection.h                   
  ${SOURCE_ROOT}/google/protobuf/generated_enum_util.h                         
  ${SOURCE_ROOT}/google/protobuf/generated_message_reflection.h                
  ${SOURCE_ROOT}/google/protobuf/generated_message_util.h                      
  ${SOURCE_ROOT}/google/protobuf/has_bits.h                                    
  ${SOURCE_ROOT}/google/protobuf/map_entry.h                                   
  ${SOURCE_ROOT}/google/protobuf/map_entry_lite.h                              
  ${SOURCE_ROOT}/google/protobuf/map_field.h                                   
  ${SOURCE_ROOT}/google/protobuf/map_field_inl.h                               
  ${SOURCE_ROOT}/google/protobuf/map_field_lite.h                              
  ${SOURCE_ROOT}/google/protobuf/map.h                                         
  ${SOURCE_ROOT}/google/protobuf/map_type_handler.h                            
  ${SOURCE_ROOT}/google/protobuf/message.h                                     
  ${SOURCE_ROOT}/google/protobuf/message_lite.h                                
  ${SOURCE_ROOT}/google/protobuf/metadata.h                                    
  ${SOURCE_ROOT}/google/protobuf/reflection.h                                  
  ${SOURCE_ROOT}/google/protobuf/reflection_ops.h                              
  ${SOURCE_ROOT}/google/protobuf/repeated_field.h                              
  ${SOURCE_ROOT}/google/protobuf/service.h                                     
  ${SOURCE_ROOT}/google/protobuf/source_context.pb.h                           
  ${SOURCE_ROOT}/google/protobuf/struct.pb.h                                   
  ${SOURCE_ROOT}/google/protobuf/text_format.h                                 
  ${SOURCE_ROOT}/google/protobuf/timestamp.pb.h                                
  ${SOURCE_ROOT}/google/protobuf/type.pb.h                                     
  ${SOURCE_ROOT}/google/protobuf/unknown_field_set.h                           
  ${SOURCE_ROOT}/google/protobuf/wire_format.h                                 
  ${SOURCE_ROOT}/google/protobuf/wire_format_lite.h                            
  ${SOURCE_ROOT}/google/protobuf/wire_format_lite_inl.h                        
  ${SOURCE_ROOT}/google/protobuf/wrappers.pb.h                                 
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/)

file(COPY                  
  ${SOURCE_ROOT}/google/protobuf/io/coded_stream.h                                                                             
  ${SOURCE_ROOT}/google/protobuf/io/printer.h                                  
  ${SOURCE_ROOT}/google/protobuf/io/strtod.h                                   
  ${SOURCE_ROOT}/google/protobuf/io/tokenizer.h                                
  ${SOURCE_ROOT}/google/protobuf/io/zero_copy_stream.h                         
  ${SOURCE_ROOT}/google/protobuf/io/zero_copy_stream_impl.h                    
  ${SOURCE_ROOT}/google/protobuf/io/zero_copy_stream_impl_lite.h               
 
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/io)

file(COPY                                  
  ${SOURCE_ROOT}/google/protobuf/compiler/cpp/cpp_generator.h                  
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler/cpp)

file(COPY                        
  ${SOURCE_ROOT}/google/protobuf/compiler/csharp/csharp_generator.h            
  ${SOURCE_ROOT}/google/protobuf/compiler/csharp/csharp_names.h                          
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler/csharp)

file(COPY                         
  ${SOURCE_ROOT}/google/protobuf/compiler/java/java_generator.h                
  ${SOURCE_ROOT}/google/protobuf/compiler/java/java_names.h                                
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler/java)

file(COPY                             
  ${SOURCE_ROOT}/google/protobuf/compiler/javanano/javanano_generator.h        
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler/javanano)

file(COPY                  
  ${SOURCE_ROOT}/google/protobuf/compiler/js/js_generator.h                    
  ${SOURCE_ROOT}/google/protobuf/compiler/js/well_known_types_embed.h          
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler/js)

file(COPY                   
  ${SOURCE_ROOT}/google/protobuf/compiler/objectivec/objectivec_generator.h    
  ${SOURCE_ROOT}/google/protobuf/compiler/objectivec/objectivec_helpers.h             
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler/objectivec)

file(COPY             
  ${SOURCE_ROOT}/google/protobuf/compiler/php/php_generator.h                  
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler/php)

file(COPY                         
  ${SOURCE_ROOT}/google/protobuf/compiler/python/python_generator.h                      
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler/python)

file(COPY                    
  ${SOURCE_ROOT}/google/protobuf/compiler/ruby/ruby_generator.h                
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler/ruby)

file(COPY             
  ${SOURCE_ROOT}/google/protobuf/compiler/code_generator.h                     
  ${SOURCE_ROOT}/google/protobuf/compiler/command_line_interface.h             
  ${SOURCE_ROOT}/google/protobuf/compiler/importer.h                           
  ${SOURCE_ROOT}/google/protobuf/compiler/parser.h                             
  ${SOURCE_ROOT}/google/protobuf/compiler/plugin.h                             
  ${SOURCE_ROOT}/google/protobuf/compiler/plugin.pb.h                          
  ${SOURCE_ROOT}/google/protobuf/compiler/cpp/cpp_generator.h                  
  ${SOURCE_ROOT}/google/protobuf/compiler/csharp/csharp_generator.h            
  ${SOURCE_ROOT}/google/protobuf/compiler/csharp/csharp_names.h                
  ${SOURCE_ROOT}/google/protobuf/compiler/java/java_generator.h                
  ${SOURCE_ROOT}/google/protobuf/compiler/java/java_names.h                    
  ${SOURCE_ROOT}/google/protobuf/compiler/javanano/javanano_generator.h        
  ${SOURCE_ROOT}/google/protobuf/compiler/js/js_generator.h                    
  ${SOURCE_ROOT}/google/protobuf/compiler/js/well_known_types_embed.h          
  ${SOURCE_ROOT}/google/protobuf/compiler/objectivec/objectivec_generator.h    
  ${SOURCE_ROOT}/google/protobuf/compiler/objectivec/objectivec_helpers.h      
  ${SOURCE_ROOT}/google/protobuf/compiler/php/php_generator.h                  
  ${SOURCE_ROOT}/google/protobuf/compiler/python/python_generator.h            
  ${SOURCE_ROOT}/google/protobuf/compiler/ruby/ruby_generator.h                
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/compiler)

file(COPY             
  ${SOURCE_ROOT}/google/protobuf/util/type_resolver.h                          
  ${SOURCE_ROOT}/google/protobuf/util/field_comparator.h                       
  ${SOURCE_ROOT}/google/protobuf/util/field_mask_util.h                        
  ${SOURCE_ROOT}/google/protobuf/util/json_util.h                              
  ${SOURCE_ROOT}/google/protobuf/util/time_util.h                              
  ${SOURCE_ROOT}/google/protobuf/util/type_resolver_util.h                     
  ${SOURCE_ROOT}/google/protobuf/util/message_differencer.h
  
  DESTINATION ${CMAKEIFY_REDIST_INCLUDE_DIRECTORY}/google/protobuf/util)

