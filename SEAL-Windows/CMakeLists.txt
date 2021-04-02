cmake_minimum_required(VERSION 3.10)
project(decryption CXX CUDA)

#add_library(decryptionLibrary STATIC
#    bfv_decryption.cuh
#    helper.h
#    ntt_60bit.cuh
#    parameter.h
#    poly_arithmetic.cuh
#    salsa_common.h
#    uint128.h
#    )

#add_executable(decryption decryption_test.cu)
add_executable(decryption decryption_test.cu bfv_decryption.cuh helper.h ntt_60bit.cuh parameter.h poly_arithmetic.cuh salsa_common.h uint128.h)
find_package(SEAL)
target_link_libraries(decryption SEAL::seal)
set_target_properties(
    decryption
    PROPERTIES CUDA_SEPERABLE_COMPULATION ON)
set_property(TARGET decryption PROPERTY CUDA_ARCHITECTURES 35 50 72)