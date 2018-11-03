cmake_minimum_required(VERSION 3.6)
project(RDMA_Tutorial C)

set(CMAKE_C_STANDARD 11)

add_executable(rdma-tutorial
        client.c
        config.c
        ib.c
        main.c
        server.c
        setup_ib.c
        sock.c)
target_link_libraries(rdma-tutorial pthread rdmacm ibverbs)
