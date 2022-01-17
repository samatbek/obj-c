# Objective-C syntax cheat sheet

#### Delay execution of my block for 1 seconds.
```objc
dispatch_after(dispatch_time(DISPATCH_TIME_NOW, 1 * NSEC_PER_SEC), dispatch_get_main_queue(), ^{
    //do something here
});
```
### Block syntax
#### As a local variable:

```objc
returnType (^blockName)(parameterTypes) = ^returnType(parameters) {...};
```

#### As a property:
```objc
@property (nonatomic, copy, nullability) returnType (^blockName)(parameterTypes);
```

#### As a method parameter:
```objc
- (void)someMethodThatTakesABlock:(returnType (^nullability)(parameterTypes))blockName;
```

#### As an argument to a method call:
```objc
[someObject someMethodThatTakesABlock:^returnType (parameters) {...}];
```

#### As a parameter to a C function:
```objc
void SomeFunctionThatTakesABlock(returnType (^blockName)(parameterTypes));
```
#### As a typedef:
```objc
typedef returnType (^TypeName)(parameterTypes);
TypeName blockName = ^returnType(parameters) {...};
```
