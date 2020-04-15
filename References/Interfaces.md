# Interfaces
Interfaces in Unreal Engine are an extremely useful tool though I feel they are underused because of the difficulty with implementation. These dont use standard C++ interfaces, tney have more in common with java interfaces but you have to be careful because the compiler has no knowledge so it wont give you clean error messages.

Interfaces can help you cut down on casting classes saving resources in the process, you can easily implement the same function across classes but interfaces allow you to call the function without knowing the class of the object by calling through the implemented interface instead.

## Interface Declaration
Header
```c++
UINTERFACE(MinimalAPI, Blueprintable)
class UYourInterface : public UInterface
{
    GENERATED_BODY()
};
```
Source
```c++
class PROJECT_API IYourInterface
{
    GENERATED_BODY()

    // Add interface functions to this class. This is the class that will be inherited to implement this interface.
public:
    virtual bool InterfaceFunction(SomeType* const TypePtr, const float& SomeFloat, const TArray<FText>& SomeTextEntries);
};
```
Actor header (override declaration)
```c++
class PROJECT_API AMyActor : public AActor, public IMyInterface

virtual bool InterfaceFunction(SomeType* const TypePtr, const float& SomeFloat, const TArray<FText>& SomeTextEntries);
```
Actor source (override definition)
```c++
bool AMyActor::InterfaceFunction(SomeType* const TypePtr, const float& SomeFloat, const TArray<FText>& SomeTextEntries) 
{
    /* some arbitrary code here */
}
```

Be sure to check your returns.

* Expand to cover UFUNCTIONS defined in Interfaces
* Overlap between Delegates and Interfaces


Back to [Main Page](../README.md)