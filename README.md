# obj-c

```
// Delay execution of my block for 1 seconds.
dispatch_after(dispatch_time(DISPATCH_TIME_NOW, 1 * NSEC_PER_SEC), dispatch_get_main_queue(), ^{
    //do something here
});
```
