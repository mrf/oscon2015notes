# Go Performance
- Write simple code and let the compiler help you <- its designed to do this
- Knuth "Premature op root of all evil quote" but this doesnt' apply if you don't have to work too hard to write code for more performant
- always use the latest version of Go

## Tools
- testing framework supports benchmarking 
  - "go test -bench=." to run them all
    - -benchtime (number of combined secs defaults to 1)
    - -benchmem (memory used)
- if processing data can pass bytes to get throughput
- benchcmp (for beginners) benchvis and benchstat (for statisticians) for combining / comparing benchmarks
- pprof < tool for profiling go applications 
  - has crappy ui but generates beautiful call graphs even with line numbers
-  "go test -bench=. -cpuprofile"
-  "go test -bench=. -memprofile"
- execution tracing coming to Go 1.5
  - super cutting edge, powerful, and dense, tons of info

## Tips and Techniques for writing more performant code
- strings
  - slicing cheap
  - concatanation expensive
    - bytes.Buffer less expnsive way to work with strings
      - go programmers love buffers because of this
  - don't switch between strings and bytes until you have to
    - last minute is best for conversion since data should be as small as possible then

# Allocation
- for cpuy things the number of allocations matters more than the size
- stack vs heap < go tries to leave as much as it can on the stack
## Allocation Habits
- buffers vs streams stream usually best only sips what it needs
- go easy on abstraction, go wants you to be concrete

- Don't leak goroutines, can use profiler to check in on this
