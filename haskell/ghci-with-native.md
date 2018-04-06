Nick Tchayka

# Using native libraries while using "stack ghci"

Today I had a problem. When executing `stack ghci` for a project that used the `hw-kafka-client` Haskell library, it
complained a lot about the fact that it couldn't find the `librdkafka.so.1` file, even though I had it installed.

I've tried setting the `LD_LIBRARY_PATH` environment variable, adding the `/usr/local/lib` directory to `extra-lib-dirs`,
exposing all the modules that used the `hw-kafka-client` library, and a bunch of other stuff I don't remember now.

## The solution

Just link the library to `/usr/lib`:

```bash
# ln -s /usr/local/lib/librdkafka.so /usr/lib/librdkafka.so
# ln -s /usr/local/lib/librdkafka.so.1 /usr/lib/librdkafka.so.1
```
