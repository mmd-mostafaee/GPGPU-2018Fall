nvcc_options= -gencode arch=compute_30,code=sm_30 -lm -D TEST --compiler-options -Wall --default-stream per-thread 
sources = vectorOp.cu

all: vectorOp vectorOp_optimized

vectorOp: $(sources) Makefile vectorOp.h
	nvcc -o vectorOp $(sources) $(nvcc_options)

vectorOp_optimized: $(sources) Makefile vectorOp.h
	nvcc -o vectorOp_optimized $(sources) $(nvcc_options) -O3

clean:
	rm vectorOp vectorOp_optimized
