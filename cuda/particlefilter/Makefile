#makefile

include ../../common/make.config

CC := $(CUDA_DIR)/bin/nvcc

INCLUDE := $(CUDA_DIR)/include

all: particlefilter_naive particlefilter_float

particlefilter_naive: ex_particle_CUDA_naive_seq.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math ex_particle_CUDA_naive_seq.cu -o $@
	
particlefilter_float: ex_particle_CUDA_float_seq.cu
	$(CC) -I$(INCLUDE) -L$(CUDA_LIB_DIR) -lcuda -g -lm -O3 -use_fast_math ex_particle_CUDA_float_seq.cu -o $@

clean:
	rm particlefilter_naive particlefilter_float
