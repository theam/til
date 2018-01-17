Nick Tchayka

# Eta's Ptr is Java's Long

When we get really deep into the low level world of the Haskell compiler, GHC (or Eta, which is based on GHC), we can easily
find ourselves using the pointer type, `Ptr`.

In regular GHC, one would interact with C, and they would pass a pointer to the C program.

But in Eta, we work with Java, so how do we solve this?

Pointers are encoded as `long`!

If we want to access a `ByteBuffer` for example, it is easy to do so by passing the address as a parameter and using the Eta
`MemoryManager` class:

```java
import eta.runtime.io.MemoryManager;
import java.nio.ByteBuffer;

public static void foo(long address){
  ByteBuffer buffer = MemoryManager.getBoundedBuffer(address);
  buffer.put(/* data to put in buffer */);
}
```

And on the Eta side:

```haskell
foreign import java unsafe "@static Utils.foo"
  foo :: Ptr TypeOfOurContent -> IO ()
```
